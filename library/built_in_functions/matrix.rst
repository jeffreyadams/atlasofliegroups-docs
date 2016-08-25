Matrix Manipulating Functions
-------------------------------

.. list-table::
   :widths: 10 20
   :header-rows: 1
   
   * - Function
     - Argument(s) -> Result(s)
   * - :ref:`id_mat`
     - ``(int->mat)``
   * - :ref:`diagonal`
     - ``(vec->mat)``
   * - :ref:`swiss_matrix_knife`
     - ``(int,mat,int,int,int,int->mat)``
   * - :ref:`echelon`
     - ``(mat->mat,[int])``
   * - :ref:`diagonalize`
     - ``(mat->vec,mat,mat)``
   * - :ref:`adapted_basis`
     - ``(mat->mat,vec)``
   * - :ref:`kernel`
     - ``(mat->mat)``
   * - :ref:`eigen_lattice`
     - ``(mat,int->mat)``
   * - :ref:`row_saturate`
     - ``(mat->mat)``
   * - :ref:`inv_fact`
     - ``(mat->vec)``
   * - :ref:`Smith_basis`
     - ``(mat->mat)``
   * - :ref:`Smith`
     - ``(mat->mat,vec)``
   * - :ref:`invert`
     - ``(mat->mat,int)``
   * - :ref:`mod2_section`
     - ``(mat->mat)``
   * - :ref:`subspace_normal`
     - ``(mat->mat,mat,mat,[int])``

.. _id_mat:

id_mat
+++++++

    ``(int->mat)``: identity matrix of given size.

.. _diagonal:

diagonal
+++++++++

    ``(vec->mat)``: square diagonal matrix with given diagonal entries.

.. _swiss_matrix_knife:

swiss_matix_knife
++++++++++++++++++

    ``(int,mat,int,int,int,int->mat)``: slice and dice a matrix. 
    
    This function selects a block from a matrix, and depending on the options in its first argument can apply a number of transformations on the fly. The basic call ``swiss_matrix_knife(0,A,i,k,j,l)`` returns the block ``A[i:k,j:l]`` (and is in fact used behind the scenes to implement that syntax). The first (integer) argument specifies 8 options (its value is taken modulo 2^8=256) as follows. Bits 0,1,2 modify row indexing: setting bit 0 reverses the rows before selecting, and bits 1,2 when set specify that i respectively k count from the end (they are subtracted from the number of rows before being used). Similarly bits 3,4,5 modify column indexing. Bit 6 when set specifies that the resulting block is transposed, and bit 7 when set indicates that all entries of the resulting matrix are negated (they are multiplied by -1).

.. _echelon:

echelon
++++++++

    ``(mat->mat,[int])``: make column echelon form, and return pivots as well. 
    
    This applies column operations, and possibly removal of null columns; the number of remaining columns is the rank. The result is a pair ``(M,s)`` with s increasing sequence, and ``M[i,j]`` is nonzero for ``i=s[j]`` and zero for ``i>s[j]``.
    
.. _diagonalize:

diagonalize
++++++++++++

    ``(mat->vec,mat,mat)``: partial Smith reduction, without divisibility.
    
    Applies row and column operations to the matrix to obtain diagonal form; returns the list of non-zero diagonal entries (all except the first are assured to be positive), and the pair of determinant 1 integral matrices that have been applied to left and right respectively.
    
.. _adapted_basis:

adapted_basis
++++++++++++++++

    ``(mat->mat,vec)``: find basis whose integer multiples span image.
    
    Returns for ``M`` a pair ``(B,c)`` of a basis (columns of ``B``) and matching list ``c`` of
    positive integers, such that the column span of ``M`` is the same as the span of
    the multiples ``c_j*B_j`` of the columns ``B_j`` of the matrix ``B`` by the scalars ``c_j``.
    
.. _kernel:

kernel
+++++++++

    ``(mat->mat)``: find matrix whose columns span kernel of the given matrix.

.. _eigen_lattice:

eigen_lattice
+++++++++++++++++

    ``(mat,int->mat)``: eigen-lattice of matrix (at integer eigenvalue).
    
    ``eigen_lattice(M,lambda)`` = ``kernel(M-lambda*id_mat(n))``, where ``#M=(n,n)``.

.. _row_saturate:

row_saturate
+++++++++++++

    ``(mat->mat)``: keep same kernel, but row-span saturated sublattice
    
    Interpreting rows of the matrix as linear forms, this transforms the system into an equivalent one, and whose Z-linear map is made to be surjective. In other words, the rows are made linearly independent, and the sublattice they generate saturated: if an integer multiple of v is in it, then so is v.

.. _inv_fact:

inv_fact
+++++++++++

    ``(mat->vec)``: invariant factors in Smith normal form (no zeros).

.. _Smith_basis:

Smith_basis
++++++++++++

    ``(mat->mat)``: a basis on which the Smith normal form is assumed.

.. _Smith:

Smith
++++++++++

    ``(mat->mat,vec)``: ``Smith(M)`` = ``( Smith_basis(M), inv_fact(M) )`` (almost). ``Smith(M)`` describes explicitly the sublattice spanned by the columns of M. The first component is an invertible matrix, whose columns, multiplied by the corresponding entries of the second component, span that sublattice. ``inv_fact(M)`` is the list of the invariant factors of M, which are like the second component of ``adpted_basis(M)``, but with additional requirement that each entry divides the next; this may involve using a different basis. Smith_basis(M) is that basis corresponding to ``inv_fact(M)``, an invertible (over Z) square matrix equal in height to M, whose columns, each multiplied by the corresponding invariant factor (or 0), span the same as those of M.

.. _invert:

invert
+++++++

    ``(mat->mat,int)``: ``invert(M)`` produces ``(inv, d)`` such that :math:`M \cdot inv=d \cdot Id`, with d minimal.

    The inverse matrix, represented as an integral numerator matrix inv, and a minimal positive common denominator d. Note: d does not mean determinant. 

.. _mod2_section:

mod2_section
+++++++++++++++

    ``(mat->mat)``: find section (left/right/inverse) of binary matrix

    The argument is reduced modulo 2 to a matrix A over :math:`\mathbb{Z}/2\mathbb{Z}`; it returns a matrix :math:`B` such that :math:`ABA=A` and :math:`BAB=B`; it will be an inverse/left inverse/right inverse of (over :math:`\mathbb{Z}/2\mathbb{Z}`) whenever :math:`A` is bijective/surjective/injective.


.. _subspace_normal:

subspace_normal
+++++++++++++++++

    ``(mat->mat,mat,mat,[int])``: normalized modulo-2 basis.


    Given a sequence of binary vectors, namely the reduction modulo 2 of the columns of the argument matrix, find a normalized basis for the subspace they span (a matrix in reduced column echelon form without zero columns), and also expressions for the basis vectors in terms of the given list, a basis for the relations between the vectors, and a list of pivot values (each list given as a matrix with the specified vectors as its columns). The argument is a list of n generators of size r whose components are interpreted modulo 2, the first output component is a reduced echelon basis, consisting of d binary vectors of size r where d is the dimension of the subspace, the next component has d binary vectors of size n, giving the combination of generators that produced this basis vector, the next component has n-d binary vectors of size n, each giving basis of the linear dependency relations among the generators, and the final component is an increasing sequence of nonnegative d integers less than r giving the pivot positions, the first nonzero positions in each of the basis vectors.
