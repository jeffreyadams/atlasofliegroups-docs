.. _parabolics.at_ref:

parabolics.at Function References
=======================================================
|

.. _sort_by_(kgbelt_->_int)_f->([kgbelt]_v)_[kgbelt]1:

sort_by
-------------------------------------------------
| ``sort_by:(KGBElt -> int) f->([KGBElt] v) [KGBElt]`` Defined in line number 61.
| 
| Given a list of KGB elements and a function f assigning integers to them, sort the list by weakly increasing value of f.
| 

.. _kgp_elt_kgpelt_pair->kgpelt1:

KGP_elt
-------------------------------------------------
| ``KGP_elt:KGPElt pair->KGPElt`` Defined in line number 75.
| 
| 

.. _s_kgpelt(s,)->[int]1:

S
-------------------------------------------------
| ``S:KGPElt(S,)->[int]`` Defined in line number 78.
| 
| The list S of simple roots of a KGP element.
| 

.. _root_datum_kgpelt(,x)->rootdatum1:

root_datum
-------------------------------------------------
| ``root_datum:KGPElt(,x)->RootDatum`` Defined in line number 81.
| 
| The root datum of the RealForm G of a KGP element.
| 

.. _real_form_kgpelt(,x)->realform1:

real_form
-------------------------------------------------
| ``real_form:KGPElt(,x)->RealForm`` Defined in line number 84.
| 
| The RealForm G of a KGP element.
| 

.. _complement_int_n,[int]_s->[int]1:

complement
-------------------------------------------------
| ``complement:int n,[int] S->[int]`` Defined in line number 87.
| 
| Complement of subset of simple roots in rank n.
| 

.. _find_ascent_[int]_s,_kgbelt_x->[kgbelt]1:

find_ascent
-------------------------------------------------
| ``find_ascent:[int] S, KGBElt x->[KGBElt]`` Defined in line number 91.
| 
| An ascent of x by a generator in S, if any exist.
| 

.. _down_neighbors_[int]_s,kgbelt_x->[int]1:

down_neighbors
-------------------------------------------------
| ``down_neighbors:[int] S,KGBElt x->[int]`` Defined in line number 99.
| 
| All descents of x by generators in S; there may be duplicates.
| 

.. _is_maximal_in_partial_order_[int]_s,kgbelt_x->bool1:

is_maximal_in_partial_order
-------------------------------------------------
| ``is_maximal_in_partial_order:[int] S,KGBElt x->bool`` Defined in line number 110.
| 
| Decide whether x is maximal in the partial order defined by S.
| 

.. _maxima_in_partial_order_realform_g,[int]_s->[kgbelt]1:

maxima_in_partial_order
-------------------------------------------------
| ``maxima_in_partial_order:RealForm G,[int] S->[KGBElt]`` Defined in line number 113.
| 
| List maximal KGB elements in the partial order defined by S.
| 

.. _maximal_[int]_s,_kgbelt_x->kgbelt1:

maximal
-------------------------------------------------
| ``maximal:[int] S, KGBElt x->KGBElt`` Defined in line number 119.
| 
| (Unique) maximal element in equivalence class of x.
| 

.. _canonical_representative_kgpelt_y->kgpelt1:

canonical_representative
-------------------------------------------------
| ``canonical_representative:KGPElt y->KGPElt`` Defined in line number 124.
| 
| The representative of a KGP element with maximal x.
| 

.. _\=_KGPElt_(S,x),KGPElt_(T,y)->bool1:

\=
-------------------------------------------------
| ``=:KGPElt (S,x),KGPElt (T,y)->bool`` Defined in line number 131.
| 
| Equality of KGP elements: (S,x)=(T,y) if these give the same K-orbit of parabolics.
| 

.. _equivalence_class_of_kgpelt(s,x)->[kgbelt]1:

equivalence_class_of
-------------------------------------------------
| ``equivalence_class_of:KGPElt(S,x)->[KGBElt]`` Defined in line number 135.
| 
| The equivalence class of a KGB element in partial order defined by S.
| 

