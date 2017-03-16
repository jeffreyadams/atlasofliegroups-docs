Defining Functions and Operators
===================================

A main use of the axis language is to allow users to define their own
functions. In practice these are often simple functions of not more than a
few lines, providing some simple pre- or post-processing around built-in
operations rather than implementing a whole new algorithm, and the language is
particularly well adapted to such usage; nonetheless it also allows for
writing elaborate functions whose body can be as large as one wishes.

Often it is convenient to have user defined functions invoked from formulas
using operator symbols. While one cannot define new operator symbols, one can
overload existing ones for new argument types. Defining operator overloads is
very similar to defining (global) functions.

The normal way to define a function is using a variation of the 'set' syntax
(which also has counterpart for 'let'), as in::

  atlas> set f (LieType lt) = void:
  : > let rd = simply_connected (lt)
  L > then ic = inner_class(rd,"s")
  L > then rf = quasisplit_form (ic) , drf = dual_quasisplit_form (ic)
  L > in print_block(block(rf,drf))
  Defined f: (LieType->)
  atlas> f("A2")
  0(0,5):  0  0  [C+,C+]  2  1   (*,*)  (*,*)   e
  1(1,4):  1  0  [i2,C-]  1  0   (3,4)  (*,*)   2,1
  2(2,3):  1  0  [C-,i2]  0  2   (*,*)  (3,5)   1,2
  3(3,0):  2  1  [r2,r2]  4  5   (1,*)  (2,*)   1,2,1
  4(3,1):  2  1  [r2,rn]  3  4   (1,*)  (*,*)   1,2,1
  5(3,2):  2  1  [rn,r2]  5  3   (*,*)  (2,*)   1,2,1
  atlas> f("G2")
   0(0,9):  0  [i1,i1]   1   2   ( 4, *)  ( 3, *)  0  e
   1(1,9):  0  [i1,ic]   0   1   ( 4, *)  ( *, *)  0  e
   2(2,9):  0  [ic,i1]   2   0   ( *, *)  ( 3, *)  0  e
   3(3,8):  1  [C+,r1]   6   3   ( *, *)  ( 0, 2)  2  2
   4(4,7):  1  [r1,C+]   4   5   ( 0, 1)  ( *, *)  1  1
   5(5,6):  2  [C+,C-]   8   4   ( *, *)  ( *, *)  1  2,1,2
   6(6,5):  2  [C-,C+]   3   7   ( *, *)  ( *, *)  2  1,2,1
   7(7,4):  3  [i2,C-]   7   6   ( 9,10)  ( *, *)  2  2,1,2,1,2
   8(8,3):  3  [C-,i2]   5   8   ( *, *)  ( 9,11)  1  1,2,1,2,1
   9(9,0):  4  [r2,r2]  10  11   ( 7, *)  ( 8, *)  3  1,2,1,2,1,2
  10(9,1):  4  [r2,rn]   9  10   ( 7, *)  ( *, *)  3  1,2,1,2,1,2
  11(9,2):  4  [rn,r2]  11   9   ( *, *)  ( 8, *)  3  1,2,1,2,1,2

The syntax for defining a function or operator instance is: 'set' followed by
the function or operator name, then enclosed in parentheses a (possibly empty)
parameter list containing pairs of the form '<type> <identifier>' separated by
commas, then '=', and finally the expression giving the function body.

In the example the function body is a cast starting with 'void:', making clear
on inspection that the return type is void (no useful return value). While
this is a useful convention, which costs nothing at run time because casts are
removed after type analysis, it is not obligatory: most of the time axis can
find the return type by itself (and in the example it would without the cast);
the reply it gives to the command, here 'Defined f: (LieType->)', indicates
which type it has found. Note that when calling 'f' we provided a 'string'
rather than a 'Lie_type' value; axis has inserted the necessary conversion
implicitly when analyzing those calls.

The example also illustrates a typical composition of the function body
consisting of a 'let' construction introducing a sequence of introductions of
local variables: here first 'rd', next (separated by 'then', which in this
context is equivalent to 'in let') 'ic', and finally (after another 'then')
'rf' and 'drf' (in parallel, separated by a comma) and finally calling (after
'in') the function 'print_block' with a nested call to 'block'. The final call
returns no value, which matches the 'void' type in the initial cast: the
function 'f' returns no value and gets type (LieType->). Note that after
calling the function 'f', the usual 'Value:' line before the next prompt is
absent; this is a special provision for expressions with void type, since
printing 'Value: ()' for them would just be distracting (the output shown above
is instead printed as a consequence of evaluating the 'print_block' function,
but it is not accessible for subsequent manipulation in atlas).

Functions defined by this syntax are overloaded, and stored in a different
table than variables of non-function type introduced by 'set var = ...'; this
means an overloaded function can coexist with a value of the same name. This
other table, called overload table, can store multiple definitions for the
same function name. So after the above definition one could continue with::

  atlas> set f(int n)=n+1
  Added definition [2] of f: (int->int)
  atlas> [f(4),f(f(6))]
  Value: [5,8]
  atlas> f("A1")
  0(0,1):  0  0  [i1]  1   (2,*)   e
  1(1,1):  0  0  [i1]  0   (2,*)   e
  2(2,0):  1  1  [r1]  2   (0,1)   1

Note how the response after the second 'set f' mentions the addition of a
definition and the total number [2] of definitions for 'f' now known. When
encountering a call of 'f', axis finds out which definition to apply based
on the type of the argument (list). All functions (and operators) built into
atlas are defined in the overload table, often with more than one initial
definition for a given name. The user can add definitions to names that
also refer to built-in functions, they will be overloaded together with the
original definitions. If one wishes that 'inner_class' can be called with a
single 'ratvec' to specify kernel generators, it suffices to write::

  atlas> set inner_class (LieType lt,ratvec gen,string ict) =
  = > inner_class(lt,[gen],ict)
  Added definition [7] of inner_class: (LieType,ratvec,string->InnerClass)

to add a new overloaded meaning to the 'inner_class' function. The fact that
this definitions itself calls another (built-in) version of 'inner_class' is
all right, because it can be distinguished by the argument type.

(As an aside, this call could not possibly be taken to be a recursive call,
even if the types would have matched, since the 'set' definition is only taken
into account after the body has been analyzed and found correct; the
definition is therefore unknown during the analysis of its own body.)

New meanings of operator symbols can also be defined in this way. So while
many versions of arithmetic operations are built into atlas, the standard
script 'basic.at' defines a lot more instances yet, such as scalar
multiplication of matrices, for which gives a definition that is basically::

  set * (int c,mat m) = mat: for column in m do for x in column do c*x od od

(the somewhat curious syntax of the 'for' loop will be explained below).

Distinction between operators and functions occurs mostly in use rather than
at their definition: as opposed to functions, operators can be used infix
(when they take exactly two arguments) or prefix (always), and without always
needing parentheses around their arguments. There are some limitations for
defining operators: one cannot introduce new operator symbols, nor change the
precedence rules for the existing symbols, and operator definitions cannot be
local (within 'let'). The last point is because operator definitions always
add to the overload table, and there is no such thing as local overloads:
defining a local identifier as a function instead temporarily hides any
existing overloads of that name for the duration of that local definition.
