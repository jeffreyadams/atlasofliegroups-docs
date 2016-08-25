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
   * - :ref:`involution3`
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
   * - :ref:`KGB`
     - ``(RealFrom,int->KGBElt)``
   * - :ref:`operator_%2`
     - ``(KGBElt->RealForm,int)``
   * - :ref:`Cartan_class3`
     - ``(KGBElt->CartanClass)``


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

    ``(RealForm->ratvec)``: Offset implicit in torus_bits values
    
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

.. _Cartan_class3:

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

.. _involution3:

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


.. _KGB:

KGB
+++++++++

    ``(RealFrom,int->KGBElt)``: select a KGB element x among those of a real form

    The call ``KGB(i,rf)`` selects the element in line i of the ``print_KGB(rf)`` output.
    
.. _operator_%2:

\%
+++

    ``(KGBElt->RealForm,int)``: real form and number; inverse of ``KGB@(RealForm,int)``
    
.. _Cartan_class:

Cartan_class
+++++++++++++++++

    ``(KGBElt->CartanClass)``: the Cartan class for the KGB element
    
involution: (KGBElt->mat): the involution of X^* associated to the KGB element

length: (KGBElt->int): length of the element within its KGB set

status: (int,KGBElt->int): status of generator on KGB element, scale 0..4
  Encoding 0: Complex descent, 1: imaginary compact, 2: real,
  3: imaginary non-compact, 4: Complex ascent
  
status: (vec,KGBElt->int): status of any root on KGB element, scale 0..4
  The value status(alpha,x) gives the status of the root alpha at x; the
  encoding of statuses is the same as for the function status@(int,KGBElt)
  
cross: (int,KGBElt->KGBElt): cross action for (posrootnr,KGB element)
  Returns result of cross action by root reflection of the given KGB element
  
Cayley: (int,KGBElt->KGBElt): Cayley transform for (posrootnr,KGB element)
  Returns either the Cayley transform or an inverse Cayley transform of the
  KGB element through the given positive root, or returns that element itself
  when neither is defined. If defined, one can find which it is using status,
  and whether there is a second inverse Cayley transform can be found out by
  applying cross action to the result; it either returns the same result,
  which signifies a single-value inverse Cayley, or else the second value
  
twist: (KGBElt->KGBElt): twist of KGB element x, useful for Hermitian dual
  This is defined by conjugation of x by the distinguished involution delta
  
torus_factor: (KGBElt->ratvec): coweight for KGB element, twice that in print_X
  This is a \theta^t stable rational vector v with integral evaluations on
  all imaginary roots; interpreted modulo the image of 1+\theta^t acting
  on X_*, so in particular modulo (2\Z)^n. For an imaginary root \alpha
  the scalar product < v + \check\rho_i , \alpha > determines whether \alpha
  is compact (if even) or noncompact (if odd). Together with the inner class
  and the invlution, this value completely characterises the KGB element (and
  its real form), and it can be reconstructed using the KGB_elt function below.
  
torus_bits: (KGBElt->vec): torus part of KGB element as vector of 0,1 values
  A vector of size the rank that distinguishes between different KGB elements
  at the same involution, in the format used internally. From this the value
  torus_factor(x) is computed using base_grading_vector(rf)-torus_bits(x), for
  the real form rf of x, which value is then symmetrized for \theta^t.
  
KGB_elt: (RealForm,mat,ratvec): KGB element defined by rational coweight
  This function finds a KGB element x such that real_form(x), involution(x),
  and torus_factor(x) match the values (rf,M,v) given as arguments. The
  interpretation for the (involution) matrix M and rational (coweight) vector
  v are as for real_form@(InnerClass,mat,ratvec); moreover rf should be equal
  to the real form returned (for this inner class) by real_form(ic,M,v), and
  the difference v-base_grading_vector(rf) must be an integer vector. There is
  then at most one KGB element x for rf such that torus_factor(x) is congruent
  to v modulo the image of ^M+1 (i.e., M+1 applied on right), which x is then
  returned by this function (if no such x is found, an error is signaled).

operator = : (KGBElt,KGBElt): equality of elements of a same KGB set



block: (RealForm,RealForm->Block): construct tradiational atlas block

%: (Block->RealForm,RealForm): decompose block, inverse of 'block'

#: (Block->int): number of elements of block

element: (Block,int->KGBElt,KGBElt): KGB and dual KGB values for block element

index (Block,KGBElt,KGBElt->int): index in block, from KGB, dual KGB components
  This is the inverse of the map defined by element@(Block,int): given a
  compatible pair of a KGB element x and a dual KGB element y, it returns the
  index in the block of the corresponding element. For efficiency reasons the
  function requires the containing block to be supplied as first argument; if
  needed, block(real_form(x),dual_real_form(real_form(y))) computes the block
  
dual: (Block->Block): dual block, with real form and dual real form swapped

status: (int,Block,int->): status at a block element of a simple reflection
  For s the index of a reflection, and i the index of an element of block b,
  status(s,b,i) gives according to the codes 0:C-, 1:ic, 2:r1, 3:r2,  4:C+,
  5: rn, 6:i1, 7:i2. Note that the descents s have status(b,i,s)<4