.. _rec_fun x_min_kgpelt_p->kgbelt1:

rec_fun x_min
-------------------------------------------------
| ``rec_fun x_min:KGPElt P->KGBElt`` Defined in line number 149.
| 
| A minimal KGB element from an equivalence class defined by S    (unlike x_max, it is not unique).
| 

.. _kgp_realform_g,[int]_s->[kgpelt]1:

KGP
-------------------------------------------------
| ``KGP:RealForm G,[int] S->[KGPElt]`` Defined in line number 155.
| 
| The set of KGP elements associated to a RealForm and a set of simple roots S; KGP(G,S) is in bijection with :math:`K\backslash G/P_S` .
| 

.. _kgp_numbers_realform_g,[int]_s->[int]1:

KGP_numbers
-------------------------------------------------
| ``KGP_numbers:RealForm G,[int] S->[int]`` Defined in line number 159.
| 
| Just the index numbers (maximal x) of KGP(G,S).
| 

.. _is_open_kgpelt_y->bool1:

is_open
-------------------------------------------------
| ``is_open:KGPElt y->bool`` Defined in line number 163.
| 
| Test whether y in :math:`K\backslash G/P_S`  is open: <=> last element of y is last element of KGB.
| 

.. _is_closed_kgpelt_p->bool1:

is_closed
-------------------------------------------------
| ``is_closed:KGPElt P->bool`` Defined in line number 166.
| 
| Test whether y in :math:`K\backslash G/P_S`  is closed: <=> length(first element)=0.
| 

.. _kgp_elt_ratvec_lambda,kgbelt_x->kgpelt1:

KGP_elt
-------------------------------------------------
| ``KGP_elt:ratvec lambda,KGBElt x->KGPElt`` Defined in line number 169.
| 
| Parabolic determined by (the stabilizer in W of) a weight lambda.
| 

.. _complex_parabolic_parabolic(s,x)->complexparabolic1:

complex_parabolic
-------------------------------------------------
| ``complex_parabolic:Parabolic(S,x)->ComplexParabolic`` Defined in line number 179.
| 
| The complex parabolic underlying P=(S,x).
| 

.. _complex_levi_rootdatum_rd,_(int->bool)_select->rootdatum1:

complex_Levi
-------------------------------------------------
| ``complex_Levi:RootDatum rd, (int->bool) select->RootDatum`` Defined in line number 182.
| 
| Auxiliary function
| 

.. _is_levi_theta_stable_parabolic_(s,x)->bool1:

is_Levi_theta_stable
-------------------------------------------------
| ``is_Levi_theta_stable:Parabolic (S,x)->bool`` Defined in line number 192.
| 
| Test if a complex Levi defined by a set of simple roots S is :math:`\theta_x` -stable;   algorithm: H=sum of fundamental coweights with index not in S,   test whether :math:`<\theta_x(\alpha),H>=0`  for all :math:`\alpha`  in S.
| 

.. _levi_parabolic(s,x):p->realform1:

Levi
-------------------------------------------------
| ``Levi:Parabolic(S,x):P->RealForm`` Defined in line number 204.
| 
| Make a real Levi factor from P=(S,x); the complex Levi of S must be theta-stable.
| 

.. _is_parabolic_theta_stable_parabolic_(s,x):p->bool1:

is_parabolic_theta_stable
-------------------------------------------------
| ``is_parabolic_theta_stable:Parabolic (S,x):P->bool`` Defined in line number 213.
| 
| Test if parabolic P=(S,x) is theta-stable: <=>    the complex Levi factor L is theta-stable, P is closed, and for    alpha simple, not in S => alpha is imaginary or C+ wrt maximal(P).
| 

.. _is_parabolic_real_parabolic_(s,x):p->bool1:

is_parabolic_real
-------------------------------------------------
| ``is_parabolic_real:Parabolic (S,x):P->bool`` Defined in line number 224.
| 
| Test if parabolic P=(S,x) is real: <=> L is theta-stable, P is open, and    for alpha simple, not in S => alpha is real or C- wrt a maximal(P).
| 

