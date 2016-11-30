.. _parabolics.at_ref:

parabolics.at Function References
=======================================================
|

.. _sort_by_(kgbelt_->_int)_f->([kgbelt]_v)_[kgbelt]1:

sort_by
-------------------------------------------------
| ``sort_by:(KGBElt -> int) f->([KGBElt] v) [KGBElt]`` Defined in line number 60.
| 
| Given a list of KGB elements and a function f assigning integers to them, sort the list by weakly increasing value of f.
| 

.. _kgp_elt_kgpelt_pair->kgpelt1:

KGP_elt
-------------------------------------------------
| ``KGP_elt:KGPElt pair->KGPElt`` Defined in line number 74.
| 
| 

.. _s_kgpelt(s,)->[int]1:

S
-------------------------------------------------
| ``S:KGPElt(S,)->[int]`` Defined in line number 77.
| 
| The list S of simple roots of a KGP element.
| 

.. _root_datum_kgpelt(,x)->rootdatum1:

root_datum
-------------------------------------------------
| ``root_datum:KGPElt(,x)->RootDatum`` Defined in line number 80.
| 
| The root datum of the RealForm G of a KGP element.
| 

.. _real_form_kgpelt(,x)->realform1:

real_form
-------------------------------------------------
| ``real_form:KGPElt(,x)->RealForm`` Defined in line number 83.
| 
| The RealForm G of a KGP element.
| 

.. _complement_int_n,[int]_s->[int]1:

complement
-------------------------------------------------
| ``complement:int n,[int] S->[int]`` Defined in line number 86.
| 
| Complement of subset of simple roots in rank n.
| 

.. _find_ascent_[int]_s,_kgbelt_x->[kgbelt]1:

find_ascent
-------------------------------------------------
| ``find_ascent:[int] S, KGBElt x->[KGBElt]`` Defined in line number 90.
| 
| An ascent of x by a generator in S, if any exist.
| 

.. _down_neighbors_[int]_s,kgbelt_x->[int]1:

down_neighbors
-------------------------------------------------
| ``down_neighbors:[int] S,KGBElt x->[int]`` Defined in line number 98.
| 
| All descents of x by generators in S; there may be duplicates.
| 

.. _is_maximal_in_partial_order_[int]_s,kgbelt_x->bool1:

is_maximal_in_partial_order
-------------------------------------------------
| ``is_maximal_in_partial_order:[int] S,KGBElt x->bool`` Defined in line number 109.
| 
| Decide whether x is maximal in the partial order defined by S.
| 

.. _maxima_in_partial_order_realform_g,[int]_s->[kgbelt]1:

maxima_in_partial_order
-------------------------------------------------
| ``maxima_in_partial_order:RealForm G,[int] S->[KGBElt]`` Defined in line number 112.
| 
| List maximal KGB elements in the partial order defined by S.
| 

.. _maximal_[int]_s,_kgbelt_x->kgbelt1:

maximal
-------------------------------------------------
| ``maximal:[int] S, KGBElt x->KGBElt`` Defined in line number 118.
| 
| (Unique) maximal element in equivalence class of x.
| 

.. _canonical_representative_kgpelt_y->kgpelt1:

canonical_representative
-------------------------------------------------
| ``canonical_representative:KGPElt y->KGPElt`` Defined in line number 123.
| 
| The representative of a KGP element with maximal x.
| 

.. _\=_KGPElt_(S,x),KGPElt_(T,y)->bool1:

\=
-------------------------------------------------
| ``=:KGPElt (S,x),KGPElt (T,y)->bool`` Defined in line number 130.
| 
| Equality of KGP elements: (S,x)=(T,y) if these give the same K-orbit of parabolics.
| 

.. _equivalence_class_of_kgpelt(s,x):y->[kgbelt]1:

equivalence_class_of
-------------------------------------------------
| ``equivalence_class_of:KGPElt(S,x):y->[KGBElt]`` Defined in line number 134.
| 
| The equivalence class of a KGB element in partial order defined by S.
| 

.. _x_min_kgpelt_p->kgbelt1:

x_min
-------------------------------------------------
| ``x_min:KGPElt P->KGBElt`` Defined in line number 148.
| 
| A minimal KGB element from an equivalence class defined by S (unlike x_max, it is not unique).
| 

.. _kgp_realform_g,[int]_s->[kgpelt]1:

