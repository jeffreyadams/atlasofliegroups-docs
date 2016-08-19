.. _control_struc:

Control Structures
====================

As control structures, the axis language currently provides sequenced
expressions, conditional and case expressions and various kinds of loops. Each
of them optionally deliver values (which is somewhat unusual in the case of
loops), though they can also serve more conventionally for selecting/iterating
actions.

Sequenced expressions
---------------------------

Sequenced expressions are simply sequences of expressions separated by
semicolons; together they form a new expression, whose evaluation consists of
the successive evaluation of the component expressions from left to right, and
whose value is taken to be that of the final component expression evaluated.
The values of the other expressions (if any) are ignored; we say they are
voided. Voiding is like an implicit conversion to a $0$-tuple '()' that can be
applied to values of all (non-void) types. In particular voiding is recorded
in the expression after type analysis, and the evaluator uses this information
to suppress the construction of any (components of) values that are destined
to be immediately voided, evaluating in those cases only for side effects;
this can be particularly relevant for the values of function calls and loops.

One might consider ';' as an associative operator with very low precedence
(lower than assignment, and on the same level as 'let': if the final operand
starts with 'let' it need not be parenthesized) that evaluates its operands in
order and returns the value of the rightmost one. Occasionally useful
(especially in loops) is its variant written as the keyword 'next', that also
evaluates its operands (usually just two of them) from left to right, but
returns the value of the leftmost one. Thus in 'e1; e2; e3 next e4' all
expressions are evaluated in order, and the value of 'e3' is returned. Both
forms have the same precedence and associate to the right (as 'let' requires
them to), which implies that in cases like 'e1; e2 next e3; e4 next e5', the
value will be that of the expression before the first 'next' (i.e., 'e2');
clearly such multiple use of 'next' is rather pointless.

Being at the same precedence level means that the scope of a 'let' is not
terminated by a following semicolon: in 'let x=3 in x:=2*x; x+3' the final 'x'
is still in scope. On the other hand expression with a semicolon always need
parentheses when used as operands. They do not need them in function
arguments, as there the parentheses and commas provide sufficient grouping; so
'f(x;y,z)' is OK though maybe more readable when written as '(x;f(y,z))'. Such
usage is rare, but the same goes for control structures like conditionals and
loops: these all provide their own closing symbols, so that semicolons can be
freely used inside those. Whether or not necessary, it can be useful to group
large sequences of expressions separated by semicolon with the keywords
'begin' and 'end', as a more readable equivalent alternative to parentheses.

Conditional expressions and case expressions
-----------------------------------------------

Conditional expressions take the form::

    if ... then ... else ... fi

for a simple 2-way branch, or a more elaborate multi-way branch::

    if   ... then ...
    elif ... then ...
    elif ... then ...
    ...
    else ...
    fi

The else branch may be omitted, the implied branch then being void: 'else ()'.

If the selection is determined by an integral expression 'I' with values in the
range 0,1,...,n-1 (for instance the result of a reduction modulo n), then the
multi-way branching is better done using a case-expressions, of the form::

    case I
    in E_0
    , E_1
    , ...
    , E_{n-1}
    esac

In the conditional expression, the branches after 'then' and 'else' should all
have the same type that will become the type of the conditional expression, or
they should be implicitly convertible to a common type. Type analysis tries to
cleverly guess that common type, and in particular if any of the branches has
void type, then all non-void branches will be voided (any value is ignored).
Should axis fail to guess the intended type (with type analysis reporting
"Could not find common type for branches"), then one can always make the type
desired (possibly void) explicit, by casting the whole conditional expression
to it. Casting 'T: if .. then E0 elif .. then E1 else E2 fi' is equivalent to
casting all branches: if .. then T:E0 elif .. then T:E1 else T:e2 fi'.

The conditions (after 'if' or 'elif') must be expressions of type 'bool'. For
such expressions one can use logical connectives 'or', 'and' and 'not'. These
behave like operators with precedences just above that of assignment (and
increasing in the order given); they are however handled in the parser, which
will for instance transform 'x and y' into 'if x then y else false fi'. In
particular 'or' and 'and' short-circuit: they only evaluate their second
operand if the first operand is not decisive. The user cannot redefine or
overload these operators. Usage of 'not' in conditions has no runtime cost, as
axis will rewrite internally to an equivalent expression without 'not'.