.. _rho_u_complexparabolic_p->ratvec1:

rho_u
-------------------------------------------------
| ``rho_u:ComplexParabolic P->ratvec`` Defined in line number 245.
| 
| Half sum of positive roots not in the Levi (L must be theta-stable).
| 

.. _rho_u_parabolic_p->ratvec1:

rho_u
-------------------------------------------------
| ``rho_u:Parabolic P->ratvec`` Defined in line number 248.
| 
| Half sum of positive roots not in the Levi (L must be theta-stable).
| 

.. _rho_l_parabolic_p->ratvec1:

rho_l
-------------------------------------------------
| ``rho_l:Parabolic P->ratvec`` Defined in line number 251.
| 
| Half sum of positive roots in the Levi (L must be theta-stable).
| 

.. _nilrad_parabolic_p->mat1:

nilrad
-------------------------------------------------
| ``nilrad:Parabolic P->mat`` Defined in line number 254.
| 
| Positive coroots in the nilradical u of P (L must be theta-stable).
| 

.. _nilrad_roots_parabolic_p->mat1:

nilrad_roots
-------------------------------------------------
| ``nilrad_roots:Parabolic P->mat`` Defined in line number 259.
| 
| Positive roots in the nilradical u of P (L must be theta-stable).
| 

.. _zero_simple_coroots_rootdatum_rd,_vec_lambda->[int]1:

zero_simple_coroots
-------------------------------------------------
| ``zero_simple_coroots:RootDatum rd, vec lambda->[int]`` Defined in line number 272.
| 
| Simple coroots on which weight lambda (in :math:`\mathfrak h^*` ) is zero.
| 

.. _parabolic_ratvec_lambda,kgbelt_x->parabolic1:

parabolic
-------------------------------------------------
| ``parabolic:ratvec lambda,KGBElt x->Parabolic`` Defined in line number 279.
| 
| Parabolic defined by weight lambda; message whether parabolic is real   or theta-stable.
| 

.. _parabolic_mute_ratvec_lambda,kgbelt_x->parabolic1:

parabolic_mute
-------------------------------------------------
| ``parabolic_mute:ratvec lambda,KGBElt x->Parabolic`` Defined in line number 290.
| 
| Parabolic defined by weight lambda; NO message whether parabolic is real   or theta-stable.
| 

.. _theta_stable_parabolic_ratvec_lambda,kgbelt_x->parabolic1:

theta_stable_parabolic
-------------------------------------------------
| ``theta_stable_parabolic:ratvec lambda,KGBElt x->Parabolic`` Defined in line number 297.
| 
| Theta-stable parabolic defined by weight lambda.
| 

.. _real_parabolic_ratvec_lambda,kgbelt_x->parabolic1:

real_parabolic
-------------------------------------------------
| ``real_parabolic:ratvec lambda,KGBElt x->Parabolic`` Defined in line number 301.
| 
| Real parabolic defined by weight lambda.
| 

.. _levi_ratvec_lambda,kgbelt_x->realform1:

Levi
-------------------------------------------------
| ``Levi:ratvec lambda,KGBElt x->RealForm`` Defined in line number 305.
| 
| Levi factor of parabolic defined by weight lambda.
| 

.. _theta_stable_levi_ratvec_lambda,_kgbelt_x->realform1:

theta_stable_Levi
-------------------------------------------------
| ``theta_stable_Levi:ratvec lambda, KGBElt x->RealForm`` Defined in line number 308.
| 
| Levi factor of theta-stable parabolic defined by weight lambda.
| 

.. _real_levi_ratvec_lambda,_kgbelt_x->realform1:

real_Levi
-------------------------------------------------
| ``real_Levi:ratvec lambda, KGBElt x->RealForm`` Defined in line number 312.
| 
| Levi factor of real parabolic defined by weight lambda.
| 

.. _nilrad_ratvec_lambda,kgbelt_x->mat1:

nilrad
-------------------------------------------------
| ``nilrad:ratvec lambda,KGBElt x->mat`` Defined in line number 316.
| 
| Positive coroots in nilradical of P defined by weight lambda (if L theta-stable).
| 

.. _nilrad_roots_ratvec_lambda,kgbelt_x->mat1:

nilrad_roots
-------------------------------------------------
| ``nilrad_roots:ratvec lambda,KGBElt x->mat`` Defined in line number 319.
| 
| Positive roots in nilradical of P defined by weight lambda (if L theta-stable).
| 

.. _rho_u_ratvec_lambda,kgbelt_x->ratvec1:

rho_u
-------------------------------------------------
| ``rho_u:ratvec lambda,KGBElt x->ratvec`` Defined in line number 324.
| 
| Half sum of positive roots in nilradical of P defined by weight lambda (if L theta-stable).
| 

.. _zero_simple_roots_rootdatum_rd,_vec_cowt->[int]1:

zero_simple_roots
-------------------------------------------------
| ``zero_simple_roots:RootDatum rd, vec cowt->[int]`` Defined in line number 327.
| 
| Simple roots which are zero on coweight H (in :math:`\mathfrak h` ).
| 

.. _parabolic_alt_ratvec_h,kgbelt_x->parabolic1:

parabolic_alt
-------------------------------------------------
| ``parabolic_alt:ratvec H,KGBElt x->Parabolic`` Defined in line number 334.
| 
| Parabolic defined by coweight H; message whether parabolic is real    or theta-stable.
| 

.. _levi_alt_ratvec_h,kgbelt_x->realform1:

Levi_alt
-------------------------------------------------
| ``Levi_alt:ratvec H,KGBElt x->RealForm`` Defined in line number 344.
| 
| Levi factor of parabolic defined by coweight H.
| 

.. _nilrad_alt_ratvec_h,kgbelt_x->mat1:

nilrad_alt
-------------------------------------------------
| ``nilrad_alt:ratvec H,KGBElt x->mat`` Defined in line number 347.
| 
| Positive coroots in nilradical of P defined by coweight H (if L theta-stable).
| 

.. _nilrad_roots_alt_ratvec_h,kgbelt_x->mat1:

nilrad_roots_alt
-------------------------------------------------
| ``nilrad_roots_alt:ratvec H,KGBElt x->mat`` Defined in line number 350.
| 
| Positive roots in nilradical of P defined by coweight H (if L theta-stable).
| 

.. _rho_u_alt_ratvec_h,kgbelt_x->ratvec1:

rho_u_alt
-------------------------------------------------
| ``rho_u_alt:ratvec H,KGBElt x->ratvec`` Defined in line number 354.
| 
| Half sum of roots in nilradical of P defined by coweight H (if L theta-stable).
| 

.. _rho_levi_alt_ratvec_h,kgbelt_x->ratvec1:

rho_Levi_alt
-------------------------------------------------
| ``rho_Levi_alt:ratvec H,KGBElt x->ratvec`` Defined in line number 357.
| 
|  :math:`\rho(L)`  for Levi of P defined by coweight H (if L theta-stable).
| 

.. _real_parabolic_kgbelt_x->parabolic1:

real_parabolic
-------------------------------------------------
| ``real_parabolic:KGBElt x->Parabolic`` Defined in line number 365.
| 
| Real parabolic defined by x has Levi factor M=centralizer(A),   :math:`\mathfrak u` =positive roots not in M;   for M to be stable: x must have no C+ roots.
| 

.. _real_levi_kgbelt_x->realform1:

real_Levi
-------------------------------------------------
| ``real_Levi:KGBElt x->RealForm`` Defined in line number 370.
| 
| Levi factor of real parabolic defined by x (must have no C+ roots).
| 

.. _theta_stable_parabolic_kgbelt_x->parabolic1:

theta_stable_parabolic
-------------------------------------------------
| ``theta_stable_parabolic:KGBElt x->Parabolic`` Defined in line number 377.
| 
| Theta-stable parabolic defined by x has Levi factor L=centralizer(T),   :math:`\mathfrak u` =positive roots not in L;   for this to be stable: no C- roots.
| 

