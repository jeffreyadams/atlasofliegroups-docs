.. _implicit_conversion:

Implicit Conversions
=========================

When types do not match exactly, axis will sometimes insert implicit type
conversions that are ac	companied by conversions of the corresponding values.
For instance, although the 'vec' type, which functions of the Atlas library
use, models the same values as '[int]' (pronounced "row of int"; this is the
general row-of construction applied for component type int), the two types
have different internal representations (that of 'vec' is a bit more compact).
The row display syntax will always produce a value of row-of type, so it can
only be used to produce a '[int]' value. What makes it nevertheless possible
to provide 'vec' values to functions that need it is the fact that atlas will
convert between '[int]' and 'vec' when the context that require this. In
particular one can write a row display as argument to a function in a position
that takes a 'vec' value. Inversely where a '[int]' value is required, a
function call returning 'vec' will be accepted, and its result converted.

Not all conversions are bidirectional; in some cases like conversion of
integers into rational numbers no conversion in the opposite direction is
provided. One could take the integer part (floor) of a rational number, but
since this is not the only reasonable option, the call of an explicit function
will be required for this conversion. Since the user has no control over
implicit conversions (neither the set of such conversions, nor the details of
each conversion), they only have been defined in cases where there appears to
be no doubt about the natural (injective) way to map one type to the other.
For similar reasons implicit conversions are defined conservatively: when for
certain values there is no obvious conversion, an error is produced rather than
making a guess about the desired value; the user who wishes more liberal
treatment is invited to write and use an explicit conversion that defines it.
For instance an implicit conversion from '[vec]' to 'mat' is provided (it is
essential for entering matrix values); a choice is built into atlas that the
vectors will become columns (rather than rows) of the matrix, but the
conversion will produce an error when applied to vectors of different lengths
(rather than padding in some way), and also when applied to an empty row of
vectors (since there is no way to know the number of rows that the resulting
empty matrix should have). The latter point causes this implicit conversion to
often be the wrong choice in programming situations where a row of vectors all
of known size (but possibly without any vectors at all) needs to be converted
into a matrix; a built-in operator '#' of signature '(int,[vec]->mat)' is
provided that allows explicitly specifying the size of the vectors, and thus
producing a correct result even when the row of vectors is empty.

Here is a list of all implicit type conversions::

  vec       <-> [int]
  mat       <-> [vec]    (vectors are columns of the matrix)
  mat       <-> [[int]]  (inner arrays are columns of the matrix)
  int        -> rat      (denominator 1)
  ratvec    <-> [rat]    (ratvec has least common denominator)
  vec        -> ratvec   (denominator 1)
  [int]      -> ratvec
  int	     -> Split
  string     -> LieType  (applies Lie_type function)
  InnerClass -> RootDatum
  RealForm   -> InnerClass
  RealForm   -> RootDatum
  Param	     -> ParamPol (parameter is converted to final parameter(s) first)

At most one implicit conversion is applied to a given subexpression, so there
is for instance no implicit conversion from '[int]' to '[rat]' passing through
the intermediate type 'ratvec'; should this chain of implicit conversions be
desired, writing a cast 'ratvec:' will allow it (the first conversion no being
inside the cast, the second applied to the result of the cast).

The one-directional conversions int->rat and string->LieType are mainly a
convenience to users, as these conversion could be written out explicitly::

  atlas> 3+1/7       { same as 3/1+1/7 }
  Value: 22/7
  atlas> Cartan_matrix("E8")  { same as Cartan_matrix(LieType("E8")) }
  Value:
  |  2,  0, -1,  0,  0,  0,  0,  0 |
  |  0,  2,  0, -1,  0,  0,  0,  0 |
  | -1,  0,  2, -1,  0,  0,  0,  0 |
  |  0, -1, -1,  2, -1,  0,  0,  0 |
  |  0,  0,  0, -1,  2, -1,  0,  0 |
  |  0,  0,  0,  0, -1,  2, -1,  0 |
  |  0,  0,  0,  0,  0, -1,  2, -1 |
  |  0,  0,  0,  0,  0,  0, -1,  2 |

