Lie Group Basics
--------------------

.. list-table::
   :widths: 10 20
   :header-rows: 1
   
   * - Function
     - Argument(s) -> Result(s)
   * - :ref:`Lie_type`
     - ``(string->LieType)``
   * - :ref:`Lie_type2`
     - ``(RootDatum->LieType)``
   * - :ref:`Cartan_matrix`
     - ``(LieType->mat)``
   * - :ref:`Cartan_matrix2`
     - ``(RootDatum->mat)``
   * - :ref:`Cartan_matrix_type`
     - ``(mat->LieType,vec)``
   * - :ref:`rank`
     - ``(LieType->int)``
   * - :ref:`semisimple_rank`
     - ``(LieType->int)``
   * - :ref:`operator_#`
     - ``(LieType->int)``
   * - :ref:`operator_%`
     - ``(LieType->[LieType])``
   * - :ref:`Smith_Cartan`
     - ``(LieType->mat,vec)``
   * - :ref:`filter_units`
     - ``(mat,vec->mat,vec)``
   * - :ref:`ann_mod`
     - ``(mat,int->mat)``
   * - :ref:`replace_gen`
     - ``((mat,vec),mat->mat)``
   * - :ref:`involution`
     - ``(LieType,string->mat)``
   * - :ref:`involution2`
     - ``(LieType,mat,string->mat)``
   * - :ref:`root_datum`
     - ``(mat,mat->RootDatum)``
   * - :ref:`root_datum2`
     - ``(LieType,mat->RootDatum)``
   * - :ref:`root_datum3`
     - ``(RootDatum,mat->RootDatum)``
   * - :ref:`root_datum4`
     - ``(InnerClass->RootDatum)``
   * - :ref:`quotient_basis`
     - ``(LieType,[ratvec]->mat)``
   * - :ref:`simply_connected`
     - ``(LieType->RootDatum)``
   * - :ref:`adjoint`
     - ``(LieType->RootDatum)``
   * - :ref:`dual`
     - ``(RootDatum->RootDatum)``
   * - :ref:`derived_info`
     - ``(RootDatum->RootDatum,mat)``
   * - :ref:`mod_central_torus_info`
     - ``(RootDatum->RootDatum,mat)``
   * - :ref:`rank2`
     - ``(RootDatum->int)``
   * - :ref:`semisimple_rank2`
     - ``(RootDatum->int)``



.. _Lie_type:

Lie_type
++++++++++

    ``(string->LieType)``: interpret string as Lie type.
    
    Factors are one of "ABCDEFGT" followed by a number; several factors can be concatenated in a string with optional punctuation. Must have total rank<=16.
    
.. _Lie_type2:

Lie_type
+++++++++

    ``(RootDatum->LieType)``: Lie type of a root datum.

.. _Cartan_matrix:

Cartan_matrix
++++++++++++++++
    
    ``(LieType->mat)``: Cartan matrix of Lie type (square of size rank).

    A block form Cartan matrix, with zeros in rows and columns of torus factors

.. _Cartan_matrix2:

Cartan_matrix
++++++++++++++

    ``(RootDatum->mat)``: Cartan matrix of root datum.

    This pairs roots and coroots, so it is square, of size the semisimple rank. By force of convention, rows correspond to roots and columns to coroots.


.. _Cartan_matrix_type:

Cartan_matrix_type
+++++++++++++++++++++

    ``(mat->LieType,vec)``: type given by Cartan matrix.

    The input should be a Cartan matrix for a semisimple type (no zero rows or columns). The function returns the semisimple type, and the permutation of mapping the standard (Bourbaki) ordering of the diagram of that type to the ordering of the corresponding simple roots in matrix rows and columns.

.. _rank:

rank
+++++

    ``(LieType->int)``: Rank of the weight lattice for this Lie type.

.. _semisimple_rank:

semisimple_rank
++++++++++++++++

    ``(LieType->int)``: Rank of the root lattice of this Lie type.

.. _operator_#:

\#
++++

    ``(LieType->int)``: Number of (simple or T1) factors in this Lie type

.. _operator_%:

\%
+++

    ``(LieType->[LieType])``: Expand into row of simple factors (or T1)

.. _Smith_Cartan:

Smith_Cartan
+++++++++++++
    
    ``(LieType->mat,vec)``: generators of weights modulo roots.
    
    Find a Smith basis for the weight lattice relative to the sublattice of roots, with corresponding invariant factors. It is almost equivalent to ``Smith(^Cartan_matrix(type))``, except that 
    (1). Smith_Cartan produces a separate diagonal block for each simple or torus factor, 
    (2). for factors ``T`` of the Lie type, ``Smith_Cartan`` produces a column with just '1' on the diagonal, but with corresponding "invariant factor" set equal to '0', and
    (3). for factors :math:`D_{2n}` an equivalent basis is given, which has been tweaked so that the final two vectors are standard basis vectors.

.. _filter_units:

filter_units
++++++++++++++

    ``(mat,vec->mat,vec)``: discard entries '1' and their columns.
    
    The input is presumably produced by ``Smith_Cartan`` or ``adapted_basis``; for all positions where the second (vector) component has '1', that entry and the corresponding column of the first matrix is discarded; what is left of the matrix and the vector is returned. If the vector has fewer entries than the matrix has columns (cf. ``adapted_basis``), missing entries count as not 1.

.. _ann_mod:

ann_mod
++++++++++++

    ``(mat,int->mat)``: find maximal matrix with product divisible by d.

    The call ``ann_mod(M,d)`` finds a square matrix A whose columns have the same height as those of M and span a maximal sublattice subject to the condition that the scalar product of every column of A with every column of M is divisible by d (the matrix product ``^A*M`` vanishes modulo d).
    