.. _theta_stable_levi_kgbelt_x->realform1:

theta_stable_Levi
-------------------------------------------------
| ``theta_stable_Levi:KGBElt x->RealForm`` Defined in line number 382.
| 
| Levi factor of theta-stable parabolic defined by x (must have no C- roots).
| 

.. _is_standard_levi_realform_l,realform_g->bool1:

is_standard_Levi
-------------------------------------------------
| ``is_standard_Levi:RealForm L,RealForm G->bool`` Defined in line number 386.
| 
| Check whether a Levi subgroup L is standard in G   (simple roots of L are simple for G).
| 

.. _kgp_realform_g,complexparabolic_(rd,s)->[kgpelt]1:

KGP
-------------------------------------------------
| ``KGP:RealForm G,ComplexParabolic (rd,S)->[KGPElt]`` Defined in line number 395.
| 
| List of K-conjugacy classes of given ComplexParabolic (as KGP elts).
| 

.. _parabolics_realform_g,complexparabolic_(rd,s)->[parabolic]1:

parabolics
-------------------------------------------------
| ``parabolics:RealForm G,ComplexParabolic (rd,S)->[Parabolic]`` Defined in line number 399.
| 
| List K-conjugacy classes of given ComplexParabolic (as Parabolics).
| 

.. _theta_stable_parabolics_realform_g,complexparabolic_p->[parabolic]1:

theta_stable_parabolics
-------------------------------------------------
| ``theta_stable_parabolics:RealForm G,ComplexParabolic P->[Parabolic]`` Defined in line number 403.
| 
| List K-conjugacy classes of given ComplexParabolic that are theta-stable.
| 

.. _theta_stable_parabolics_realform_g->[parabolic]1:

theta_stable_parabolics
-------------------------------------------------
| ``theta_stable_parabolics:RealForm G->[Parabolic]`` Defined in line number 409.
| 
| List all theta-stable parabolics for G.
| 

.. _theta_stable_parabolics_type_realform_g,[int]_p->[parabolic]1:

theta_stable_parabolics_type
-------------------------------------------------
| ``theta_stable_parabolics_type:RealForm G,[int] P->[Parabolic]`` Defined in line number 416.
| 
| List all theta-stable parabolics of G, of type S.
| 

.. _all_rel_split_theta_stable_parabolics_realform_g->[parabolic]1:

all_rel_split_theta_stable_parabolics
-------------------------------------------------
| ``all_rel_split_theta_stable_parabolics:RealForm G->[Parabolic]`` Defined in line number 422.
| 
| List all theta-stable parabolics of G with relatively split L.
| 

.. _print_theta_stable_parabolics_realform_g->void1:

print_theta_stable_parabolics
-------------------------------------------------
| ``print_theta_stable_parabolics:RealForm G->void`` Defined in line number 435.
| 
| For each theta-stable parabolic of G, print S, Levi factor, and maximal x.
| 

.. _support_kgbelt_x->[int]2:

support
-------------------------------------------------
| ``support:KGBElt x->[int]`` Defined in line number 441.
| 
| The smallest list of simple roots such that descents lead to the   distinguished fiber.
| 

.. _support_alt_kgbelt_x->[int]1:

support_alt
-------------------------------------------------
| ``support_alt:KGBElt x->[int]`` Defined in line number 450.
| 
| Auxiliary function.
| 

.. _KGPElt1:

KGPElt
----------------------------------------
| ``([int], KGBElt)`` Defined in line number 54.
| 
| Data type for a K_orbit on G/P_S, equivalently a K-conjugacy class of    parabolics of type S.
| 

.. _Parabolic1:

Parabolic
----------------------------------------
| ``([int], KGBElt)`` Defined in line number 57.
| 
| Data type for a K_orbit on G/P_S (synonym for KGPElt).
| 

.. _ComplexParabolic1:

ComplexParabolic
----------------------------------------
| ``(RootDatum,[int])`` Defined in line number 176.
| 
| Data type for a complex parabolic subrgoup
| 

