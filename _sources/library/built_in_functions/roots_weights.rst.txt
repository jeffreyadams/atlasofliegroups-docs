Roots and Weights
----------------------

.. list-table::
   :widths: 10 20
   :header-rows: 1
   
   * - Function
     - Argument(s) -> Result(s)
   * - :ref:`simple_roots`
     - ``(RootDatum->mat)``
   * - :ref:`simple_coroots`
     - ``(RootDatum->mat)``
   * - :ref:`posroots`
     - ``(RootDatum->mat)``
   * - :ref:`poscoroots`
     - ``(RootDatum->mat)``
   * - :ref:`roots`
     - ``(RootDatum->mat)``
   * - :ref:`coroots`
     - ``(RootDatum->mat)``
   * - :ref:`root_coradical`
     - ``(RootDatum->mat)``
   * - :ref:`coroot_radical`
     - ``(RootDatum->mat)``
   * - :ref:`fundamental_weight`
     - ``(RootDatum,int->ratvec)``
   * - :ref:`fundamental_coweight`
     - ``(RootDatum,int->ratvec)``
   * - :ref:`nr_of_posroots`
     - ``(RootDatum->int)``
   * - :ref:`root_index`
     - ``(RootDatum->int)``
   * - :ref:`coroot_index`
     - ``(RootDatum,vec->int)``
   * - :ref:`integrality_datum`
     - ``(RootDatum,ratvec->RootDatum)``
   * - :ref:`integrality_points`
     - ``(Rootdatum,ratvec->[rat])``


.. _simple_roots:

simple_roots
++++++++++++++++++

    ``(RootDatum->mat)``: matrix of simple roots in the root datum.

.. _simple_coroots:

simple_coroots
+++++++++++++++++++
    
    ``(RootDatum->mat)``: matrix of simple coroots in the root datum.

.. _posroots:

posroots
++++++++++++

    ``(RootDatum->mat)``: matrix of positive roots in the root datum.

.. _poscoroots:

poscoroots
++++++++++++

    ``(RootDatum->mat)``: matrix of positive coroots in the root datum.

.. _roots:

roots
+++++++

    ``(RootDatum->mat)``: set of roots in the root datum (columns of result).

.. _coroots:

coroots
++++++++++

    ``(RootDatum->mat)``: set of coroots in the root datum (as columns).

.. _root_coradical:

root_coradical
+++++++++++++++

    ``(RootDatum->mat)``: simple roots and coradical basis.
    
    With respect to simple_roots, add columns for coradical basis generators.

.. _coroot_radical:

coroot_radical
+++++++++++++++++++

    ``(RootDatum->mat)``: simple coroots and radical basis.
    
    With respect to ``simple_coroots``, add columns for radical basis generators.

.. _fundamental_weight:

fundamental_weight
++++++++++++++++++++

    ``(RootDatum,int->ratvec)``: fundamental weight number :math:`i`.
    
.. _fundamental_coweight:

fundamental_coweight
++++++++++++++++++++++++

    ``(RootDatum,int->ratvec)``: fundamental coweight number :math:`i`.

.. _nr_of_posroots:

nr_of_posroots
+++++++++++++++++

    ``(RootDatum->int)``: Number of positive roots in the root datum.

.. _root_index:

root_index
+++++++++++

    ``(RootDatum,vec->int)``: Index of root with respect to posroots.

.. _coroot_index:

coroot_index
+++++++++++++++

    ``(RootDatum,vec->int)``: Index of coroot with respect to poscoroots.
    
    These functions look up the vector in ``posroots(rd)`` or ``poscoroots(rd)``, and return the index found shifted down by ``nr_of_posroots(rd)``, so that the simple roots start at 0, and negative roots give a negative result. In case the vector is not found at all, the value ``nr_of_posroots(rd)`` is returned.


.. _integrality_datum:

integrality_datum
+++++++++++++++++++

    ``(RootDatum,ratvec->RootDatum)``: integral coroots subdatum.
    
    Applied to ``(rd,gamma)``, forms the root datum whose coroots form the closed subsystem of the coroots of rd that take an integral value on gamma.

.. _integrality_points:

integrality_points
++++++++++++++++++++

    ``(RootDatum,ratvec->[rat])``: fractions with integrality.
    
    The call integrality_points(rd,lambda) returns the increasing list of positive fractions f<=1 so f\* lambda has more integrality than generically: for some coroot alphav one has integral and nonzero value ``<alphav,f*lambda>``.

