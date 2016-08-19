Array 
===============

Array Displays
------------------

Array values can be constructed by enclosing a comma-separated lists of
component expressions (all of the same type) in brackets, as in ``[1,-4,3*6]``,
which is called a **row display** (the given one will be printed as ``[1,-4,18]``).
They are also implicitly constructed by :ref:`loops <control_struc>`.

Array Selection
------------------

If 'v' is an identifier, or more generally an expression, whose value is an
array, then the individual components can of the array can be accessed by
subscripting, as in 'v[i]'. Interpretation of the index always starts from 0:
the first element of v is v[0], and the last is v[#v-1]. However, one can also
index counting from the end by prefixing the '[' by '~', so the last element
is also v~[0], and the before-last v~[1] and so on.

Array Slicing
------------------

One can also select
multiple elements at once (combined into a new array value) using a "slice",
specifying the a lower and an upper bound separated by ':'. Each should be
thought of as indicating a separation between two elements, namely between the
one at the given index and at an index one less; the slice then selects all
elements between the lower separator and the upper separator. This means that
in a v[a:b] includes the element v[a] but excludes v[b], and therefore selects
b-a elements in all. In case a>=b the slice returns an empty array of the same
type as v (having a=b is normal, having a>b is allowed but rarely useful). It
is an error if the lower bound is negative, or if the upper bound exceeds the
size of the array. Individual bounds in a range can also be counted from the
end by appending a '~', in which case they indicate the separation after (that
is, closer to the end) then the element the index would reversely select. As a
convenience a completely omitted lower bound means 0 (from the beginning) and
an omitted upper bound means 0~ (up to the end). Finally one can (like for
subscription) select from the reverses array by prefixing the '[' by '~'.

Here are some examples of various uses of slices

.. list-table::
   :widths: 12 40
   :header-rows: 1

   * - Expression
     - Effect
   * - v[0:3]  or v[:3]
     - the first 3 elements of v
   * - v[3:0~] or v[3:]
     - everything except the first 3 elements of v
   * - v[2~:0~] or v[2~:]
     - the last 2 elements of v
   * - v[0:2~]  or v[:2~]
     - everything except the last 2 elements of v
   * - v[i:k]
     - the elements [v[i],v[i+1],...,v[k-1]
   * - v[i:k~]
     - all of v except its first i and its last k elements
   * - v~[0:0~] or v~[:]
     - all of v in reverse order
   * - v~[4:0~] or v~[4:]
     - all of v except the last 4 elements, in reverse order
   * - v~[0:5~] or v~[:5~]
     - all of v except the first 5 elements, in reverse order
   * - v~[i:k]
     - the k-i elements [v[n-1-i],...,v[n-k-1],v[n-k]] (n=#v)
   * - v~[k~:i~]
     - the k-i elements [v[k-1],...,v[i+1],v[i]]

  
Other Array-Like Types
------------------------

While vectors, rational vectors, matrices and strings are not axis arrays
(they are instead members of primitive types), they do behave like arrays for
the purpose of selection; the result is respectively an integer, rational
number, vector (column of the matrix) or a one-character string (the selection
can also cause an error, if the index is out of bounds). They can also be used
in slicing, in which case they return a value of the same type as what was
selected from. For instance "reverse me!"~[:] gives "!em esrever" and
id_mat(6)[1:2~] returns::

    | 0, 0, 0 |
    | 1, 0, 0 |
    | 0, 1, 0 |
    | 0, 0, 1 |
    | 0, 0, 0 |
    | 0, 0, 0 |

For individual entries of a matrix, one can provide row and column index at
once (in that order), separated by a comma as in A[i,j] (this actually indexes
A by a tuple of type (int,int), as in A[(i,j)]). One can apply reverse
indexing provided it applies to both indexes, as in A~[0,0] for the bottom
right entry. Slicing applies somewhat differently in case of matrices (unless
it involves a single integer range, in which case a range of columns is
selected). The general form is A[i:k,j:l] where each of the bounds i,k,j,l may
be followed by '~' (but not 'A'; this syntax allows no global reversal). This
selects a block of 'A' with the interpretation above for each of the ranges.
For more general slicing of matrices (with optional reversal of row and/or
columns, transposition, and negation of individual entries, atlas provides a
built-in function swiss_matrix_knife (the A[i:k,j:l] syntax in fact uses it).

Finally there is selection if ParamPol values, which can be seen as
associative arrays mapping certain Param values to Split coefficients, by
Param values used as index: for a ParamPol P and a Pram value q, the
subscription P[q] returns the coefficient of q in P (or Split:0 if no term q
is present). There is a technical restriction to this use due to the fact that
terms in ParamPol can only involve so-called standard parameters, and these
are automatically expanded to nonzero final parameters; therefore P[q] gives
an error unless q is standard, nonzero and final. There is no such thing as
reversal in associative arrays, so the syntax P~[q] is not allowed here.