.. _replace_gen:

replace_gen
+++++++++++++

    ``((mat,vec),mat->mat)``: replace generators of weight lattice.
    
    The arguments are as for ``filter_units``. For every entry different from '1' in the vector argument, replace a column from the first matrix by a column from the second matrix. Both matrices must have the same column size; like for ``filter_units`` the vector may be short, missing entries being not 1.

.. _involution:

involution
+++++++++++++

    ``(LieType,string->mat)``: diagram involution for inner class.

    Return an involution matrix corresponding to the diagram involution described symbolically by the string, which is interpreted as the inner class string is in the Atlas, where 'e' or 'c' mean compact (equal rank), 'u' means unequal rank (for types :math:`A_n` with :math:`n>1`, :math:`D_n` and :math:`E_6`), 's' means split and 'C' means Complex. This is essentially a permutation matrix, except that for the split type on torus factors there is a diagonal entry -1

.. _involution2:

involution
++++++++++++

    ``(LieType,mat,string->mat)``: basic involution on given basis.

    This is like previous 'involution' for the same Lie type and inner class string, but the involution matrix is now expressed the given basis given by the columns of the matrix specified as second argument; this expression must be possible, so the sublattice spanned should be stable under the involution.

.. _root_datum:

root_datum
+++++++++++++

    ``(mat,mat->RootDatum)``: root datum from simple (co)root systems.

    In ``root_datum(roots,coroots)``, matrices roots and coroots must have the same dimensions (rank x semisimple rank); their columns give the desired systems of simple roots respectively simple coroots. The matrix of pairings of roots and coroots should be a valid Cartan matrix. A root datum with those systems of simple roots and simple coroots is returned.

.. _root_datum2:

root_datum
+++++++++++++

    ``(LieType,mat->RootDatum)``: root datum for given type and sublattice.
    
    The columns of the matrix argument are interpreted as specifying the basis of a sublattice of the character lattice of the "simply connected" group G of the given Lie type (which is a direct product of a simply connected semisimple group G' and a central torus S), expressed in the basis of fundamental weights of G' and an arbitrary basis for characters of S). For this to be possible, it is required that the sublattice contain the root lattice of G'. The sublattice becomes the standard lattice for working with the root datum, and is identified with Z^n using the given basis, which thus becomes the standard basis of the sublattice, henceforth called lattice.
    
.. _root_datum3:

root_datum
++++++++++++

    ``(RootDatum,mat->RootDatum)``: root datum for sublattice in old one
    
    This is like root_datum@(LieType,mat), but starting from the specified root datum rd rather than from the simply connected one for the Lie type. The provided sublattice matrix must be square and full rank (invertible of the rational numbers) and the roots of rd must be in its integral column span.

.. _root_datum4:

root_datum
+++++++++++++

    ``(InnerClass->RootDatum)``: root datum of inner class.

    Extract the root datum from the ``InnerClass`` value.

.. _quotient_basis:

quotient_basis
++++++++++++++++

``(LieType,[ratvec]->mat)``: sublattice given by kernel generators.

    Interpret the rational vectors as kernel generators for the given type, as in the atlas program, and return the corresponding sublattice as a matrix whose column are its generators. More precisely, the rational vectors represent linear combinations of certain coweights in the dual basis to a basis of the weight lattice adapted to the root lattice; for those weights in the latter basis that already lie in the root lattice, the corresponding coweight is omitted, since there are no useful rational multiples of it anyway. Return a basis for the sublattice of :math:`X^{\*}` of weights on which all kernel generators have integer evaluation. If M is the matrix whose columns are the numerators of the kernel generators, brought to a common denominator d, this amounts to setting ``S=Smith_Cartan(type)`` and ``(C,)=filter_units(S)``, and then returning the value ``replace_gen(S,C\*ann_mod(M,d))``. This function is intended for use in constructing root data; see basic.at

.. _simply_connected:

simply_connected
++++++++++++++++++

    ``(LieType->RootDatum)``: simply connected datum for given type.

    This gives the root datum for the "simply connected" group of the given type (the direct product of a simply conneted G' with a central torus): ``set simply_connected_datum(LieType type) = root_datum(type,id_mat(rank))``

.. _adjoint:

adjoint
++++++++++

    ``(LieType->RootDatum)``: adjoint root datum for given type.
    Here the sublattice for the semisimple factor is the root lattice, with simple roots as basis; for the central torus an arbitrary basis is used. Therefore the this function could be defined as
  
::

    set adjoint_datum(LieType type) =
    let M= for alpha@j in ^Cartan_matrix(type)
           do for entry@i in alpha
              do if i=j and entry=0 then 1 else entry fi
              od
           od
    in root_datum(type,M)

.. _dual:

dual
++++++++

    ``(RootDatum->RootDatum)``: dual of given root datum.

.. _derived_info:

derived_info
++++++++++++++++

    ``(RootDatum->RootDatum,mat)``: information for the derived group.
    
    The first result is the root datum for the derived group itself, the second result is a matrix mapping weights from the original to the derived datum.

.. _mod_central_torus_info:

mod_central_torus_info
++++++++++++++++++++++++

    ``(RootDatum->RootDatum,mat)``: quotient by central torus.

    The (semisimple) root datum obtained by quotienting by the central torus, and matrix embedding weights for the quotient datum into the original datum.

.. _rank2:

rank
++++++

    ``(RootDatum->int)``: Rank of the weight lattice for this Lie type.

.. _semisimple_rank2:

semisimple_rank
++++++++++++++++

    ``(RootDatum->int)``: Rank of the root lattice of  this Lie type.