Loops
-------------

While loops
+++++++++++++

Loops come in various flavors, each one returning a row value with one
component for each iteration of the loop (however for loops in voided context,
no result is constructed). There are simple while loops::

    while ... do ... od

with as usual a continuation condition after 'while'. This condition is
evaluated before each iteration, but if some action must be performed each
time before the condition is tested, it suffices to use a sequenced expression
as condition. The other expression is the loop body; it is evaluated as long
as the condition evaluated to 'true', and the values (all of the same type) of
the evaluations of the loop body for, in order, the components of the row
value returned by the loop. Obviously evaluating the loop body (or maybe of the
condition itself) must potentially involve a a side effect susceptible of
changing the loop condition, if the loop is ever to terminate. So the loop in::

    let i=0 in while i<=n do i+:=1 od

will produce a row [1,2,...,n]. Often the side effect is required to
take place after a component to the row result is contributed; to that end and
expression sequenced by 'next' can be used. So for instance the variation::

    let i=0 in while i<=n do i next i+:=i od

produces the row [0,1,...,n-1].

Counted for loops
+++++++++++++++++++++

The remaining loops are 'for' loops, which determine the number of iterations
at the beginning rather than dynamically. Their syntax is somewhat unusual, in
that it does not specify the starting and ending values of the iteration, but
rather the number of iterations and the smallest index (which may be the first
or the last one, depending on the sense of the loop); this appears to be less
conducive to producing off-by-one errors. Thus an iteration from 0 to n-1 is
specified as n iterations with lowest index 0, an iteration from 1 to n as n
iterations with lowest index 1, and an iteration from n-1 to 0 as n downwards
iterations with lowest index 0. More specifically, one specifies (in this
order) the number of iterations, the direction (increasing or decreasing) and
the lower bound of the range (only unit steps are supported, and a negative
iteration count is interpreted as no iterations). The iteration count is
preceded by ':', the direction by the keyword 'from' (increasing) or 'downto'
(decreasing), and the lower bound follows. In the common case of increasing
iteration starting at 0, the part 'from 0' may be omitted. So::

    for i : n from 0 do i od

is an alternative way to produce [0,1,...,n-1], and it may be abbreviated::

    for i : n do i od .

To obtain a more traditional range [1,2,...,n], one may say::

    for i : n from 1 do i od .

For the reverse list [n-1,...,1,0] use '~' as in::

    for i : n ~ do i od

and the shifted reversed list [n,...,1] is produced by::

    for i : n from 1 ~ do i od

(This used to be written as 'for i : n downto 1 do i od', but this syntax is
redundant given the new more flexible tilde syntax, and is now deprecated.)

If something is just to be repeated n times, the loop index can be omitted::

    for :n do 1 od { generate a list of n ones }

Iteration over composite values
++++++++++++++++++++++++++++++++++

Rather than counted iteration, it is often convenient to use iteration over an
existing composite value. If V is a row value, or vector, rational vector
string or matrix then::

    for e in V do ... od

iterates over the components of V (for a string these components are
one-character strings; for a matrix they are its columns), setting e to such a
component before evaluating the loop body. For instance, one can produce the
scalar multiple by 3 of a vector V using::

    vec: for e in V do 3*e od

(the 'vec:' serves to assemble the entries in a vector rather than a list).
In some cases it is useful to know the index of the component taken as well
inside the loop body, in other words the iteration count starting from 0; this
can be accessed by writing '@ index' before 'in' where 'index' is an
identifier used to bind the index to, This explains the vector addition above::

    set +(vec v,vec w) = vec: for vi@i in v do vi+w[i] od

where the index i is needed to select the corresponding entry from the other
vector. These value-returning loops are quite flexible, for instance::

    mat: for j = n do for i = m do if i=j then 1 else 0 fi od od