param: (KGBElt,vec,ratvec->Param): form parameter from (x,lambda-rho,nu)

operator % : (Param->KGBElt,vec,ratvec): recover (x,lambda-rho,nu) from param

real_form: (Param->RealForm): recover the real form from a Param value

infinitesimal_character: (Param->ratvec): infinitesimal character of parameter
  This is actually a representative of the infinitesimal character, given by
  gamma = ((1+theta)lambda+(1-theta)nu)/2. The meaning of the x component of
  the parameter is determined by its position relative to this representative
  gamma, so to find the x value uniquely associated to the representation for
  the parameter, one should apply the function 'dominant' to the parameter
  first, after which the value of infinitesimal_character is indeed dominant
  
is_standard: (Param->bool): whether parameter defines a standard module
  This is true whenever gamma is dominant relative to the imaginary roots
  
is_zero: (Param->bool): whether parameter defines a zero standard module
  True whenever gamma is singular on a compact (for x) simple-imaginary root
  
is_final: (Param->bool): whether parameter defines a final standard module
  False whenever associated standard representation is combination of others
  on more compact Cartans by a Hecht-Schmid identity. So is_final(p) is true
  provided no real coroots for which gamma is singular satisfy the parity
  condition. Note: one could still have is_zero(p); this needs a separate test.
  
dominant: (Param->Param): make gamma dominant and do singular complex descents
  This brings the parameter p into standard form, in which it will appear when
  p occurs in a ParamPol (which also requires is_final(p) and not is_zero(p)).
  
operator = : (Param,Param->bool): test equivalence of parameters
  This is implemented by applying dominant and testing identity of all
  three components x, lambda (defined modulo (1-theta_x)X^*) and nu.
  
cross: (int,Param->Param): cross action for (Weyl group generator,parameter)
  This first argument indexes (starting at 0) a simple root for the subsystem
  for the given parameter p: integrality_datum(infinitesimal_character(p))
  
Cayley: (int,Param->Param): Cayley transform for (Weyl generator,parameter)
  If (and only if) the transform is undefined it returns the same parameter
  Find out possible second value by applying cross action to the result
  
inv_Cayley: (int,Param->Param): inverse Cayley transform
  If (and only if) the inverse transform is undefined it returns the same
  parameter. Find out possible second value of invere transform by applying
  cross action to the result, which either produces it or else fixes result
  
cross: (vec,Param->Param): cross action for (root,parameter)

Cayley: (vec,Param->Param): Cayley transform for (root,parameter)
  These two functions should do the same as the three before, but taking the
  root in coordinates, and combining the Cayley/inverse Cayley into one
  function (whichever is defined is applied, or else the parameter returned).
  The implementation is quite independent however, so comparison is useful.

twist: (Param->Param): twist the parameter by the distinguihed involution

orientation_nr: (Param->int): the orientation number

reducibility_points: (Param->[rat]): the 0<t<=1 with I(x,lambda,t\nu) reducible

print_block: (Param->): print (nonintegral) block generated from parameter

block: (Param->[Param],int): return block as list of parameters, and index
  The second component is the index into the first of the original parameter.

partial_block: (Param->[Param]): return partial block as list of parameters
  This is the Bruhat interval of the block below the given parameter,
  sorted by length and including the given parameter as final element

length: (Param->int): the length of a parameter within its block

KL_block: (Param->[Param],int,mat,[vec],vec,vec,mat): block, raw_KL, and more
  This combines block with the Kazhdan-Lustzig table for the block appended,
  and two more values that allow cumulation to be performed. The two values of
  block are followed by three values in the format of raw_KL below: a matrix
  of indices into the following list of polynomials, coded as a list of
  coefficient vectors, then a list of indices where the length function
  increases. Finally follow a vector with indices of the "surviving" block
  elements, and a matrix whose rows correspond to those survivors, its columns
  to all block elements, and whose the entries gives the coefficients by which
  each the block element (column) contributes to the surviving element (row),
  with a sign given by the parity of their length difference. Here "surviving"
  refers to the result of applying a translation functor to a standard module,
  namely a functor from regular infinitesimal character to the current
  (possibly) singular infinitesimal character. Thus one can transform the
  given KL matrix (computed at regular infinitesimal character) to one at the
  actual block by selecting only the columns whose index is among the
  survivors, and multiplying the resulting matrix on the left by the
  contibution-coefficient matrix (the final component this function returns).

partial_KL_block: (Param->[Param],mat,[vec],vec,vec,mat) partial KL_block
  This function relates to KL_block as partial_block relates to block. The
  first component of the result is the Bruhat interval as in partial_block,
  and all other components are the same is in KL_block (except that the now
  superfluous second component of KL_block is omitted), but with the two vec
  components filtered so as to be indexed by the Bruhat interval indices only.


operators =, != : (Split->bool): test split integer against Split:(0,0)
operators =, != : (Split,Split->bool): equality/inequality of split integers
operator + : (Split,Split->Split): addition of split integers
operator - : (Split,Split->Split): subtraction of split integers
operator - : (Split->Split): negation of a split integer
operator * : (Split,Split->Split): multiplication of split integers
operator % : (Split,int,int): decomposition of split integer into components

