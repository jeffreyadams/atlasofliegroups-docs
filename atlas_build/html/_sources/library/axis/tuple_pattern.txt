Tuple Displays and Pattern Matching
========================================


If instead of brackets of a row display one uses parentheses to enclose a
sequence of expressions, then a tuple rather than an array is formed (except
in case there is exactly one expression in the sequence: then parentheses just
imply grouping as used for instance to override operator precedence). Tuples
differs from array in that there elements are not required to have the same
type, and (therefore) cannot be selected by position. In fact the type of a
tuples expression explicitly specifies the type of the component at each
position, and since the type checker insists that all expressions have a type,
it is not possible to work with a tuple not having a fixed number of
components (unlike arrays, which can well be of varying length). Tuple
displays are frequently used to pack the arguments of a function (officially
every function takes a single argument, but very often it is of tuple type).
So for instance 'f(x,y)' applies the function 'f' to a 2-tuple with components
'x' and 'y'. But one is not obliged to write a tuple display as argument of a
function expecting a tuple; for instance after 'set z=(3,4)' the variable 'z'
holds a 2-tuple, and (the same instance of) 'f' may also be called as 'f(z)'.
One could even for instance multiply the components of 'z' by writing ``*z``
(giving 12 in the example); indeed the expression ``3*4`` is transformed by the
parser into ``*(3,4)``, and (currently) this form is also used in error
messages, for instance in::

  atlas> GL(10/2)
  Error in expression GL(/(10,2)) at <standard input>:...
    Failed to match 'GL' with argument type rat
  Type check failed

(The operator '/' on integers produces a rational number; for integer division
ignoring the remainder one should write 10\\2 instead).

To decompose tuples, a simple form of pattern matching is provided: wherever
an identifier can be introduced, one may also specify a tuple of identifiers,
if the type of the value is appropriate, and the components will be bound to
the corresponding identifiers. So whereas::

    atlas> set x = E

introduces the identifier 'x' whose value (and type) are set to that of the
expression 'E', one can alternatively say 

.. code-block:: none

    atlas> set (x,y) = E
    
provided that E produces a pair (some value of some 2-tuple type), and the
variable 'x' will be set to the first component of the pair, and 'y' to the
second component. In either case, the types of the variables introduced will
be reported, as in::

  atlas> set (q,r) = 22 \% 7   { Euclidean division with remainder }
  Identifiers q: int, r: int
  atlas> q    { quotient }
  Value: 3
  atlas> r    { remainder }
  Value: 1

The same pattern-matching is also allowed when introducing parameters of
user-defined functions, or when introducing local variables. To introduce
local variables one uses a syntax like that of 'set' used above, but with
'let' instead of 'set', and followed by 'in' and the "body" if the
let-expression, the expression where the local variable is in scope. So to
compute a value from the components of 'z', one could say:

.. code-block:: none

    atlas> let (x,y) = z in 3*y-x

If only the first component is needed, there is no need to give a name to the
other one, so for the projection to the first component one can write:

.. code-block:: none

    atlas> let (x,)=z in x

Local variables get their value and type from the expression between '=' and
'in', and are independent of any meaning that might previously be associated
to the identifier; after evaluation of the body, the local identifiers
introduced, and their values associated to them, are forgotten. (One can no
longer refer to the local name outside the expression following 'in'; in some
cases references to them made from inside that expression may survive though.)

Using a local variable, the initial example could have been given in a form
that does not permanently bind the identifier 'ic'::

  atlas> let ic = inner_class("B5.A3.T1",[[1/2,0,0],[0,1/2,1/2]],"scc")
  L > in block_sizes(ic)
  Value:
  | 0,  0,   0,  0,   0,    0,    0,     1 |
  | 0,  0,   0,  0,   0,    0,    0,    11 |
  | 0,  0,   0,  0,   0,    0,    0,    10 |
  | 0,  0,   0,  0,   0,    0,    0,    75 |
  | 0,  0,   0,  0,   0,    0,    0,   110 |
  | 0,  0,   0,  0,   0,    0,    3,    21 |
  | 0,  0,   0,  0,   0,    0,    0,   305 |
  | 0,  0,   0,  0,   0,    0,    0,   750 |
  | 0,  0,   0,  0,   0,    0,   33,   231 |
  | 0,  0,   0,  0,   0,    0,    0,   810 |
  | 0,  0,   0,  0,   0,    0,    0,  3050 |
  | 0,  0,   0,  0,   0,    0,  225,  1575 |
  | 0,  0,   0,  1,  25,  130,    0,  1342 |
  | 0,  0,   0,  0,   0,    0,    0,  8100 |
  | 0,  0,   0,  0,   0,    0,  915,  6405 |
  | 0,  0,   0, 10, 250, 1300,    0, 13420 |
  | 0,  0,   0,  0,   0,    0, 2430, 17010 |
  | 3, 75, 390, 21, 525, 2730, 4026, 28182 |

Note that axis recognized that the let-expression was incomplete after the
first line, changing the prompt to 'L >' in the second line to indicate this.
