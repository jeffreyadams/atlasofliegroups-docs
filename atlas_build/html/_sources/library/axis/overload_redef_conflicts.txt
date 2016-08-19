Overloading v.s. Redefining, and Conflicts
=============================================

While the overload table can handle many definitions with the same function
(or operator) name, it must be able to tell them apart by the argument types
(the result type is usually not available when resolving an overloaded call,
so it cannot be used to distinguish overloaded definitions). Moreover some
implicit conversions can be applied to arguments, making some overloaded
argument types incompatible (for instance having separate definitions for
'vec' and '[int]' arguments is not possible, as arguments of these types can
be implicitly converted into one another). However if a new definition exactly
matches the argument types of a previous definition, the new definition is
taken to replace rather than to overload the previous definition. The reply
that axis gives to a definition indicates when this happens, for instance::

  set inner_class (RootDatum rd, string ict)=
  let lt = Lie_type (rd), basis=^coroot_radical(rd)
  in inner_class(rd, involution(lt, basis, ict))

(here and henceforth we suppress prompts for readability) leads to the reply::

  Redefined inner_class: (RootDatum,string->InnerClass)

showing that a previous (in this case built-in) definition of 'inner_class'
has been superseded and has become unavailable (the user-defined version has
replaced it; as it happens, it is almost equivalent to the built-in version).

Here is an example where an attempt to add an overloaded definition for a
different but closely related argument type is refused (attempt to overload
the variant defined above with 'ratvec' second argument with a similar
instance with a '[rat]' second argument::

  set inner_class (LieType lt,[rat] gen,string ict)=
  inner_class(lt, [ratvec: gen],ict)

gives the somewhat elaborate error message::

  Cannot overload `inner_class': previous type (LieType,ratvec,string)
  is too close to (LieType,[rat],string),
  making overloading potentially ambiguous. Broadness cannot disambiguate,
  as either type converts to the other, definition aborted.

The "broadness" phrase relates to the fact that one can for instance overload
with types 'int' and 'rat', even though the former can be implicitly converted
to the latter: since the opposite is not possible, 'rat' is considered the
broader of the two types, and overload resolution will proceed by trying the
broader type only if no matching for the narrower type is possible. But
between 'ratvec' and '[rat]' conversions in either direction are possible, so
axis cannot decide which overload would have to be tried first, whence its
refusal of the overloaded definition. Note that the full argument types here
are '(LieType,ratvec,string)' respectively '(LieType,[rat],string)', which are
not directly convertible (just their second components are), but ambiguity may
still arise in function calls; axis is conservative and prefers to refuse
potentially ambiguous overloads when the ambiguity is introduced, rather than
to wait for a usage that actually exposes the ambiguity (at which point it may
have become hard to hunt down the offending definitions).

If one wants to replace the old definition so that one with a close but
distinct type can be accepted, a command 'forget' can be used; here::

  atlas> forget inner_class@(LieType,ratvec,string)
  Definition of inner_class@(LieType,ratvec,string) forgotten

after which the definition attempted and refused above will be accepted.

Functions can also be unnamed values, which is particularly useful if the are
to be passed as arguments to other functions. So supposing g was defined by::

  atlas> set g ((int->int) f) = vec: [f(0),f(f(1)),f(5)]
  Defined g: ((int->int)->vec)

a function that takes as parameter another function, of type '(int->int)'. As
argument of 'g' one can provide an anonymous function, for instance one that
adds 1 to an integer, which can be denoted by '(int n) : n+1', or to make the
return type explicit '(int n) int: n+1' (the syntax is a parenthesized
parameter list, an optional return type followed by a colon, and an expression
giving the function body). One can now call g with this argument::

  atlas> g((int n):n+1)
  Value: [ 1, 3, 6 ]

One can also call 'g' with a named function 'f'. However since defining a
named function just introduces an overload for the function name, a bare 'f'
does not suffice; one needs to specify the argument type for 'f' in the call
of 'g'::

  atlas> set f (int n) = 3*n+1
  Defined f: (int->int)
  atlas> g(f)
  Error during analysis of expression at...
    Undefined identifier f
  Type check failed
  atlas> g(f@int)
  Value: [  1, 13, 16 ]

Note that 'f' was called "Undefined" even though a function 'f' is defined: in
the call 'g(f)' the name 'f' is not called, and bindings of 'f' in the
overload table are not considered. Using 'set' with a value of function type
always enters in into the overload table, even when it is for instance written::

  atlas> set f = (int n): 3*n+1
  Redefined f: (int->int)

To get a global variable whose value happens to have function type, a special
syntax is provided, namely 'name : function' instead of 'set name = function"::

  atlas>  f : (int n): 2*n+3
  Identifier f: (int->int)
  atlas> g(f)
  Value: [  3, 13, 13 ]

A global identifier defined with a function value in this way can coexist with
one or more overloaded instances for the same name. However, the presence of
overloaded instances make the function variable unavailable for use in direct
function calls, though it can still be used to pass the function value, assign
it to local variables, or assign a new function (of the same type) to it.
::

  atlas> f(10) { overloaded instance }
  Value: 31
  atlas> let ff=f in ff(10) { pass global variable to local one, then call it }
  Value: 23
  atlas> f := ((int n) int: n*n) { syntax requires parentheses here }
  Value: Function defined at <standard input>:...
  (n): *@(int,int)(n,n)
  atlas> g(f) { call g with new value of f }
  Value: [  0,  1, 25 ]

The 'name : value' syntax is also available for values of non-function type,
in which case it is strictly equivalent to 'set name = value'.

Although the design of axis aims at always giving variables a value at their
introduction, deducing their type from that value and avoiding the possibility
of uninitialized variables, it does allow introducing a global variable
without specifying an initial value, but only a type. To this end there is the
variation of the 'name : value' syntax consisting of writing 'name : type'
instead. For instance the function variable 'f' above could have been
introduced by::

  atlas> f: (int->int)
  Declaring identifier 'f': (int->int)

after which it has a type but no value, whence the following gives no type
error but a runtime error::

  atlas> g(f)
  Runtime error:
    Taking value of uninitialized variable 'f'
  Evaluation aborted.

(it would be however possible to use 'f' in unevaluated function definitions
at this point). Before doing anything useful with 'f', it must be assigned to::

  atlas> f := ((int n): 2*n+3)
  Value: Function defined at <standard input>:...
  (n): +@(int,int)(*@(int,int)(2,n),3)
  atlas> g(f)
  Value: [  3, 13, 13 ]

(Note that after the assignment to 'f' its function body is printed in an
internal representation, in which overload resolution has been made explicit
by writing operators prefix and followed by @argument_types; if there had been
any implicit conversion, it would also have been made visible by a somewhat
cryptic code. If a command is an assignment, the value assigned is printed, as
it is for any command that is an expression returning a value; this printing
can however be suppressed by adding ';()' at the end of the command.)