null_module: (RealForm->ParamPol): empty sum of parameters for the real form
real_form: (ParamPol->RealForm): recover the real form from a ParamPol value
operator # : (ParamPol->int): number of nonzero terms of the formal sum
operators =, != : (ParamPol->bool): test virtual module for being zero
operators =, != : (ParamPol,ParamPol->bool): test virtual modules for equality
operator +, - : (ParamPol,Param->ParamPol): add/subtract parameter to formal sum
operator + : (ParamPol,(Split,Param)->ParamPol): add parameter with coefficient
operator + : (ParamPol,[(Split,Param)]->ParamPol): add terms to formal sum
operators +, - : (ParamPol,ParamPol->ParamPol): addition/subtraction formal sums
operator * : (int,ParamPol->ParamPol): integer multiple of a formal sum
operator * : (Split,ParamPol->ParamPol): split integer multiple of a formal sum
last_term: (ParamPol->Split,Param): highest term (for #x(p)) of non-empty module
first_term: (ParamPol->Split,Param): lowest term (for #x(p)) of non-empty module

K_type_formula: (Param->ParamPol) Express K-type in terms of standardrepns|_K
  The argument parameter is interpreted as giving an irreducible module; its
  restriction to K is expressed as linear combination of restrictions to K of
  standard representations, and a polynomial giving their parameters returned.

branch: (Param,int->ParamPol) Find K-types of standardrepn up to given limit
  The first argument is taken as standard representation, and is interpreted
  as restricted to K (the nu component is replaced by a zero vector), while
  the argument second is a bound on the height; the result should be
  interpreted as linear combination of K-types, each standard final parameter
  term standing for its lowest K-type.

to_canonical: (Param->Param) Move parameter to canonical fiber (making nu=0)

height: (Param->int) W-invariant height measure standardrepn restricted to K
  This is the sum of absolute values of the scalar products of (1+theta)lambda
  and the positive coroots; it ignores the nu component of the parameter.
  This is the same function as used in branch to compare with the given limit.


deform: (Param->ParamPol): compute deformation terms when nu decreases
  The non-integral block for the parameter and its KL polynomials are
  computed, from which the deformation terms involing other members of the
  block are computed. They are returned as a formal sum of paramters with
  split integer coefficients, which are in fact integer multiples of (1-s).

full_deform: (Param->ParamPol): perform deformation all the way to nu=0
  This is like deform, but recursively deforms all new terms produced as long
  as they do not have nu=0; all terms in the result therefore have nu=0.

KL_sum_at_s: (Param->ParamPol): signed sum of KL polynomials at s, fixed y
  Computes \sum_{x\leq y}(-1)^{l(y)-l(x)}P_{x,y}[q:=s].x where y is the block
  element of the parameter, and the sum is over other block elements x.

raw_KL: (Block->mat,[vec],vec): Kazhdan-Lusztig data for block, raw form
  The call raw_KL(b) produces a matrix of numbers identifying polynomials, a
  list of those polynomials in the form of coefficient vectors, and a sequence
  of length boundaries that allow deducing the "lengths" of the integers used
  to index the matrix. These integers identify block elements for the block
  print_block(b). If (M,L,len)=raw_KL(b), and v,w are integers identifying
  block elements, then the vector L[M[v,w]] gives the coefficients of the KL
  polynomial P_{v,w}. The length of v is the lergest index i such that
  len[i]<=v, so the length difference between v and w is the number of indices
  with v<len[i]<=w.

dual_KL: (Block->mat,[vec],vec): dual KL polynomials (Q_{x,y}) for block
  This is like raw_KL, but computes the polynomials Q instead of P. The
  indexing of the block is the same as for the polynomials P, so up to length
  signs, the matrix should be the inverse of the P matrix. The length stops
  are provided as final value, as in raw_KL; these are for the _same_ block.

print_gradings: (CartanClass,RealForm->): print gradings defined by real form
  This more or less gives the output of the 'gradings' command in the Atlas
  software, for the selected real form. The type of the imaginary root system
  is printed, with the numbers of the roots that span this root subsytem as
  simple roots, in the Bourbaki ordering for its type. Then for each element
  in the list produced by fiber_part for the same arguments, the grading of
  the imaginary root system is given as a sequence of bits 0 (compact) or 1
  (non-compact), to be interpreted on the simple roots in the given order, and
  extended to the whole imaginary root subsystem as a Z/2Z grading.

print_real_Weyl: (RealForm,CartanClass->)
print_strong_real: (CartanClass->)

print_block: (Block->):
print_blocku: (Block->):
print_blockd: (Block->):
print_blockstabilizer: (Block,CartanClass->):
print_KGB: (RealForm->):
print_X: (InnerClass->):
print_KL_basis: (Block->):
print_prim_KL: (Block->):
print_KL_list: (Block->):
print_W_cells: (Block->):
print_W_graph: (Block->):

These commands give the output of the corresponding commands of 'atlas'.