KGP
-------------------------------------------------
| ``KGP:RealForm G,[int] S->[KGPElt]`` Defined in line number 153.
| 
| The set of KGP elements associated to a RealForm and a set of simple roots S; KGP(G,S) is in bijection with :math:`K\backslash G/P_S` .
| 

.. _kgp_numbers_realform_g,[int]_s->[int]1:

KGP_numbers
-------------------------------------------------
| ``KGP_numbers:RealForm G,[int] S->[int]`` Defined in line number 157.
| 
| Just the index numbers (maximal x) of KGP(G,S).
| 

.. _is_open_kgpelt_y->bool1:

is_open
-------------------------------------------------
| ``is_open:KGPElt y->bool`` Defined in line number 161.
| 
| Test whether y in :math:`K\backslash G/P_S`  is open: <=> last element of y is last element of KGB.
| 

.. _is_closed_kgpelt_p->bool1:

is_closed
-------------------------------------------------
| ``is_closed:KGPElt P->bool`` Defined in line number 164.
| 
| Test whether y in :math:`K\backslash G/P_S`  is closed: <=> length(first element)=0.
| 

.. _kgp_elt_ratvec_lambda,kgbelt_x->kgpelt1:

KGP_elt
-------------------------------------------------
| ``KGP_elt:ratvec lambda,KGBElt x->KGPElt`` Defined in line number 167.
| 
| Parabolic determined by (the stabilizer in W of) a weight lambda.
| 

.. _complex_parabolic_parabolic(s,x)->complexparabolic1:

complex_parabolic
-------------------------------------------------
| ``complex_parabolic:Parabolic(S,x)->ComplexParabolic`` Defined in line number 177.
| 
| The complex parabolic underlying P=(S,x).
| 

.. _complex_levi_rootdatum_rd,_(int->bool)_select->rootdatum1:

complex_Levi
-------------------------------------------------
| ``complex_Levi:RootDatum rd, (int->bool) select->RootDatum`` Defined in line number 180.
| 
| Auxiliary function
| 

.. _is_levi_theta_stable_parabolic_(s,x)->bool1:

is_Levi_theta_stable
-------------------------------------------------
| ``is_Levi_theta_stable:Parabolic (S,x)->bool`` Defined in line number 190.
| 
| Test if a complex Levi defined by a set of simple roots S is :math:`\theta_x` -stable;   algorithm: H=sum of fundamental coweights with index not in S,   test whether :math:`<\theta_x(\alpha),H>=0`  for all :math:`\alpha`  in S.
| 

.. _levi_parabolic(s,x):p->realform1:

Levi
-------------------------------------------------
| ``Levi:Parabolic(S,x):P->RealForm`` Defined in line number 202.
| 
| Make a real Levi factor from P=(S,x); the complex Levi of S must be theta-stable.
| 

.. _is_parabolic_theta_stable_parabolic_(s,x):p->bool1:

is_parabolic_theta_stable
-------------------------------------------------
| ``is_parabolic_theta_stable:Parabolic (S,x):P->bool`` Defined in line number 211.
| 
| Test if parabolic P=(S,x) is theta-stable: <=>    the complex Levi factor L is theta-stable, P is closed, and for    alpha simple, not in S => alpha is imaginary or C+ wrt maximal(P).
| 

.. _is_parabolic_real_parabolic_(s,x):p->bool1:

is_parabolic_real
-------------------------------------------------
| ``is_parabolic_real:Parabolic (S,x):P->bool`` Defined in line number 222.
| 
| Test if parabolic P=(S,x) is real: <=> L is theta-stable, P is open, and    for alpha simple, not in S => alpha is real or C- wrt a maximal(P).
| 

.. _rho_u_complexparabolic_p->ratvec1:

rho_u
-------------------------------------------------
| ``rho_u:ComplexParabolic P->ratvec`` Defined in line number 243.
| 
| Half sum of positive roots not in the Levi (L must be theta-stable).
| 

.. _rho_u_parabolic_p->ratvec1:

rho_u
-------------------------------------------------
| ``rho_u:Parabolic P->ratvec`` Defined in line number 246.
| 
| Half sum of positive roots not in the Levi (L must be theta-stable).
| 

.. _rho_l_parabolic_p->ratvec1:

rho_l
-------------------------------------------------
| ``rho_l:Parabolic P->ratvec`` Defined in line number 249.
| 
| Half sum of positive roots in the Levi (L must be theta-stable).
| 

.. _nilrad_parabolic_p->mat1:

nilrad
-------------------------------------------------
| ``nilrad:Parabolic P->mat`` Defined in line number 252.
| 
| Positive coroots in the nilradical u of P (L must be theta-stable).
| 

.. _nilrad_roots_parabolic_p->mat1:

nilrad_roots
-------------------------------------------------
| ``nilrad_roots:Parabolic P->mat`` Defined in line number 257.
| 
| Positive roots in the nilradical u of P (L must be theta-stable).
| 

.. _zero_simple_coroots_rootdatum_rd,_vec_lambda->[int]1:

zero_simple_coroots
-------------------------------------------------
| ``zero_simple_coroots:RootDatum rd, vec lambda->[int]`` Defined in line number 270.
| 
| Simple coroots on which weight lambda (in :math:`\mathfrak h^*` ) is zero.
| 

.. _parabolic_ratvec_lambda,kgbelt_x->parabolic1:

parabolic
-------------------------------------------------
| ``parabolic:ratvec lambda,KGBElt x->Parabolic`` Defined in line number 276.
| 
| Parabolic defined by weight lambda.
| 

.. _levi_ratvec_lambda,kgbelt_x->realform1:

Levi
-------------------------------------------------
| ``Levi:ratvec lambda,KGBElt x->RealForm`` Defined in line number 281.
| 
| Levi factor of parabolic defined by weight lambda.
| 

.. _nilrad_ratvec_lambda,kgbelt_x->mat1:

nilrad
-------------------------------------------------
| ``nilrad:ratvec lambda,KGBElt x->mat`` Defined in line number 284.
| 
| Positive coroots in nilradical of P defined by weight lambda (if L theta-stable).
| 

.. _nilrad_roots_ratvec_lambda,kgbelt_x->mat1:

nilrad_roots
-------------------------------------------------
| ``nilrad_roots:ratvec lambda,KGBElt x->mat`` Defined in line number 287.
| 
| Positive roots in nilradical of P defined by weight lambda (if L theta-stable).
| 

.. _rho_u_ratvec_lambda,kgbelt_x->ratvec1:

rho_u
-------------------------------------------------
| ``rho_u:ratvec lambda,KGBElt x->ratvec`` Defined in line number 292.
| 
| Half sum of positive roots in nilradical of P defined by weight lambda (if L theta-stable).
| 

.. _zero_simple_roots_rootdatum_rd,_vec_cowt->[int]1:

zero_simple_roots
-------------------------------------------------
| ``zero_simple_roots:RootDatum rd, vec cowt->[int]`` Defined in line number 295.
| 
| Simple roots which are zero on coweight H (in :math:`\mathfrak h` ).
| 

.. _parabolic_alt_ratvec_h,kgbelt_x->parabolic1:

parabolic_alt
-------------------------------------------------
| ``parabolic_alt:ratvec H,KGBElt x->Parabolic`` Defined in line number 301.
| 
| Parabolic defined by coweight H.
| 

.. _levi_alt_ratvec_h,kgbelt_x->realform1:

Levi_alt
-------------------------------------------------
| ``Levi_alt:ratvec H,KGBElt x->RealForm`` Defined in line number 306.
| 
| Levi factor of parabolic defined by coweight H.
| 

.. _nilrad_alt_ratvec_h,kgbelt_x->mat1:

nilrad_alt
-------------------------------------------------
| ``nilrad_alt:ratvec H,KGBElt x->mat`` Defined in line number 309.
| 
| Positive coroots in nilradical of P defined by coweight H (if L theta-stable).
| 

.. _nilrad_roots_alt_ratvec_h,kgbelt_x->mat1:

nilrad_roots_alt
-------------------------------------------------
| ``nilrad_roots_alt:ratvec H,KGBElt x->mat`` Defined in line number 312.
| 
| Positive roots in nilradical of P defined by coweight H (if L theta-stable).
| 

.. _rho_u_alt_ratvec_h,kgbelt_x->ratvec1:

rho_u_alt
-------------------------------------------------
| ``rho_u_alt:ratvec H,KGBElt x->ratvec`` Defined in line number 316.
| 
| Half sum of roots in nilradical of P defined by coweight H (if L theta-stable).
| 

.. _rho_levi_alt_ratvec_h,kgbelt_x->ratvec1:

rho_Levi_alt
-------------------------------------------------
| ``rho_Levi_alt:ratvec H,KGBElt x->ratvec`` Defined in line number 319.
| 
|  :math:`\rho(L)`  for Levi of P defined by coweight H (if L theta-stable).
| 