produces an m*n matrix with unit diagonal entries and zeroes elsewhere. Of
course the case m=n of the identity matrix is most common, be we allowed
distinct values of m and n to stress that the column-oriented conventions
force the outer loop to be over the columns and the inner loop to be over the
rows. (In this case the relevant convention is not one associated to the loops
themselves, but the one for the implicit conversion of a row of integer lists
to a value of type 'mat'; but all these conventions are "column-oriented" for
compatibility.) To add such a matrix to an existing matrix M it suffices to
write (with again columns being traversed in the outer loop and rows in the
inner loop)::

    for col@j in M do for entry@i in col do entry+if i=j then 1 else 0 fi od od

By the way the standard definitions in basic.at allow replacing the expression
'if i=j then 1 else 0 fi' by '#(i=j)', a axis version of the Iverson symbol.

These for loops can iterate over every kind of composite value that allows
subscription (but although one can obtain matrix _entries_ directly by
subscription, one cannot directly iterate over them; this requires two nested
loops as the last example above illustrates). Thus one can loop over
characters in a string (which for lack of a character type are turned into
single-character strings), entries of a rational vector.

One can also loop over the (nonzero) terms of a 'ParamPol' value, which is
convenient though somewhat special. One should think of a 'ParamPol' not as a
list of terms (there is no absolute meaning to the order in which terms are
presented) but as an association of coefficients (of type 'Split') to values
of type 'Param' (which values have been made standard, nonzero, and final in
order for the association to be mathematically meaningful; they also have
their infinitesimal character representative made dominant so that terms with
equivalent Param values will combine). This is reflected by allowing the
coefficient associated in the ParamPol 'pol' to the Param value 'p' to be
written as 'pol[p]'. Then iterating over a 'pol', a term with Param 'p' and
coefficient 'c' is presented as a component 'c' stored at index 'p'. Therefore
a loop over such terms will take the form::

    for c@p in pol do ... od

During execution, each time 'c' will be a nonzero 'Split' coefficient, and 'p'
the corresponding (standard final nonzero dominant) 'Param' value. The order
of traversal of the terms in the loop is determined by an ordering of 'Param'
values that is fixed by atlas but not easy to fully describe; however in most
cases it ought not matter much. (This does imply that the value of this loop,
in which the values of the loop bodies have been ordered by traversal order,
is only rarely useful; it could be for instance if the values are then passed
through a commutative operation, or are being sorted afterwards.) For the
opposite operation of combining a collection of '(Split,Param)' values
(possibly generated by a loop) into a 'ParamPol' value, a built-in instance of
'+' is provided. The collection is given as a row forming the right operand of
'+', while the left operand is an initial 'ParamPol' to which the terms are to
be added; often this will take the form 'null_module(rf)+for ... od'.

Reversal variants in loops
++++++++++++++++++++++++++++

As a general rule, if 'do' in a for loop is preceded by a tilde, then the
iteration will be performed on the same set of values as before, but traversed
in the opposite order. If a row is produced as value of the loop, it will
still be the values of the loop bodies in the order of traversal. However
preceding the final 'od' be a tilde assembles the values of the loop bodies in
the order opposite to iteration. The two variants can be combined (traversing
backwards, but assembling the result in the original increasing order), and
apply also to versions of 'for' loops given below (the second variant also
applies to 'while' loops; not the first variant, which is meaningless there).

Like for the while loop, the body may be a sequence expression, and it may
have side effects. However, assignments to the variables introduced in the
loop (index and/or value of iteration) are forbidden. This is so because it
would usually mask an error: once the heading of a loop is processed, there is
no way to alter the number of iterations (in particular the expressions for
bounds or array iterated over are evaluated just once), and assignment to the
loop index suggests that the user tries to do so anyway. (In rare cases where
one really needs a modified version of an iteration value, copy it to a local
variable and modify that.) In fact the loop variables are distinct for each
iteration: if one captures them in functions, each one stays at its initial
value; so to create a list of functions that add respectively 1,3,6, doing::

    functions := for x in [1,3,6] do (int n): n+x od

has the desired effect (functions[1] adds 3, not the "final value" 6 of 'x').

