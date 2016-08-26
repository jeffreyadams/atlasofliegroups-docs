KGB Related
-------------------

.. list-table::
   :widths: 10 20
   :header-rows: 1
   
   * - Function
     - Argument(s) -> Result(s)
   * - :ref:`KGB`
     - ``(RealFrom,int->KGBElt)``
   * - :ref:`operator_%2`
     - ``(KGBElt->RealForm,int)``
   * - :ref:`Cartan_class4`
     - ``(KGBElt->CartanClass)``
   * - :ref:`involution3`
     - ``(KGBElt->mat)``
   * - :ref:`length`
     - ``(KGBElt->int)``
   * - :ref:`status`
     - ``(int,KGBElt->int)``
   * - :ref:`status2`
     - ``(vec,KGBElt->int)``
   * - :ref:`cross`
     - ``(int,KGBElt->KGBElt)``
   * - :ref:`Cayley`
     - ``(int,KGBElt->KGBElt)``
   * - :ref:`twist`
     - ``(KGBElt->KGBElt)``
   * - :ref:`torus_factor`
     - ``(KGBElt->ratvec)``
   * - :ref:`torus_bits`
     - ``(KGBElt->vec)``
   * - :ref:`operator_=3`
     - ``(KGBElt,KGBElt)``
   * - :ref:`block2`
     - ``(RealForm,RealForm->Block)``
   * - :ref:`operator_%3`
     - ``(Block->RealForm,RealForm)``
   * - :ref:`operator_#`
     - ``(Block->int)``
   * - :ref:`element`
     - ``(Block,int->KGBElt,KGBElt)``
   * - :ref:`index`
     - ``(Block,KGBElt,KGBElt->int)``
   * - :ref:`dual2`
     - ``(Block->Block)``
   * - :ref:`status3`
     - ``(int,Block,int->)``

.. _KGB:

KGB
+++++++++

    ``(RealFrom,int->KGBElt)``: select a KGB element x among those of a real form

    The call ``KGB(i,rf)`` selects the element in line i of the ``print_KGB(rf)`` output.
    
.. _operator_%2:

\%
+++

    ``(KGBElt->RealForm,int)``: real form and number; inverse of ``KGB@(RealForm,int)``
    
.. _Cartan_class4:

Cartan_class
+++++++++++++++++

    ``(KGBElt->CartanClass)``: the Cartan class for the KGB element
    
.. _involution3:

involution
+++++++++++++

    ``(KGBElt->mat)``: the involution of X^* associated to the KGB element

.. _length:

length
+++++++

    ``(KGBElt->int)``: length of the element within its KGB set

.. _status:

status
++++++++

    ``(int,KGBElt->int)``: status of generator on KGB element, scale 0..4

    Encoding 0: Complex descent, 1: imaginary compact, 2: real, 3: imaginary non-compact, 4: Complex ascent

.. _status2:

status
++++++++

    ``(vec,KGBElt->int)``: status of any root on KGB element, scale 0..4

    The value status(alpha,x) gives the status of the root alpha at x; the encoding of statuses is the same as for the function status@(int,KGBElt)
  
.. _cross:

cross
++++++

    ``(int,KGBElt->KGBElt)``: cross action for (posrootnr,KGB element)

    Returns result of cross action by root reflection of the given KGB element
  
.. _Cayley:

Cayley
++++++++++

    ``(int,KGBElt->KGBElt)``: Cayley transform for (posrootnr,KGB element)

    Returns either the Cayley transform or an inverse Cayley transform of the KGB element through the given positive root, or returns that element itself when neither is defined. If defined, one can find which it is using status, and whether there is a second inverse Cayley transform can be found out by applying cross action to the result; it either returns the same result, which signifies a single-value inverse Cayley, or else the second value
  
.. _twist:

twist
++++++++

    ``(KGBElt->KGBElt)``: twist of KGB element x, useful for Hermitian dual

    This is defined by conjugation of x by the distinguished involution delta

.. _torus_factor:

torus_factor
++++++++++++++

    ``(KGBElt->ratvec)``: coweight for KGB element, twice that in print_X

    This is a :math:`\theta^t` stable rational vector v with integral evaluations on all imaginary roots; interpreted modulo the image of 1+\theta^t acting on :math:`X_*`, so in particular modulo :math:`(2\\mathbb{Z})^n`. For an imaginary root :math:`\alpha` the scalar product :math:`langle v + \check\rho_i , \alpha \rangle` determines whether :math:`\alpha` is compact (if even) or noncompact (if odd). Together with the inner class and the invlution, this value completely characterises the KGB element (and its real form), and it can be reconstructed using the ``KGB_elt`` function below.
  
.. _torus_bits:

torus_bits
+++++++++++++

    ``(KGBElt->vec)``: torus part of KGB element as vector of 0,1 values

    A vector of size the rank that distinguishes between different KGB elements at the same involution, in the format used internally. From this the value torus_factor(x) is computed using base_grading_vector(rf)-torus_bits(x), for the real form rf of x, which value is then symmetrized for \theta^t.
  
.. _KGB_elt:

KGB_elt
+++++++++++

    ``(RealForm,mat,ratvec)``: KGB element defined by rational coweight

    This function finds a KGB element x such that ``real_form(x)``, ``involution(x)``, and ``torus_factor(x)`` match the values ``(rf,M,v)`` given as arguments. The interpretation for the (involution) matrix M and rational (coweight) vector v are as for ``real_form@(InnerClass,mat,ratvec)``; moreover rf should be equal to the real form returned (for this inner class) by ``real_form(ic,M,v)``, and the difference ``v-base_grading_vector(rf)`` must be an integer vector. There is then at most one KGB element x for rf such that ``torus_factor(x)`` is congruent to v modulo the image of ``^M+1`` (i.e., M+1 applied on right), which x is then returned by this function (if no such x is found, an error is signaled).

.. _operator_=3:

\=
+++++++++++++

    ``(KGBElt,KGBElt)``: equality of elements of a same KGB set


.. _block2:

block
+++++++

    ``(RealForm,RealForm->Block)``: construct tradiational atlas block

.. _operator_%3:

\%
+++++++++++++

    ``(Block->RealForm,RealForm)``: decompose block, inverse of 'block'

.. _operator_#:

#
++++++++

    ``(Block->int)``: number of elements of block

.. _element:

element
++++++++++

    ``(Block,int->KGBElt,KGBElt)``: KGB and dual KGB values for block element

.. _index:

index
+++++++

    ``(Block,KGBElt,KGBElt->int)``: index in block, from KGB, dual KGB components
    This is the inverse of the map defined by element@(Block,int): given a compatible pair of a KGB element x and a dual KGB element y, it returns the index in the block of the corresponding element. For efficiency reasons the function requires the containing block to be supplied as first argument; if needed, ``block(real_form(x),dual_real_form(real_form(y)))`` computes the block
  
.. _dual2:

dual
+++++

    ``(Block->Block)``: dual block, with real form and dual real form swapped

.. _status3:

status
++++++++

    ``(int,Block,int->)``: status at a block element of a simple reflection
    
    For s the index of a reflection, and i the index of an element of block b, status(s,b,i) gives according to the codes 0:C-, 1:ic, 2:r1, 3:r2,  4:C+, 5: rn, 6:i1, 7:i2. Note that the descents s have status(b,i,s)<4