If desired, a context requiring a given type can be created by a cast: writing
the desired type name followed by a colon and the expression. So while one
(currently, this may change in the future) gets an error for::

  atlas> [1,1/2,1/3,1/4]
  Error during analysis of expression at <standard input>:...
  Type error:
    Subexpression /(1,2) at <standard input>:...
    has wrong type: found rat while int was needed.
  Type check failed

this can be repaired by asking for a list of 'rat'::

  atlas> [rat]: [1,1/2,1/3,1/4]
  Value: [1/1,1/2,1/3,1/4]

Alternatively this input could be turned into a 'ratvec'::

  atlas> ratvec: [1,1/2,1/3,1/4]
  Value: [ 12,  6,  4,  3 ]/12

Note that here in addition to the conversion of the initial '1' from integer
to rational, a conversion of the row from '[rat]' to 'ratvec' is inserted.

This conversion is applied whenever a list of rationals (or integers) is given
in place of a 'ratvec'; for instance inner_class takes a list of 'ratvec'
values as second "kernel generators" argument, and they can be specified as::

  atlas> inner_class ("D4.A3",[ratvec]:[[0,1/2,1/4],[0,0,1/2]],"ss")
  Value: Complex reductive group of type D4.A3, with involution defining
  inner class of type 'cs', with 10 real forms and 15 dual real forms

Note that the cast '[ratvec]:' to a row of rational vectors is needed because
(1) the call to 'inner_class' is overloaded, so atlas cannot know beforehand
that the second argument is of type '[ratvec]', and (2) in isolation the row
display '[[0,1/2,1/4],[0,0,1/2]]' would give a type error, similarly to the
example just above. But once the cast is written, atlas knows that each of
the two sub-displays in the row display must have type 'ratvec', so it is not
necessary to separately cast those, or to cast the constants '0' to 'rat'.

In this call there could be one kernel generator, '[ratvec]:[[0,1/2,1/4]]', or
none at all 'ratvec:[]' (for an empty row argument a cast is always necessary
in order to resolve overloading). However 'ratvec:[0,1/2,1/4]' will not be
accepted, since a row of rational vectors is required, and atlas will not
turn a single value into a singleton row automatically. (One could on the
other hand admit such an argument by defining an additional overload of
'inner_class' that accepts a single 'ratvec' and builds a singleton row from
it with which it then calls the built-in version of 'inner_class'.)

Matrices can be built from lists of columns by requiring type 'mat'::

  atlas> mat: [[1,2,4],[3,5,7]]
  Value:
  | 1, 3 |
  | 2, 5 |
  | 4, 7 |

Each list of integers giving a column is in fact first converted to a vector,
and one could also use a vector-valued expression in its place (for instance
an identifier bound to a vector value).

For specifying a matrix by rows, a special syntax is provided::

  atlas> [ 1,2,4 | 3,5,7 | 0,-1,6 ]
  Value:
  | 1,  2, 4 |
  | 3,  5, 7 |
  | 0, -1, 6 |

Note that 'mat:' is not required here, the syntax itself forces a matrix
result. On the other hand it will not accept 'vec' values as lines; to
construct a matrix from its row vectors, write '^[r_0,r_1,...]', where '^' is
a prefix operator indicating matrix transposition. Here the argument is
implicitly converted from '[vec]' to 'mat', illustrating that although
overloaded calls (here of the operator '^') do not impose any type on their
argument, they do match when an argument is found with a type (here '[vec]')
sufficiently close to one (here 'mat') for which an overload is defined. In
case the list of rows is given by an expression other than a row display, and
it could return an empty list, it is better to write 'n^rows' rather than
just '^rows', where 'n' is the constant size of the rows, as it then returns
an n times 0 empty matrix rather than an error when 'rows' is an empty list.

