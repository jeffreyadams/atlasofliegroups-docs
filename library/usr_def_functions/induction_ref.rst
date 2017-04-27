.. _induction.at_ref:

induction.at Function References
=======================================================
|

.. _embed_kgb_kgbelt_x_l,realform_g->kgbelt1:

embed_KGB
-------------------------------------------------
| ``embed_KGB:KGBElt x_L,RealForm G->KGBElt`` Defined in line number 90.
| 
| If L is a theta-stable Levi factor in G,  KGB for L embeds in KGB for G.
| 

.. _inverse_embed_kgb_kgbelt_x_g,realform_l->kgbelt1:

inverse_embed_KGB
-------------------------------------------------
| ``inverse_embed_KGB:KGBElt x_G,RealForm L->KGBElt`` Defined in line number 94.
| 
| Given a KGB element of G, find one for the theta-stable Levi L which maps to it.
| 

.. _makes_mat_theta,rootdatum_rd->mat1:

makeS
-------------------------------------------------
| ``makeS:mat theta,RootDatum rd->mat`` Defined in line number 103.
| 
| Given an involution theta and a root datum, return the set S of complex roots    containing the first positive representative of each quadruple    ( :math:`\pm`  alpha, :math:`\pm`  theta(alpha)).
| 

.. _makes_kgbelt_x->mat1:

makeS
-------------------------------------------------
| ``makeS:KGBElt x->mat`` Defined in line number 108.
| 
| As the previous function, with argument a KGB element x determining the involution    and root datum
| 

.. _rho_s_(mat,rootdatum)pair->ratvec1:

rho_S
-------------------------------------------------
| ``rho_S:(mat,RootDatum)pair->ratvec`` Defined in line number 111.
| 
| Half sum of roots in chosen set S of complex roots, described above.
| 

.. _rho_s_kgbelt_x->ratvec1:

rho_S
-------------------------------------------------
| ``rho_S:KGBElt x->ratvec`` Defined in line number 114.
| 
| As previous function, with argument KGB element x.
| 

.. _make_parabolic_realform_l,realform_g->parabolic1:

make_parabolic
-------------------------------------------------
| ``make_parabolic:RealForm L,RealForm G->Parabolic`` Defined in line number 118.
| 
| Given a Levi subgroup L of G, construct the parabolic with Levi L   (this reverses Levi(P) defined in parabolics.at).
| 

.. _real_induce_standard_param_p_l,realform_g->param1:

real_induce_standard
-------------------------------------------------
| ``real_induce_standard:Param p_L,RealForm G->Param`` Defined in line number 126.
| 
| Real parabolic induction of a standard module of real Levi L (i.e., L   must be the Levi factor of a real parabolic subgroup) to G
| 

.. _real_induce_standard_parampol_p,realform_g->parampol1:

real_induce_standard
-------------------------------------------------
| ``real_induce_standard:ParamPol P,RealForm G->ParamPol`` Defined in line number 137.
| 
| Real parabolic induction of standards, applied to a formal sum of    parameters (ParamPol).
| 

.. _real_induce_irreducible_as_sum_of_standards_param_p_l,_realform_g->parampol1:

real_induce_irreducible_as_sum_of_standards
-------------------------------------------------
| ``real_induce_irreducible_as_sum_of_standards:Param p_L, RealForm G->ParamPol`` Defined in line number 145.
| 
| Write the (real) induced of an irreducible J(p_L) of L as a formal sum of    standards for G; uses the character formula to write J(p_L)    as a formal sum of standards for L first. (Auxiliary function)
| 

.. _real_induce_irreducible_param_p_l,_realform_g->parampol1:

real_induce_irreducible
-------------------------------------------------
| ``real_induce_irreducible:Param p_L, RealForm G->ParamPol`` Defined in line number 155.
| 
| Write the (real) induced Ind(J(p_L)) of an irreducible of L as a sum of    irreducibles for G; uses composition series to convert    output of the previous function into sum of irreducibles. L must    be the Levi factor of a real parabolic subgroup.
| 