.. _real_parabolic_kgbelt_x->parabolic1:

real_parabolic
-------------------------------------------------
| ``real_parabolic:KGBElt x->Parabolic`` Defined in line number 328.
| 
| Real parabolic defined by x has Levi factor M=centralizer(A),   :math:`\mathfrak u` =positive roots not in M;   for M to be stable: x must have no C+ roots.
| 

.. _theta_stable_parabolic_kgbelt_x->parabolic1:

theta_stable_parabolic
-------------------------------------------------
| ``theta_stable_parabolic:KGBElt x->Parabolic`` Defined in line number 337.
| 
| Theta-stable parabolic defined by x has Levi factor L=centralizer(T),   :math:`\mathfrak u` =positive roots not in L;   for this to be stable: no C- roots.
| 

.. _real_levi_kgbelt_x->realform1:

real_Levi
-------------------------------------------------
| ``real_Levi:KGBElt x->RealForm`` Defined in line number 345.
| 
| Levi factor of real cuspidal parabolic;  M=centralizer of A in H=TA, as a RealForm.
| 

.. _is_standard_levi_realform_l,realform_g->bool1:

is_standard_Levi
-------------------------------------------------
| ``is_standard_Levi:RealForm L,RealForm G->bool`` Defined in line number 403.
| 
| Check whether a Levi subgroup L is standard in G   (simple roots of L are simple for G).
| 

.. _kgp_realform_g,complexparabolic_(rd,s)->[kgpelt]1:

KGP
-------------------------------------------------
| ``KGP:RealForm G,ComplexParabolic (rd,S)->[KGPElt]`` Defined in line number 412.
| 
| List of K-conjugacy classes of given ComplexParabolic (as KGP elts).
| 

.. _parabolics_realform_g,complexparabolic_(rd,s)->[parabolic]1:

parabolics
-------------------------------------------------
| ``parabolics:RealForm G,ComplexParabolic (rd,S)->[Parabolic]`` Defined in line number 416.
| 
| List K-conjugacy classes of given ComplexParabolic (as Parabolics).
| 

.. _theta_stable_parabolics_realform_g,complexparabolic_p->[parabolic]1:

theta_stable_parabolics
-------------------------------------------------
| ``theta_stable_parabolics:RealForm G,ComplexParabolic P->[Parabolic]`` Defined in line number 420.
| 
| List K-conjugacy classes of given ComplexParabolic that are theta-stable.
| 

.. _theta_stable_parabolics_realform_g->[parabolic]1:

theta_stable_parabolics
-------------------------------------------------
| ``theta_stable_parabolics:RealForm G->[Parabolic]`` Defined in line number 426.
| 
| List all theta-stable parabolics for G.
| 

.. _theta_stable_parabolics_type_realform_g,[int]_p->[parabolic]1:

theta_stable_parabolics_type
-------------------------------------------------
| ``theta_stable_parabolics_type:RealForm G,[int] P->[Parabolic]`` Defined in line number 433.
| 
| List all theta-stable parabolics of G, of type S.
| 

.. _all_rel_split_theta_stable_parabolics_realform_g->[parabolic]1:

all_rel_split_theta_stable_parabolics
-------------------------------------------------
| ``all_rel_split_theta_stable_parabolics:RealForm G->[Parabolic]`` Defined in line number 439.
| 
| List all theta-stable parabolics of G with relatively split L.
| 

.. _print_theta_stable_parabolics_realform_g->void1:

print_theta_stable_parabolics
-------------------------------------------------
| ``print_theta_stable_parabolics:RealForm G->void`` Defined in line number 447.
| 
| For each theta-stable parabolic of G, print S, Levi factor, and maximal x.
| 

.. _KGPElt1:

KGPElt
----------------------------------------
| ``([int], KGBElt)`` Defined in line number 53.
| 
| Data type for a K_orbit on G/P_S, equivalently a K-conjugacy class of    parabolics of type S.
| 

.. _Parabolic1:

Parabolic
----------------------------------------
| ``([int], KGBElt)`` Defined in line number 56.
| 
| Data type for a K_orbit on G/P_S (synonym for KGPElt).
| 

.. _ComplexParabolic1:

ComplexParabolic
----------------------------------------
| ``(RootDatum,[int])`` Defined in line number 174.
| 
| Data type for a complex parabolic subrgoup
| 

