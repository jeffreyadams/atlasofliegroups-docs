Parameter, KL, print, etc.
---------------------------

.. list-table::
   :widths: 10 20
   :header-rows: 1
   
   * - Function
     - Argument(s) -> Result(s)
   * - :ref:`param2`
     - ``(KGBElt,vec,ratvec->Param)``
   * - :ref:`operator_%4`
     - ``(Param->KGBElt,vec,ratvec)``
   * - :ref:`real_form3`
     - ``(Param->RealForm)``
   * - :ref:`infinitesimal_character`
     - ``(Param->ratvec)``
   * - :ref:`is_standard`
     - ``(Param->bool)``
   * - :ref:`is_zero`
     - ``(Param->bool)``
   * - :ref:`is_final`
     - ``(Param->bool)``
   * - :ref:`dominant`
     - ``(Param->Param)``
   * - :ref:`operator_=4`
     - ``(Param,Param->bool)``
   * - :ref:`cross2`
     - ``(int,Param->Param)``
   * - :ref:`Cayley2`
     - ``(int,Param->Param)``
   * - :ref:`inv_Cayley`
     - ``(int,Param->Param)``
   * - :ref:`cross3`
     - ``(vec,Param->Param)``
   * - :ref:`Cayley3`
     - ``(vec,Param->Param)``
   * - :ref:`twist2`
     - ``(Param->Param)``
   * - :ref:`orientation_nr`
     - ``(Param->int)``
   * - :ref:`reducibility_points`
     - ``(Param->[rat])``
   * - :ref:`print_block`
     - ``(Param->)``
   * - :ref:`block3`
     - ``(Param->[Param],int)``
   * - :ref:`partial_block` 
     - ``(Param->[Param])``
   * - :ref:`length2`
     - ``(Param->int)``
   * - :ref:`KL_block`
     - ``(Param->[Param],int,mat,[vec],vec,vec,mat)``
   * - :ref:`partial_KL_block`
     - ``(Param->[Param],mat,[vec],vec,vec,mat)``

.. _param2:

param
++++++

    ``(KGBElt,vec,ratvec->Param)``: form parameter from (x,lambda-rho,nu)

.. _operator_%4:

\%
++++++

    ``(Param->KGBElt,vec,ratvec)``: recover (x,lambda-rho,nu) from param

.. _real_form3:

real_form
+++++++++++

    ``(Param->RealForm)``: recover the real form from a Param value

.. _infinitesimal_character:

infinitesimal_character
+++++++++++++++++++++++++++

    ``(Param->ratvec)``: infinitesimal character of parameter

    This is actually a representative of the infinitesimal character, given by gamma = ((1+theta)lambda+(1-theta)nu)/2. The meaning of the x component of the parameter is determined by its position relative to this representative gamma, so to find the x value uniquely associated to the representation for the parameter, one should apply the function 'dominant' to the parameter first, after which the value of infinitesimal_character is indeed dominant
  
.. _is_standard:

is_standard
+++++++++++++++

    ``(Param->bool)``: whether parameter defines a standard module

    This is true whenever gamma is dominant relative to the imaginary roots
  
.. _is_zero:

is_zero
++++++++++

    ``(Param->bool)``: whether parameter defines a zero standard module

    True whenever gamma is singular on a compact (for x) simple-imaginary root
  
.. _is_final:

is_final
+++++++++++++

    ``(Param->bool)``: whether parameter defines a final standard module

    False whenever associated standard representation is combination of others on more compact Cartans by a Hecht-Schmid identity. So is_final(p) is true provided no real coroots for which gamma is singular satisfy the parity condition. Note: one could still have is_zero(p); this needs a separate test.
  
.. _dominant:

dominant
+++++++++++

    ``(Param->Param)``: make gamma dominant and do singular complex descents

    This brings the parameter p into standard form, in which it will appear when p occurs in a ParamPol (which also requires is_final(p) and not is_zero(p)).
  
.. _operator_=4:

\=
+++++

    ``(Param,Param->bool)``: test equivalence of parameters

    This is implemented by applying dominant and testing identity of all three components x, lambda (defined modulo (1-theta_x)X^*) and nu.
  
.. _cross2:

cross
+++++++++

    ``(int,Param->Param)``: cross action for (Weyl group generator,parameter)

    This first argument indexes (starting at 0) a simple root for the subsystem for the given parameter p: integrality_datum(infinitesimal_character(p))
  
.. _Cayley2:

Cayley
+++++++++++

    ``(int,Param->Param)``: Cayley transform for (Weyl generator,parameter)

    If (and only if) the transform is undefined it returns the same parameter Find out possible second value by applying cross action to the result
  
.. _inv_Cayley:

inv_Cayley
++++++++++++++

    ``(int,Param->Param)``: inverse Cayley transform

    If (and only if) the inverse transform is undefined it returns the same parameter. Find out possible second value of invere transform by applying cross action to the result, which either produces it or else fixes result
  
.. _cross3:

cross
+++++++++

    ``(vec,Param->Param)``: cross action for (root,parameter)

.. _Cayley3:

Cayley
++++++++++

    ``(vec,Param->Param)``: Cayley transform for (root,parameter)

    These two functions should do the same as the three before, but taking the root in coordinates, and combining the Cayley/inverse Cayley into one function (whichever is defined is applied, or else the parameter returned). The implementation is quite independent however, so comparison is useful.

.. _twist2:

twist
+++++++++

    ``(Param->Param)``: twist the parameter by the distinguihed involution

.. _orientation_nr:

orientation_nr
++++++++++++++++

    ``(Param->int)``: the orientation number

.. _reducibility_points:

reducibility_points
++++++++++++++++++++++++

    ``(Param->[rat])``: the :math:`0<t<=1` with :math:`I(x,lambda,t\nu)` reducible

.. _print_block:

print_block
++++++++++++++

    ``(Param->)``: print (nonintegral) block generated from parameter

.. _block3:

block
+++++++++

    ``(Param->[Param],int)``: return block as list of parameters, and index

    The second component is the index into the first of the original parameter.

.. _partial_block:

partial_block
++++++++++++++++

    ``(Param->[Param])``: return partial block as list of parameters

    This is the Bruhat interval of the block below the given parameter, sorted by length and including the given parameter as final element

.. _length2:

length
++++++++++

    ``(Param->int)``: the length of a parameter within its block

.. _KL_block:

KL_block
++++++++++++++

    ``(Param->[Param],int,mat,[vec],vec,vec,mat)``: block, raw_KL, and more

    This combines block with the Kazhdan-Lustzig table for the block appended, and two more values that allow cumulation to be performed. The two values of block are followed by three values in the format of raw_KL below: a matrix of indices into the following list of polynomials, coded as a list of coefficient vectors, then a list of indices where the length function increases. Finally follow a vector with indices of the "surviving" block elements, and a matrix whose rows correspond to those survivors, its columns to all block elements, and whose the entries gives the coefficients by which each the block element (column) contributes to the surviving element (row), with a sign given by the parity of their length difference. Here "surviving" refers to the result of applying a translation functor to a standard module, namely a functor from regular infinitesimal character to the current (possibly) singular infinitesimal character. Thus one can transform the given KL matrix (computed at regular infinitesimal character) to one at the actual block by selecting only the columns whose index is among the survivors, and multiplying the resulting matrix on the left by the contibution-coefficient matrix (the final component this function returns).

.. _partial_KL_block:

partial_KL_block
++++++++++++++++++

    ``(Param->[Param],mat,[vec],vec,vec,mat)`` partial KL_block

    This function relates to KL_block as partial_block relates to block. The first component of the result is the Bruhat interval as in partial_block, and all other components are the same is in KL_block (except that the now superfluous second component of KL_block is omitted), but with the two vec components filtered so as to be indexed by the Bruhat interval indices only.




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