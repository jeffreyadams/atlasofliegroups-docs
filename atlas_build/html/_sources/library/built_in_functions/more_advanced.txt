More Advanced Functions
----------------------------

.. list-table::
   :widths: 10 20
   :header-rows: 1
   
   * - Function
     - Argument(s) -> Result(s)
   * - :ref:`classify_involution`
     - ``(mat->int,int,int)``
   * - :ref:`inner_class`
     - ``(RootDatum,mat->InnerClass)``
   * - :ref:`twisted_involution`
     - ``(RootDatum,mat->InnerClass,vec)``
   * - :ref:`inner_class2`
     - ``(RootDatum,string->InnerClass)``
   * - :ref:`inner_class3`
     - ``(Lie_type,[ratvec],string->InnerClass)``
   * - :ref:`operator_=`
     - ``(InnerClass,InnerClass->bool)``
   * - :ref:`nr_of_real_forms`
     - ``(InnerClass->int)``
   * - :ref:`nr_of_dual_real_forms`
     - ``(InnerClass->int)``
   * - :ref:`nr_of_Cartan_classes`
     - ``(InnerClass->int)``
   * - :ref:`block_sizes`
     - ``(InnerClass->mat)``
   * - :ref:`form_names`
     - ``(InnerClass->[string])``
   * - :ref:`dual_form_names`
     - ``(InnerClass->[string])``
   * - :ref:`occurrence_matrix`
     - ``(InnerClass->mat)``
   * - :ref:`dual_occurrence_matrix`
     - ``(InnerClass->mat)``
   * - :ref:`real_form`
     - ``(InnerClass,int->RealForm)``
   * - :ref:`inner_class`
     - ``(RealForm->InnerClass)``
   * - :ref:`form_number`
     - ``(RealForm->int)``
   * - :ref:`quasisplit_form`
     - ``(InnerClass->RealForm)``
   * - :ref:`components_rank`
     - ``(RealForm->int)``
   * - :ref:`count_Cartans`
     - ``(RealForm->int)``
   * - :ref:`operator_=2`
     - ``(RealForm,RealForm->bool)``
   * - :ref:`KGB_size`
     - ``(RealForm->int)``
   * - :ref:`base_grading_vector`
     - ``(RealForm->ratvec)``
   * - :ref:`Cartan_order`
     - ``(RealForm->mat)``
   * - :ref:`dual_real_form`
     - ``(InnerClass,int->RealForm)``
   * - :ref:`dual_quasisplit_form`
     - ``(InnerClass->RealForm)``
   * - :ref:`Cartan_class`
     - ``(InnerClass,int->CartanClass)``
   * - :ref:`Cartan_class2`
     - ``(RealForm,int->CartanClass)``
   * - :ref:`most_split_Cartan`
     - ``(RealForm->CartanClass)``
   * - :ref:`involution4`
     - ``(CartanClass->mat)``
   * - :ref:`Cartan_info`
     - ``(CartanClass->(int,int,int),vec,(int,int),(LieType,LieType,LieType))``
   * - :ref:`real_forms`
     - ``(CartanClass->[RealForm])``
   * - :ref:`dual_real_forms`
     - ``(CartanClass->[RealForm])``
   * - :ref:`square_classes`
     - ``(CartanClass->[[int]])``
   * - :ref:`fiber_partition`
     - ``(CartanClass,RealForm->[int])``
   * - :ref:`real_form2`
     - ``(InnerClass,mat,ratvec->RealForm)``
   * - :ref:`central_fiber`
     - ``(RealForm->[vec])``
   * - :ref:`initial_torus_bits`
     - ``(RealForm->vec)``



.. _classify_involution:

classify_involution
++++++++++++++++++++

    ``(mat->int,int,int)``: determine type of lattice involution

    For any linear involution of :math:`\mathbb{Z}^n`, there is a basis consisting of certain vectors that are eigenvectors with eigenvalues 1 or -1 for the involution, and of pairs of vectors that are interchanged by the involution. The numbers of such vectors for each eigenvalue and of interchanged pairs determine the involution up to base change. This function, which requires its argument to be the matrix of an involution, returns these three numbers in the following order: eigenvectors for 1 (compact rank), pairs of interchanged vectors (Complex rank), eigenvectors for -1 (split rank).

.. _inner_class:

inner_class
++++++++++++++

    ``(RootDatum,mat->InnerClass)``: inner_class of G from involution
    
    This is the basic function for building a complex reductive group equipped with an involution from the root datum and that involution; the latter is given on the lattice basis of the root datum, and must describe an involutive automorphism of the root datum. The involution is converted to a based root datum involution if necessary, using the Weyl group.

.. _twisted_involution:

twisted_involution
+++++++++++++++++++

    ``(RootDatum,mat->InnerClass,vec)``: inner_class and Weyl word
    Build an inner class as the above function, and also return a Weyl word (twisted involution) that expresses the given involution in that inner class. The latter is a reduced word (with Weyl group generators numbered from 0), to be left-multiplied to the distinguished involution.

.. _inner_class2:

inner_class
+++++++++++++

    ``(RootDatum,string->InnerClass)``: get inner class of G symbolically
    Build a complex reductive group directly from a root datum, but compute the distinguished involution from the string describing it symbolically.
    
.. _inner_class3:

inner_class
+++++++++++++

    ``(Lie_type,[ratvec],string->InnerClass)``: inner class as in Atlas
    
.. _operator_=:

\=
++++

    ``(InnerClass,InnerClass->bool)``: identity of inner classes

    This holds only when both arguments refer to the same inner class creation, in other words it will recognize ``ic=inner_class(real_form(ic,0))`` as true, but any freshly built inner class tests unequal to anything preexisting ``distinguished_involution``: ``(InnerClass->mat)``: involution of the inner class. Extract the distinguished involution of :math:`X^*` that defines the inner class dual: ``(InnerClass->InnerClass)``: dual inner class for dual complex group

.. _nr_of_real_forms:

nr_of_real_forms
+++++++++++++++++

    ``(InnerClass->int)``: number of real forms in inner class
    
.. _nr_of_dual_real_forms:

nr_of_dual_real_forms
+++++++++++++++++++++++

    ``(InnerClass->int)``: number of dual forms in inner class

.. _nr_of_Cartan_classes:

nr_of_Cartan_classes
++++++++++++++++++++++

    ``(InnerClass->int)``: total number of Cartans in inner class

.. _block_sizes:

block_sizes
+++++++++++++

    ``(InnerClass->mat)``: matrix giving the block sizes.

    This is essentially the same as the output of 'blocksizes' in Atlas; the rows of the matrix correspond to real forms for the inner class, and the columns correspond to dual real forms for the inner class.

.. _form_names:

form_names
++++++++++++++++

    ``(InnerClass->[string])``: list of names of real forms.

    These are the same names used in atlas, describing real Lie algebras

.. _dual_form_names:

dual_form_names
++++++++++++++++

    ``(InnerClass->[string])``: list of names of dual real forms.

    These are the names for the real forms of the dual InnerClass value


.. _occurrence_matrix:

occurrence_matrix
+++++++++++++++++++

    ``(InnerClass->mat)``: real form-Cartan class incidence matrix

    For the given inner class, construct a matrix whose rows are parametrized by the real forms, and whose columns are parametrized by the Cartan classes, showing whether (1) or not (0) the Cartan class occurs for the real form 

.. _dual_occurrence_matrix:

dual_occurrence_matrix
+++++++++++++++++++++++++

    ``(InnerClass->mat)``: dual real form-Cartan class matrix. This is like ``occurrence_matrix``, but with rows representing dual real forms.

.. _real_form:

real_form
+++++++++++

    ``(InnerClass,int->RealForm)``: select a real form from inner class.
    
    The result of form_names describes the valid range and names of real forms; this function actually constructs a real form from the list, selected by its position (starting from 0). The list is always the same for a given inner class (independent of other computations), unlike the list of Cartan classes for a real form as discussed below
    
    ``inner_class: (RealForm->InnerClass)``: inner class containing the form

.. _form_number: 

form_number
++++++++++++++

    ``(RealForm->int)``: index of the real form in its inner class

.. _quasisplit_form:

quasisplit_form
+++++++++++++++++

    ``(InnerClass->RealForm)``: quasisplit form for the inner class

    This is the last one in the list of real forms for the fundamental Cartan (number 0 in the list) of the inner class.


.. _components_rank:

components_rank
++++++++++++++++

    ``(RealForm->int)``: rank of the component group

    The group of connected components of the real Lie group defined by a real form is an elementary 2-group (:math:`\mathbb{Z}/2\mathbb{Z}` vector space); this function gives its rank, so the number of connected components is 2^components_rank(rf)

.. _count_Cartans:

count_Cartans
++++++++++++++++

    ``(RealForm->int)``: number of Cartan classes for this real form

    The Cartan classes are actually constructed, and remembered, by this command whence its first execution for some real form may take some time

.. _operator_=2:

\=
++++

    ``(RealForm,RealForm->bool)``: equality of real forms
    
    It means they belong to an identical inner class, and have same form number

.. _KGB_size:

KGB_size
+++++++++++++
    ``(RealForm->int)``: size of the set :math:`K\backslash G/B` for this real form
    
.. _base_grading_vector:

base_grading_vector
+++++++++++++++++++++

    ``(RealForm->ratvec)``: Offset implicit in ``torus_bits`` values
    
    The binary vectors torus_bits for elements of the KGB associated to a real form are relative to a special torus element t0, and this function produces a dominant rational coweight c for which :math:`\exp(\pi i c)` equals this t0. The choice of t0 and of c are constant for each "square class" of real forms (which are grouped together in the output of print_strong_real for the fundamental Cartan), for which the squares of any of their strong involutions are the same torus element z: the choice of c is subject to :math:`\exp(2\pi i(c+rho_check))=z` which reflects :math:`(t0)^2\exp(2\pi i rho_check)=z`.

    Apart from z, the choice of c (or of t0) defines an implicit "base grading" of the simple roots at the distinguished involution of the inner class, by the parity of the (integer) pairing of c with the simple root. Here "odd" corresponds to grading 0, due to the mentioned rho_check: so c differs by ``rho_check`` from some "inifinitesimal cocharacter" g chosen for the real form. A standard choice for c is determined by the base grading for the  weak real form, whence the name of this function. However for real forms synthesized by the function ``real_form@(InnerClass,mat,ratvec)``, the arguments of that call may determine a different value of z, in which case a different choice for c is made to match it. The choice of c then depends on z only; in particular it will be the same for real forms synthesized using different strong involutions for the same real group, and such groups will test equal.

.. _Cartan_order:

Cartan_order
+++++++++++++++

    ``(RealForm->mat)``: matrix describing ordering of Cartan classes
    
    The Cartan classes for a given real form form a partially ordered set; this function returns this partial ordering in the form of a square 0-1 matrix.

.. _dual_real_form:

dual_real_form
++++++++++++++++++

    ``(InnerClass,int->RealForm)``: select a dual real form

    This is like real_form, but selects a dual real form for the inner class (whose names are given by ``dual_form_names``) by index. This is intended for functions that require both a real form and a dual real form for a given inner class; the compatibility between them is tested by a runtime check. 
    
.. _dual_quasisplit_form:

dual_quasisplit_form
+++++++++++++++++++++++

    ``(InnerClass->RealForm)``: quasisplit dual real form

.. _Cartan_class:

Cartan_class
+++++++++++++++++

    ``(InnerClass,int->CartanClass)``: Cartan class selected by number

    This selects a Cartan class by number in the list of all Cartan classes for this inner class. The numbering is fixed, and compatible with  the partial ordering on Cartan classes where more split ones are considered greater.

.. _Cartan_class2:

Cartan_class
+++++++++++++++

    ``(RealForm,int->CartanClass)``: Cartan class selected by number
    

    This selects a Cartan class by number in the list of Cartan classes defined for this real form. The numbering is not the same as when selecting a Cartan class directly from an inner class, unless the real form is quasisplit.

.. _most_split_Cartan:

most_split_Cartan
++++++++++++++++++

    ``(RealForm->CartanClass)``: most split Cartan class for form
    
    The most split Cartan class of a given real form is the last one in the list of its Cartan classes, so set ``most_split_Cartan(RealForm rf)``=``Cartan_class(rf,count_Cartans(rf)-1)``

.. _involution4:

involution
++++++++++++++

    ``(CartanClass->mat)``: weight lattice involution for Cartan class
    
.. _Cartan_info:

Cartan_info
++++++++++++++

    ``(CartanClass->(int,int,int),vec,(int,int),(LieType,LieType,LieType))``:

    Information about the Cartan class, essentially that given by the output of 'cartan' in Fokko (except for the final partition corresponding to the real forms for this Cartan class, for which see fiber_partition). The first triple of integers gives in order the number of compact (:math:`U(1)`), complex (:math:`GL(1,\mathbb{C})`), and split (:math:`GL(1,\mathbb{R})`) factors of the real torus defined by this Cartan class. Follows the canonical twisted involution for the Cartan class, a pair of integers giving the number of distinct twisted involutions defining this same Cartan class and their fiber size, and finally the types of the imaginary, real, and complex root subsystems (note the order here).

.. _real_forms:

real_forms
+++++++++++

    ``(CartanClass->[RealForm])``: list of real forms with given Cartan

    Returns a list of the real forms for which this Cartan class occurs 

.. _dual_real_forms:
    
dual_real_forms
++++++++++++++++++++++

    ``(CartanClass->[RealForm])``: list Cartan's dual real forms

    Returns a list of the dual real forms for which this Cartan class occurs

.. _square_classes:

square_classes
++++++++++++++++++

    ``(CartanClass->[[int]])``: partition real forms by square class

    This returns a list of lists of numbers that identify real forms in the inner class. All real forms whose representative strong involutions may square to the same value in the center are grouped together in a sublist (the number of sublists is a power of 2). Each number occurs only in a single sublist, but may be repeated, which indicates that there are mulitple orbits of strong involutions (strong real forms) for the same real form. The value returned represents a part of the print_strong_real output.
    
.. _fiber_partition:

fiber_partition
+++++++++++++++++

    ``(CartanClass,RealForm->[int])``: identifying part of fiber group

    This produces an increasing sequence of integers that characterizes the real form relative to the CartanClass. It describes a part of the adjoint fiber group associated to the Cartan class (an elementary 2-group of rank r equal to the number of compact factors of the real torus in the _adjoint_ group defined by the Cartan class), whose elements are represented by numbers 0 to :math:`2^r-1`; as the real form traverses all those for which this Cartan class occurs, the results of the function form a partition of that set of numbers.

.. _real_form2:

real_form
++++++++++++

    ``(InnerClass,mat,ratvec->RealForm)``: real form from strong real form

    Synthesize a real form defined by an involution and a torus factor. With arguments (ic,M,v), the matrix M should define an involution theta in the inner class. The rational vector v, after being made right M-fixed by right multiplication by (M+1)/2, defines a torus element :math:`\exp(\pi i v)` whose square must be central, which means that v*alpha must be integral for all (simple) roots alpha. If this holds then theta and torus_factor v together define a strong involution representative. The function returns the strong real form rf identified by that strong involution. It may differ from real_form(ic,form_number(rf)), the standard version of this weak real form; the difference can be seen through the value of base_grading_vector(rf), and in the RealForm equality test (because of this distinction, one may consider the result to represent a strong real form). Real forms produced by this function are said to be synthesized (rather than selected). A subsequent call KGB_elt(rf,theta,v) should always produce a valid KGB element x. The grading of the imaginary roots alpha for theta defined by this x will be given by the parity of :math:`< v+\check\rho_i, \alpha >`, where :math:`\check\rho_i` is half the sum of the positive imaginary coroots for M (its presence in the formula ensures that v=0 is always valid, and grades all simple-imaginary roots as noncompact). This grading is the most tangible aspect of (theta,v), but only determines the weak real form, and may fail to identify a unique KGB element x; this function and the mentioned instance of KGB_elt are faithful beyond just reconstructing the correct grading.
    
.. _central_fiber:

central_fiber
+++++++++++++++

    ``(RealForm->[vec])``: Set of torus bits not affecting any gradings

    These are binary vectors that can be added to ``|torus_bits|`` of KGB elements in the fundamental fiber to get another KGB element giving the same status (including compactness of imaginary roots) to every simple root; adding any of these values to torus bits defines an automorphism of the KGB structure

.. _initial_torus_bits:

initial_torus_bits
+++++++++++++++++++++

    ``(RealForm->vec)``: Torus bits for initial KGB element

    This is a test function, computing what should be the torus bits of KGB(G,0) independently of what is currently set in the implementation. They could differ from reality by an element of ``|central_fiber(G)|``. This function can be removed once the same computation will actually replace the implemented choice for the torus bits with which the KGB construction starts off.