.. _cuspidal_data_param_p->(parabolic,param)1:

cuspidal_data
-------------------------------------------------
| ``cuspidal_data:Param p->(Parabolic,Param)`` Defined in line number 166.
| 
| Cuspidal data associated to a parameter p: a cuspidal parabolic subgroup P=MN    and parameter p_M for a relative limit of discrete series so that    Ind(I(p_M))=I(p); uses real_parabolic(x) of parabolics.at
| 

.. _theta_stable_data_param_p->(parabolic,param)1:

theta_stable_data
-------------------------------------------------
| ``theta_stable_data:Param p->(Parabolic,Param)`` Defined in line number 187.
| 
| Theta-stable data associated to a parameter p: a theta-stable parabolic P=LN    with L relatively split, and parameter p_L for a principal series representation    so that p is obtained by cohomological parabolic induction    from p_L; uses theta_stable_parabolic(x) of parabolics.at.
| 

.. _coherent_std_imaginary_w_word_w,param_p->parampol1:

coherent_std_imaginary
-------------------------------------------------
| ``coherent_std_imaginary:W_word w,Param p->ParamPol`` Defined in line number 204.
| 
| Auxiliary function
| 

.. _standardize_param_p->parampol1:

standardize
-------------------------------------------------
| ``standardize:Param p->ParamPol`` Defined in line number 220.
| 
| Convert a possibly non-standard parameter into a linear combination of   standard ones
| 

.. _standardize_parampol_p->parampol1:

standardize
-------------------------------------------------
| ``standardize:ParamPol P->ParamPol`` Defined in line number 231.
| 
| Standardize a formal linear combination of possibly non-standard parameters
| 

.. _theta_induce_standard_param_p_l,realform_g->parampol1:

theta_induce_standard
-------------------------------------------------
| ``theta_induce_standard:Param p_L,RealForm G->ParamPol`` Defined in line number 240.
| 
| Theta-stable (cohomological) parabolic induction of a standard module for    the Levi L of a theta-stable parabolic; if outside of weakly good range,    must apply standardize.
| 

.. _theta_induce_irreducible_as_sum_of_standards_param_p_l,_realform_g->parampol1:

theta_induce_irreducible_as_sum_of_standards
-------------------------------------------------
| ``theta_induce_irreducible_as_sum_of_standards:Param p_L, RealForm G->ParamPol`` Defined in line number 269.
| 
| Write the (theta-stable) induced of an irreducible J(p_L) of L as a formal    sum of standards for G; uses the character formula to write J(p_L)    as a formal sum of standards for L first. (Auxiliary function)
| 

.. _theta_induce_irreducible_param_p_l,_realform_g->parampol1:

theta_induce_irreducible
-------------------------------------------------
| ``theta_induce_irreducible:Param p_L, RealForm G->ParamPol`` Defined in line number 285.
| 
| Write the (theta-stable) induced Ind(J(p_L)) of an irreducible of L    as a sum of irreducibles for G; uses composition series to convert    output of the previous function into sum of irreducibles. The subgroup    L must be the Levi factor of a theta-stable parabolic.
| 

.. _map_into_distinguished_fiber_kgbelt_x->kgbelt1:

map_into_distinguished_fiber
-------------------------------------------------
| ``map_into_distinguished_fiber:KGBElt x->KGBElt`` Defined in line number 314.
| 
| (Auxiliary function)
| 

.. _strong_map_into_distinguished_fiber_kgbelt_x->kgbelt1:

strong_map_into_distinguished_fiber
-------------------------------------------------
| ``strong_map_into_distinguished_fiber:KGBElt x->KGBElt`` Defined in line number 331.
| 
| Map KGB element x to x_K in the distinguished fiber; if necessary, use complex   cross actions first to move x to a fiber with no C- roots.
| 

.. _canonical_x_k_kgbelt_x->kgbelt1:

canonical_x_K
-------------------------------------------------
| ``canonical_x_K:KGBElt x->KGBElt`` Defined in line number 335.
| 
| Same as previous function.
| 

.. _canonical_x_k_param_p->kgbelt1:

canonical_x_K
-------------------------------------------------
| ``canonical_x_K:Param p->KGBElt`` Defined in line number 338.
| 
| Previous function with input a parameter p; it is applied to x(p).
| 

.. _u_kgbelt_x->mat1:

u
-------------------------------------------------
| ``u:KGBElt x->mat`` Defined in line number 342.
| 
| Positive coroots in the nilradical of the theta-stable parabolic determined by x.
| 

.. _rho_u_cx_parabolic_p->ratvec1:

rho_u_cx
-------------------------------------------------
| ``rho_u_cx:Parabolic P->ratvec`` Defined in line number 353.
| 
| Half sum of positive complex roots (on fundamental Cartan) in the nilradical of P;   P must be theta-stable.
| 

.. _rho_u_cx_t_parabolic_p->vec1:

rho_u_cx_T
-------------------------------------------------
| ``rho_u_cx_T:Parabolic P->vec`` Defined in line number 369.
| 
| Element of :math:`X^*`  with same restriction to :math:`(X^*)^{\theta}`  as rho_u_cx(P);   P must be theta-stable.
| 

.. _rho_u_ic_parabolic_p->ratvec1:

rho_u_ic
-------------------------------------------------
| ``rho_u_ic:Parabolic P->ratvec`` Defined in line number 379.
| 
| Half sum of imaginary compact roots in nilradical of (theta-stable) P.
| 

.. _two_rho_u_cap_k_parabolic_p->vec1:

two_rho_u_cap_k
-------------------------------------------------
| ``two_rho_u_cap_k:Parabolic P->vec`` Defined in line number 387.
| 
| Sum of compact roots (of :math:`\mathfrak t` ) in :math:`\mathfrak u`  for theta-stable parabolic P.
| 

.. _two_rho_u_cap_s_parabolic_p->vec1:

two_rho_u_cap_s
-------------------------------------------------
| ``two_rho_u_cap_s:Parabolic P->vec`` Defined in line number 391.
| 
| Sum of non-compact roots in :math:`\mathfrak u`  (for theta-stable parabolic).
| 

.. _rho_u_cap_k_parabolic_p->ratvec1:

rho_u_cap_k
-------------------------------------------------
| ``rho_u_cap_k:Parabolic P->ratvec`` Defined in line number 396.
| 
| Half sum of compact roots in :math:`\mathfrak u`  (for theta-stable parabolic).
| 

.. _rho_u_cap_s_parabolic_p->ratvec1:

rho_u_cap_s
-------------------------------------------------
| ``rho_u_cap_s:Parabolic P->ratvec`` Defined in line number 399.
| 
| Half sum of non-compact roots in :math:`\mathfrak u`  (for theta-stable parabolic).
| 

.. _dim_u_parabolic_p->int1:

dim_u
-------------------------------------------------
| ``dim_u:Parabolic P->int`` Defined in line number 402.
| 
| Dimension of :math:`\mathfrak u`  (nilrad of theta-stable parabolic).
| 

.. _dim_u_kgbelt_x->int1:

dim_u
-------------------------------------------------
| ``dim_u:KGBElt x->int`` Defined in line number 405.
| 
| Dimension of the nilradical of the theta-stable parabolic determined by KGB elt x.
| 

.. _dim_u_cap_k_parabolic_(,x):p->int1:

dim_u_cap_k
-------------------------------------------------
| ``dim_u_cap_k:Parabolic (,x):P->int`` Defined in line number 411.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak k`  for theta-stable parabolic.
| 

.. _dim_u_cap_k_kgbelt_x->int1:

dim_u_cap_k
-------------------------------------------------
| ``dim_u_cap_k:KGBElt x->int`` Defined in line number 422.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak k`  for theta-stable parabolic determined   by x.
| 

.. _dim_u_cap_k_ratvec_lambda,kgbelt_x->int1:

dim_u_cap_k
-------------------------------------------------
| ``dim_u_cap_k:ratvec lambda,KGBElt x->int`` Defined in line number 426.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak k`  for theta-stable parabolic determined by   weight lambda.
| 

.. _dim_u_cap_p_parabolic_(,x):p->int1:

dim_u_cap_p
-------------------------------------------------
| ``dim_u_cap_p:Parabolic (,x):P->int`` Defined in line number 431.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak p`  for theta-stable parabolic.
| 

.. _dim_u_cap_p_kgbelt_x->int3:

dim_u_cap_p
-------------------------------------------------
| ``dim_u_cap_p:KGBElt x->int`` Defined in line number 442.
| 
| Dimension of :math:`\mathfrak u \cap\mathfrak p`  for theta-stable parabolic associated   to x.
| 

.. _dim_u_cap_p_ratvec_lambda,kgbelt_x->int1:

dim_u_cap_p
-------------------------------------------------
| ``dim_u_cap_p:ratvec lambda,KGBElt x->int`` Defined in line number 446.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak p`  for theta-stable parabolic determined by   weight lambda.
| 

.. _dim_u_cap_k_2_parabolic_p,ratvec_h->int1:

dim_u_cap_k_2
-------------------------------------------------
| ``dim_u_cap_k_2:Parabolic P,ratvec H->int`` Defined in line number 451.
| 
| (Auxiliary function)
| 

.. _dim_u_cap_k_ge2_parabolic_p,ratvec_h->int1:

dim_u_cap_k_ge2
-------------------------------------------------
| ``dim_u_cap_k_ge2:Parabolic P,ratvec H->int`` Defined in line number 462.
| 
| (Auxiliary function)
| 

.. _dim_u_cap_p_ge2_parabolic_p,ratvec_h->int1:

dim_u_cap_p_ge2
-------------------------------------------------
| ``dim_u_cap_p_ge2:Parabolic P,ratvec H->int`` Defined in line number 473.
| 
| (Auxiliary function)
| 

.. _dim_u_cap_k_1_parabolic_p,ratvec_h->int1:

dim_u_cap_k_1
-------------------------------------------------
| ``dim_u_cap_k_1:Parabolic P,ratvec H->int`` Defined in line number 484.
| 
| (Auxiliary function)
| 

.. _make_dominant_kgbelt_x_in,ratvec_lambda_in,_ratvec_lambda_q_in->(kgbelt,ratvec,ratvec)1:

make_dominant
-------------------------------------------------
| ``make_dominant:KGBElt x_in,ratvec lambda_in, ratvec lambda_q_in->(KGBElt,ratvec,ratvec)`` Defined in line number 517.
| 
| Conjugate the triple (x,lambda, lambda_q) to make lambda_q weakly   dominant (auxiliary function).
| 

.. _aq_param_pol_kgbelt_x_in,ratvec_lambda_in,_ratvec_lambda_q->parampol1:

Aq_param_pol
-------------------------------------------------
| ``Aq_param_pol:KGBElt x_in,ratvec lambda_in, ratvec lambda_q->ParamPol`` Defined in line number 524.
| 
| A_q(lambda) module; :math:`\mathfrak q`  is defined by the weight lambda_q; x_in   must be attached to the fundamental Cartan. The module is defined as a ParamPol,   in case it is reducible.
| 

.. _aq_kgbelt_x_in,ratvec_lambda_in,_ratvec_lambda_q->param1:

Aq
-------------------------------------------------
| ``Aq:KGBElt x_in,ratvec lambda_in, ratvec lambda_q->Param`` Defined in line number 546.
| 
| A_q(lambda) module defined as above, but as a parameter, assuming it is   irreducible.
| 

.. _aq_kgbelt_x,ratvec_lambda_in->param1:

Aq
-------------------------------------------------
| ``Aq:KGBElt x,ratvec lambda_in->Param`` Defined in line number 554.
| 
| If not provided, assume lambda_q=lambda_in in the definition of A_q.
| 

.. _aq_realform_g,ratvec_lambda_in,_ratvec_lambda_q->param1:

Aq
-------------------------------------------------
| ``Aq:RealForm G,ratvec lambda_in, ratvec lambda_q->Param`` Defined in line number 558.
| 
| A_q(lambda), specify G, not x, to use x=KGB(G,0).
| 

.. _aq_realform_g,ratvec_lambda_in->param1:

Aq
-------------------------------------------------
| ``Aq:RealForm G,ratvec lambda_in->Param`` Defined in line number 562.
| 
| A_q(lambda), specify G, not x, and use lambda_q=lambda_in.
| 

.. _is_one_dimensional_param_p->bool1:

is_one_dimensional
-------------------------------------------------
| ``is_one_dimensional:Param p->bool`` Defined in line number 569.
| 
| Decide whether a parameter defines a one-dimensional representation.
| 

.. _is_good_kgbelt_x_in,ratvec_lambda_in,ratvec_lambda_q_in->bool1:

is_good
-------------------------------------------------
| ``is_good:KGBElt x_in,ratvec lambda_in,ratvec lambda_q_in->bool`` Defined in line number 573.
| 
| Decide whether A_q(lambda) is good.
| 

.. _is_weakly_good_kgbelt_x_in,ratvec_lambda_in,ratvec_lambda_q_in->bool1:

is_weakly_good
-------------------------------------------------
| ``is_weakly_good:KGBElt x_in,ratvec lambda_in,ratvec lambda_q_in->bool`` Defined in line number 578.
| 
| Decide whether A_q(lambda) is weakly good.
| 

.. _is_fair_kgbelt_x_in,ratvec_lambda_in,ratvec_lambda_q_in->bool1:

is_fair
-------------------------------------------------
| ``is_fair:KGBElt x_in,ratvec lambda_in,ratvec lambda_q_in->bool`` Defined in line number 583.
| 
| Decide whether A_q(lambda) is fair.
| 

.. _is_weakly_fair_kgbelt_x_in,ratvec_lambda_in,ratvec_lambda_q_in->bool1:

is_weakly_fair
-------------------------------------------------
| ``is_weakly_fair:KGBElt x_in,ratvec lambda_in,ratvec lambda_q_in->bool`` Defined in line number 588.
| 
| Decide whether A_q(lambda) is weakly fair.
| 

.. _goodness_kgbelt_x,ratvec_lambda_in,ratvec_lambda_q->void1:

goodness
-------------------------------------------------
| ``goodness:KGBElt x,ratvec lambda_in,ratvec lambda_q->void`` Defined in line number 594.
| 
| Determine the "goodness" of an Aq(lambda); returns "good", "weakly good",   "fair", "weakly fair", or "none".
| 

.. _is_good_param_p_l,realform_g->bool1:

is_good
-------------------------------------------------
| ``is_good:Param p_L,RealForm G->bool`` Defined in line number 610.
| 
| Decide whether a parameter for L is in the good range for G; this only    makes sense if L is the Levi of a (standard) theta-stable parabolic.
| 

.. _is_weakly_good_param_p_l,realform_g->bool1:

is_weakly_good
-------------------------------------------------
| ``is_weakly_good:Param p_L,RealForm G->bool`` Defined in line number 624.
| 
| Decide whether a parameter for L is in the weakly good range for G; this only    makes sense if L is the Levi of a theta-stable parabolic.
| 

.. _is_fair_param_p_l,realform_g->bool1:

is_fair
-------------------------------------------------
| ``is_fair:Param p_L,RealForm G->bool`` Defined in line number 634.
| 
| Decide whether a parameter for L is in the fair range for G; this only    makes sense if L is the Levi of a theta-stable parabolic.
| 

.. _is_weakly_fair_param_p_l,realform_g->bool1:

is_weakly_fair
-------------------------------------------------
| ``is_weakly_fair:Param p_L,RealForm G->bool`` Defined in line number 649.
| 
| Decide whether a parameter for L is in the weakly fair range for G; this only    makes sense if L is the Levi of a theta-stable parabolic, and is only defined    if p_L is one-dimensional.
| 

.. _goodness_param_p_l,realform_g->void1:

goodness
-------------------------------------------------
| ``goodness:Param p_L,RealForm G->void`` Defined in line number 661.
| 
| Determine the "goodness" of a parameter for L; returns "good", "weakly good",   "fair", "weakly fair", or "none"; only makes sense if L is Levi of theta-stable   parabolic.
| 

.. _aq_packet_realform_g,complexparabolic_p->[param]1:

Aq_packet
-------------------------------------------------
| ``Aq_packet:RealForm G,ComplexParabolic P->[Param]`` Defined in line number 677.
| 
| List all A_q(0) (actually: R_q(trivial): infinitesimal character rho(G)) modules   with Q a theta-stable parabolic of type P.
| 

.. _aq_packet_realform_g,[int]_s->[param]:aq_packet(g,complexparabolic1:

Aq_packet
-------------------------------------------------
| ``Aq_packet:RealForm G,[int] S->[Param]:Aq_packet(G,ComplexParabolic`` Defined in line number 686.
| 
| List all A_q(0) (infinitesimal character rho(G)) modules   with Q a theta-stable parabolic of type S (list of simple roots).
| 

.. _aq_packet_realform_g,[*]_s->[param]:aq_packet(g,[int]1:

Aq_packet
-------------------------------------------------
| ``Aq_packet:RealForm G,[*] S->[Param]:Aq_packet(G,[int]`` Defined in line number 688.
| 
| 

.. _aq_zeros_realform_g->[param]1:

Aq_zeros
-------------------------------------------------
| ``Aq_zeros:RealForm G->[Param]`` Defined in line number 692.
| 
| List all good Aq(0) (inf. char. rho) of G; this is more or less   blocku (there may be duplications).
| 

.. _theta_stable_parabolics_max_kgbelt_x->[parabolic]1:

theta_stable_parabolics_max
-------------------------------------------------
| ``theta_stable_parabolics_max:KGBElt x->[Parabolic]`` Defined in line number 699.
| 
| Given a KGB element x, list all theta-stable parabolics in G   with maximal element x.
| 

.. _theta_stable_parabolics_with_kgbelt_x->[parabolic]1:

theta_stable_parabolics_with
-------------------------------------------------
| ``theta_stable_parabolics_with:KGBElt x->[Parabolic]`` Defined in line number 706.
| 
| Given a KGB element x, list all theta-stable parabolics in G   determined by x.
| 

.. _theta_stable_parabolics_with_[parabolic]_tsp,kgbelt_x->[parabolic]1:

theta_stable_parabolics_with
-------------------------------------------------
| ``theta_stable_parabolics_with:[Parabolic] tsp,KGBElt x->[Parabolic]`` Defined in line number 713.
| 
| Same as previous function, but takes the output of   theta_stable_parabolics(G) as additional input for efficiency.
| 

.. _is_theta_x_kgbelt_x->bool1:

is_theta_x
-------------------------------------------------
| ``is_theta_x:KGBElt x->bool`` Defined in line number 720.
| 
| Decide whether there is a theta-stable parabolic determined by x.
| 

.. _is_good_range_induced_from_param_p->[param]1:

is_good_range_induced_from
-------------------------------------------------
| ``is_good_range_induced_from:Param p->[Param]`` Defined in line number 724.
| 
| List of parameters p_L in the (weakly) good range for G so that p is   theta-induced from p_L; may be more than one.
| 

.. _reduce_good_range_param_p->param1:

reduce_good_range
-------------------------------------------------
| ``reduce_good_range:Param p->Param`` Defined in line number 814.
| 
| Find the parameter p_L so that p is cohomologically induced, in the   (weakly) good range, from p_L, with L minimal (may be G).
| 

.. _is_good_aq_param_p->bool1:

is_good_Aq
-------------------------------------------------
| ``is_good_Aq:Param p->bool`` Defined in line number 829.
| 
| Determine whether p is a (weakly) good Aq(lambda).
| 

.. _is_proper_aq_param_p->bool1:

is_proper_Aq
-------------------------------------------------
| ``is_proper_Aq:Param p->bool`` Defined in line number 834.
| 
| Determine whether p is a proper (weakly) good Aq(lambda).
| 

