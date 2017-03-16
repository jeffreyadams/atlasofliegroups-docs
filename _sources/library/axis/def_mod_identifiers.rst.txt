Defining and Modifying Identifiers
=====================================

As shown in the examples above, global identifiers are introduced using 'set',
while local identifiers are introduced with 'let'. Local identifiers can be
used only in the expression after the following 'in', which may however be an
arbitrarily large composite expression or clause. Note that in both cases
the initial keyword is necessary; without it the '=' would be interpreted as
equality test (probably leading to an error due to an undefined left operand).

For modifying an existing variable, global or local, the assignment operator
':=' is provided. It is mainly intended for programming use rather than for
expression evaluation. For instance, a function returning a list of numbers
1,...,n may be written as follows (while-loops are explained later)::

  atlas> set initial (int n) = let i=0 in while i<n do i:=i+1 od
  Defined initial: (int->[int])

Here the part 'let i=0 in' serves to introduce 'i' as a variable, whose value
is then repeatedly modified by the assignment 'i:=i+1'. (The values from the
assignments in the successive iterations of the loop body are then gathered
into a row-of-integer value; a property of axis that is uncommon in other
languages.) Any identifier can be used as a variable, including one introduced
as a function argument; for instance for a decreasing list n-1,...,1,0 one
could write::

  atlas> set initial_downwards (int n) = while (n:=n-1)>=0 do n od
  Defined initial_downwards: (int->[int])

For identifiers holding an array, vector or matrix, one can also assign to
individual entries, as in 'v[i]:=x' or 'm[i,j]=i+j'; for matrices one can also
assign to a whole column, provided the vector that replaces it has the correct
size; for instance m[i]:=m[i]+m[j]*2 adds column j of m twice to its column i.

It is important to note that (unlike many programming languages) axis does
not distinguish between values and objects. In other words two different names
can never have any intimate relation (sharing an object) to each other, so
assigning to one name will have no effect on the value associated to the other
name. Therefore evaluating 'let vi=v[i] in vi:=3' does not have the same
effect as evaluating v[i]:=3, as this would suppose that assigning to vi
changes the (vector) value associated to v. Instead the value of the local
name vi is assigned to just before that name disappears, so there is no side
effect at all and the expression (it just returns 3), which then is rather
pointless. By the same token calling functions is conceptually strictly by
value (even if the implementation often avoids duplicating values); a function
is allowed to assign to the names of its arguments, but this has no effect for
the caller. For instance the assignment to its argument in the above function
'initial_downwards' does not have any affect for callers of this function, who
do not know about the identifier 'n' in 'initial_downwards', or of its use. To
pass information back from function to its caller, use the return value(s).

As a consequence of this principle, an assignment like v[i]:=x is really an
assignment to the name v; this value is replaced by a value differing only at
index i from the value it previously held.

(There is one way a function f can alter values of names of its caller g, but
this requires that f be defined as a local function inside the body of g. Now
f can, apart from its own parameters and local variables, can also "see" the
names of g that are accessible at the point where f is defined, and just like
any subexpression of the body of g, the body of f can assign to those names.)

In some cases it is desirable to introduce a name, but to forbid any form of
assignment to that name; for instance if the value of a global variable is
used inside a function, it can be important to ensure that the value obtained
is that at the time the function was defined. Such constant names can be
introduced by prefixing the name by '!', as in 'set !s = Split:(0,1)' (this
applies to local names as well as to global ones, and to function parameters,
and also to components of a pattern matching a tuple value). Names introduced
locally in loops (as described below) are automatically considered constant in
this sense, since assigning to them has little effect and is usually an error.

As a convenience one can write 'x +:= y' instead of 'x := x + y', and
similarly for any operator in the place of '+', so in the above examples one
could say i+:=1 and n-:=1. This is a transformation performed in the parser,
so '+:=' is not really an operator (and is composed of separate '+' and ':=').
It should be noted that this requires a simple variable as left operand: the
parser will reject for instance v[i]+:=1; this should be written v[i]:=v[i]+1.

The rules for assignment are quite different from the introduction of a
variable (by 'set' or 'let'): the variable must have been introduced
beforehand, and the value assigned must have the same type as the previously
held value. An assignment need not be used exclusively for the change to its
variable it causes; it is also a subexpression in its own right whose value is
the value assigned (both for ordinary and for component assignments); we
already used this fact in the examples above.