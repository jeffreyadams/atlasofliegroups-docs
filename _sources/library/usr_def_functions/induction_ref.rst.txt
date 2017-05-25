.. _induction.at_ref:

induction.at Function References
=======================================================
|

.. _embed_kgb_kgbelt_x_l,realform_g->kgbelt1:

embed_KGB
-------------------------------------------------
| ``embed_KGB:KGBElt x_L,RealForm G->KGBElt`` Defined in line number 89.
| 
| If L is a theta-stable Levi factor in G,  KGB for L embeds in KGB for G.
| 

.. _inverse_embed_kgb_kgbelt_x_g,realform_l->kgbelt1:

inverse_embed_KGB
-------------------------------------------------
| ``inverse_embed_KGB:KGBElt x_G,RealForm L->KGBElt`` Defined in line number 93.
| 
| Given a KGB element of G, find one for the theta-stable Levi L which maps to it.
| 

.. _makes_mat_theta,rootdatum_rd->mat1:

makeS
-------------------------------------------------
| ``makeS:mat theta,RootDatum rd->mat`` Defined in line number 102.
| 
| Given an involution theta and a root datum, return the set S of complex roots    containing the first positive representative of each quadruple    ( :math:`\pm`  alpha, :math:`\pm`  theta(alpha)).
| 

.. _makes_kgbelt_x->mat1:

makeS
-------------------------------------------------
| ``makeS:KGBElt x->mat`` Defined in line number 107.
| 
| As the previous function, with argument a KGB element x determining the involution    and root datum
| 

.. _rho_s_(mat,rootdatum)pair->ratvec1:

rho_S
-------------------------------------------------
| ``rho_S:(mat,RootDatum)pair->ratvec`` Defined in line number 110.
| 
| Half sum of roots in chosen set S of complex roots, described above.
| 

.. _rho_s_kgbelt_x->ratvec1:

rho_S
-------------------------------------------------
| ``rho_S:KGBElt x->ratvec`` Defined in line number 113.
| 
| As previous function, with argument KGB element x.
| 

.. _make_parabolic_realform_l,realform_g->parabolic1:

make_parabolic
-------------------------------------------------
| ``make_parabolic:RealForm L,RealForm G->Parabolic`` Defined in line number 117.
| 
| Given a Levi subgroup L of G, construct the parabolic with Levi L   (this reverses Levi(P) defined in parabolics.at).
| 

.. _real_induce_standard_param_p_l,realform_g->param1:

real_induce_standard
-------------------------------------------------
| ``real_induce_standard:Param p_L,RealForm G->Param`` Defined in line number 125.
| 
| Real parabolic induction of a standard module of real Levi L (i.e., L   must be the Levi factor of a real parabolic subgroup) to G
| 

.. _real_induce_standard_parampol_p,realform_g->parampol1:

real_induce_standard
-------------------------------------------------
| ``real_induce_standard:ParamPol P,RealForm G->ParamPol`` Defined in line number 136.
| 
| Real parabolic induction of standards, applied to a formal sum of    parameters (ParamPol).
| 

.. _real_induce_irreducible_as_sum_of_standards_param_p_l,_realform_g->parampol1:

real_induce_irreducible_as_sum_of_standards
-------------------------------------------------
| ``real_induce_irreducible_as_sum_of_standards:Param p_L, RealForm G->ParamPol`` Defined in line number 142.
| 
| Write the (real) induced of an irreducible J(p_L) of L as a formal sum of    standards for G; uses the character formula to write J(p_L)    as a formal sum of standards for L first. (Auxiliary function)
| 

.. _real_induce_irreducible_final_param_p_l,_realform_g->parampol1:

real_induce_irreducible_final
-------------------------------------------------
| ``real_induce_irreducible_final:Param p_L, RealForm G->ParamPol`` Defined in line number 151.
| 
| Write the (real) induced :math:`Ind(J(p_L))`  of an irreducible of |L| as a sum of    irreducibles for |G|; uses composition series to convert output of the    |real_induce_irreducible_as_sum_of_standards| into sum of irreducibles.    The real form |L| of |p_L| must be the Levi factor of a real parabolic    subgroup; and the parameter p_L must be final.
| 

.. _real_induce_irreducible_parampol_p,realform_g->parampol1:

real_induce_irreducible
-------------------------------------------------
| ``real_induce_irreducible:ParamPol P,RealForm G->ParamPol`` Defined in line number 156.
| 
| Given a polynomial of parameters of L, real induce each term,    and write the result as a polynomial of parameters for G.
| 

.. _cuspidal_data_param_p->(parabolic,param)1:

cuspidal_data
-------------------------------------------------
| ``cuspidal_data:Param p->(Parabolic,Param)`` Defined in line number 170.
| 
| Cuspidal data associated to a parameter p: a cuspidal parabolic subgroup P=MN    and parameter p_M for a relative limit of discrete series so that    Ind(I(p_M))=I(p); uses real_parabolic(x) of parabolics.at
| 

.. _theta_stable_data_param_p->(parabolic,param)1:

theta_stable_data
-------------------------------------------------
| ``theta_stable_data:Param p->(Parabolic,Param)`` Defined in line number 191.
| 
| Theta-stable data associated to a parameter p: a theta-stable parabolic P=LN    with L relatively split, and parameter p_L for a principal series representation    so that p is obtained by cohomological parabolic induction    from p_L; uses theta_stable_parabolic(x) of parabolics.at.
| 

.. _coherent_std_imaginary_w_word_w,param_p->parampol1:

coherent_std_imaginary
-------------------------------------------------
| ``coherent_std_imaginary:W_word w,Param p->ParamPol`` Defined in line number 208.
| 
| Auxiliary function
| 

.. _standardize_param_p->parampol1:

standardize
-------------------------------------------------
| ``standardize:Param p->ParamPol`` Defined in line number 224.
| 
| Convert a possibly non-standard parameter into a linear combination of   standard ones
| 

.. _standardize_parampol_p->parampol1:

standardize
-------------------------------------------------
| ``standardize:ParamPol P->ParamPol`` Defined in line number 235.
| 
| Standardize a formal linear combination of possibly non-standard parameters
| 

.. _theta_induce_standard_param_p_l,realform_g->parampol1:

theta_induce_standard
-------------------------------------------------
| ``theta_induce_standard:Param p_L,RealForm G->ParamPol`` Defined in line number 242.
| 
| Theta-stable (cohomological) parabolic induction of a standard module for    the Levi L of a theta-stable parabolic; if outside of weakly good range,    must apply standardize.
| 

.. _theta_induce_parampol_parampol_p,_realform_g->parampol1:

theta_induce_parampol
-------------------------------------------------
| ``theta_induce_parampol:ParamPol P, RealForm G->ParamPol`` Defined in line number 270.
| 
| Given a ParamPol P, form a new ParamPol by theta-inducing each    summand.
| 

.. _theta_induce_irreducible_as_sum_of_standards_param_p_l,_realform_g->parampol1:

theta_induce_irreducible_as_sum_of_standards
-------------------------------------------------
| ``theta_induce_irreducible_as_sum_of_standards:Param p_L, RealForm G->ParamPol`` Defined in line number 280.
| 
| Write the (theta-stable) induced of an irreducible J(p_L) of L as a formal    sum of standards for G; uses the character formula to write J(p_L)    as a formal sum of standards for L first. (Auxiliary function)
| 

.. _theta_induce_irreducible_final_param_p_l,_realform_g->parampol1:

theta_induce_irreducible_final
-------------------------------------------------
| ``theta_induce_irreducible_final:Param p_L, RealForm G->ParamPol`` Defined in line number 295.
| 
| Write the (theta-stable) induced Ind(J(p_L)) of an irreducible of L    as a sum of irreducibles for G; uses composition series to convert    output of the previous function into sum of irreducibles. The subgroup    L must be the Levi factor of a theta-stable parabolic. The parameter    p_L must be final.
| 

.. _theta_induce_irreducible_parampol_p,realform_g->parampol1:

theta_induce_irreducible
-------------------------------------------------
| ``theta_induce_irreducible:ParamPol P,RealForm G->ParamPol`` Defined in line number 304.
| 
| Given a polynomial of parameters, theta-induce each constituent, and    write the result as a polynomial of parameters.
| 

.. _map_into_distinguished_fiber_kgbelt_x->kgbelt1:

map_into_distinguished_fiber
-------------------------------------------------
| ``map_into_distinguished_fiber:KGBElt x->KGBElt`` Defined in line number 334.
| 
| (Auxiliary function)
| 

.. _strong_map_into_distinguished_fiber_kgbelt_x->kgbelt1:

strong_map_into_distinguished_fiber
-------------------------------------------------
| ``strong_map_into_distinguished_fiber:KGBElt x->KGBElt`` Defined in line number 351.
| 
| Map KGB element x to x_K in the distinguished fiber; if necessary, use complex   cross actions first to move x to a fiber with no C- roots.
| 

.. _canonical_x_k_kgbelt_x->kgbelt1:

canonical_x_K
-------------------------------------------------
| ``canonical_x_K:KGBElt x->KGBElt`` Defined in line number 355.
| 
| Same as previous function.
| 

.. _canonical_x_k_param_p->kgbelt1:

canonical_x_K
-------------------------------------------------
| ``canonical_x_K:Param p->KGBElt`` Defined in line number 358.
| 
| Previous function with input a parameter p; it is applied to x(p).
| 

.. _u_kgbelt_x->mat1:

u
-------------------------------------------------
| ``u:KGBElt x->mat`` Defined in line number 362.
| 
| Positive coroots in the nilradical of the theta-stable parabolic determined by x.
| 

.. _rho_u_cx_parabolic_p->ratvec1:

rho_u_cx
-------------------------------------------------
| ``rho_u_cx:Parabolic P->ratvec`` Defined in line number 373.
| 
| Half sum of positive complex roots (on fundamental Cartan) in the nilradical of P;   P must be theta-stable.
| 

.. _rho_u_cx_t_parabolic_p->vec1:

rho_u_cx_T
-------------------------------------------------
| ``rho_u_cx_T:Parabolic P->vec`` Defined in line number 389.
| 
| Element of :math:`X^*`  with same restriction to :math:`(X^*)^{\theta}`  as rho_u_cx(P);   P must be theta-stable.
| 

.. _rho_u_ic_parabolic_p->ratvec1:

rho_u_ic
-------------------------------------------------
| ``rho_u_ic:Parabolic P->ratvec`` Defined in line number 399.
| 
| Half sum of imaginary compact roots in nilradical of (theta-stable) P.
| 

.. _two_rho_u_cap_k_parabolic_p->vec1:

two_rho_u_cap_k
-------------------------------------------------
| ``two_rho_u_cap_k:Parabolic P->vec`` Defined in line number 407.
| 
| Sum of compact roots (of :math:`\mathfrak t` ) in :math:`\mathfrak u`  for theta-stable parabolic P.
| 

.. _two_rho_u_cap_s_parabolic_p->vec1:

two_rho_u_cap_s
-------------------------------------------------
| ``two_rho_u_cap_s:Parabolic P->vec`` Defined in line number 411.
| 
| Sum of non-compact roots in :math:`\mathfrak u`  (for theta-stable parabolic).
| 

.. _rho_u_cap_k_parabolic_p->ratvec1:

rho_u_cap_k
-------------------------------------------------
| ``rho_u_cap_k:Parabolic P->ratvec`` Defined in line number 416.
| 
| Half sum of compact roots in :math:`\mathfrak u`  (for theta-stable parabolic).
| 

.. _rho_u_cap_s_parabolic_p->ratvec1:

rho_u_cap_s
-------------------------------------------------
| ``rho_u_cap_s:Parabolic P->ratvec`` Defined in line number 419.
| 
| Half sum of non-compact roots in :math:`\mathfrak u`  (for theta-stable parabolic).
| 

.. _dim_u_parabolic_p->int1:

dim_u
-------------------------------------------------
| ``dim_u:Parabolic P->int`` Defined in line number 422.
| 
| Dimension of :math:`\mathfrak u`  (nilrad of theta-stable parabolic).
| 

.. _dim_u_kgbelt_x->int1:

dim_u
-------------------------------------------------
| ``dim_u:KGBElt x->int`` Defined in line number 425.
| 
| Dimension of the nilradical of the theta-stable parabolic determined by KGB elt x.
| 

.. _dim_u_cap_k_parabolic_(,x):p->int1:

dim_u_cap_k
-------------------------------------------------
| ``dim_u_cap_k:Parabolic (,x):P->int`` Defined in line number 431.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak k`  for theta-stable parabolic.
| 

.. _dim_u_cap_k_kgbelt_x->int1:

dim_u_cap_k
-------------------------------------------------
| ``dim_u_cap_k:KGBElt x->int`` Defined in line number 442.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak k`  for theta-stable parabolic determined   by x.
| 

.. _dim_u_cap_k_ratvec_lambda,kgbelt_x->int1:

dim_u_cap_k
-------------------------------------------------
| ``dim_u_cap_k:ratvec lambda,KGBElt x->int`` Defined in line number 446.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak k`  for theta-stable parabolic determined by   weight lambda.
| 

.. _dim_u_cap_p_parabolic_(,x):p->int1:

dim_u_cap_p
-------------------------------------------------
| ``dim_u_cap_p:Parabolic (,x):P->int`` Defined in line number 451.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak p`  for theta-stable parabolic.
| 

.. _dim_u_cap_p_kgbelt_x->int1:

dim_u_cap_p
-------------------------------------------------
| ``dim_u_cap_p:KGBElt x->int`` Defined in line number 462.
| 
| Dimension of :math:`\mathfrak u \cap\mathfrak p`  for theta-stable parabolic associated   to x.
| 

.. _dim_u_cap_p_ratvec_lambda,kgbelt_x->int1:

dim_u_cap_p
-------------------------------------------------
| ``dim_u_cap_p:ratvec lambda,KGBElt x->int`` Defined in line number 466.
| 
| Dimension of :math:`\mathfrak u\cap\mathfrak p`  for theta-stable parabolic determined by   weight lambda.
| 

.. _dim_u_cap_k_2_parabolic_p,ratvec_h->int1:

dim_u_cap_k_2
-------------------------------------------------
| ``dim_u_cap_k_2:Parabolic P,ratvec H->int`` Defined in line number 471.
| 
| (Auxiliary function)
| 

.. _dim_u_cap_k_ge2_parabolic_p,ratvec_h->int1:

dim_u_cap_k_ge2
-------------------------------------------------
| ``dim_u_cap_k_ge2:Parabolic P,ratvec H->int`` Defined in line number 482.
| 
| (Auxiliary function)
| 

.. _dim_u_cap_p_ge2_parabolic_p,ratvec_h->int1:

dim_u_cap_p_ge2
-------------------------------------------------
| ``dim_u_cap_p_ge2:Parabolic P,ratvec H->int`` Defined in line number 493.
| 
| (Auxiliary function)
| 

.. _dim_u_cap_k_1_parabolic_p,ratvec_h->int1:

dim_u_cap_k_1
-------------------------------------------------
| ``dim_u_cap_k_1:Parabolic P,ratvec H->int`` Defined in line number 504.
| 
| (Auxiliary function)
| 

.. _make_dominant_kgbelt_x_in,ratvec_lambda_in,_ratvec_lambda_q_in->(kgbelt,ratvec,ratvec)1:

make_dominant
-------------------------------------------------
| ``make_dominant:KGBElt x_in,ratvec lambda_in, ratvec lambda_q_in->(KGBElt,ratvec,ratvec)`` Defined in line number 537.
| 
| Conjugate the triple (x,lambda, lambda_q) to make lambda_q weakly   dominant (auxiliary function).
| 

.. _aq_reducible_kgbelt_x_in,ratvec_lambda_in,_ratvec_lambda_q->parampol1:

Aq_reducible
-------------------------------------------------
| ``Aq_reducible:KGBElt x_in,ratvec lambda_in, ratvec lambda_q->ParamPol`` Defined in line number 544.
| 
| A_q(lambda) module; :math:`\mathfrak q`  is defined by the weight lambda_q; x_in   must be attached to the fundamental Cartan. The module is defined as a ParamPol,   in case it is reducible.
| 

.. _aq_kgbelt_x_in,ratvec_lambda_in,_ratvec_lambda_q->param1:

Aq
-------------------------------------------------
| ``Aq:KGBElt x_in,ratvec lambda_in, ratvec lambda_q->Param`` Defined in line number 566.
| 
| A_q(lambda) module defined as above, but as a parameter, assuming it is   irreducible.
| 

.. _aq_kgbelt_x,ratvec_lambda_in->param1:

Aq
-------------------------------------------------
| ``Aq:KGBElt x,ratvec lambda_in->Param`` Defined in line number 574.
| 
| If not provided, assume lambda_q=lambda_in in the definition of A_q.
| 

.. _aq_realform_g,ratvec_lambda_in,_ratvec_lambda_q->param1:

Aq
-------------------------------------------------
| ``Aq:RealForm G,ratvec lambda_in, ratvec lambda_q->Param`` Defined in line number 578.
| 
| A_q(lambda), specify G, not x, to use x=KGB(G,0).
| 

.. _aq_realform_g,ratvec_lambda_in->param1:

Aq
-------------------------------------------------
| ``Aq:RealForm G,ratvec lambda_in->Param`` Defined in line number 582.
| 
| A_q(lambda), specify G, not x, and use lambda_q=lambda_in.
| 

.. _is_one_dimensional_param_p->bool1:

is_one_dimensional
-------------------------------------------------
| ``is_one_dimensional:Param p->bool`` Defined in line number 589.
| 
| Decide whether a parameter defines a one-dimensional representation.
| 

.. _is_unitary_character_param_p->bool1:

is_unitary_character
-------------------------------------------------
| ``is_unitary_character:Param p->bool`` Defined in line number 593.
| 
| Decide whether a parameter defines a unitary one-dimensional character.
| 

.. _is_good_kgbelt_x_in,ratvec_lambda_in,ratvec_lambda_q_in->bool1:

is_good
-------------------------------------------------
| ``is_good:KGBElt x_in,ratvec lambda_in,ratvec lambda_q_in->bool`` Defined in line number 600.
| 
| Decide whether A_q(lambda) is good.
| 

.. _is_weakly_good_kgbelt_x_in,ratvec_lambda_in,ratvec_lambda_q_in->bool1:

is_weakly_good
-------------------------------------------------
| ``is_weakly_good:KGBElt x_in,ratvec lambda_in,ratvec lambda_q_in->bool`` Defined in line number 605.
| 
| Decide whether A_q(lambda) is weakly good.
| 

.. _is_fair_kgbelt_x_in,ratvec_lambda_in,ratvec_lambda_q_in->bool1:

is_fair
-------------------------------------------------
| ``is_fair:KGBElt x_in,ratvec lambda_in,ratvec lambda_q_in->bool`` Defined in line number 610.
| 
| Decide whether A_q(lambda) is fair.
| 

.. _is_weakly_fair_kgbelt_x_in,ratvec_lambda_in,ratvec_lambda_q_in->bool1:

is_weakly_fair
-------------------------------------------------
| ``is_weakly_fair:KGBElt x_in,ratvec lambda_in,ratvec lambda_q_in->bool`` Defined in line number 615.
| 
| Decide whether A_q(lambda) is weakly fair.
| 

.. _goodness_kgbelt_x,ratvec_lambda_in,ratvec_lambda_q->string1:

goodness
-------------------------------------------------
| ``goodness:KGBElt x,ratvec lambda_in,ratvec lambda_q->string`` Defined in line number 621.
| 
| Determine the "goodness" of an Aq(lambda); returns "good", "weakly good",   "fair", "weakly fair", or "none".
| 

.. _is_good_param_p_l,realform_g->bool1:

is_good
-------------------------------------------------
| ``is_good:Param p_L,RealForm G->bool`` Defined in line number 637.
| 
| Decide whether a parameter for L is in the good range for G; this only    makes sense if L is the Levi of a (standard) theta-stable parabolic.
| 

.. _is_weakly_good_param_p_l,realform_g->bool1:

is_weakly_good
-------------------------------------------------
| ``is_weakly_good:Param p_L,RealForm G->bool`` Defined in line number 651.
| 
| Decide whether a parameter for L is in the weakly good range for G; this only    makes sense if L is the Levi of a theta-stable parabolic.
| 

.. _is_fair_param_p_l,realform_g->bool1:

is_fair
-------------------------------------------------
| ``is_fair:Param p_L,RealForm G->bool`` Defined in line number 662.
| 
| Decide whether a parameter for L is in the fair range for G; this only    makes sense if L is the Levi of a theta-stable parabolic, and is only    defined if p_L is one_dimensional.
| 

.. _is_weakly_fair_param_p_l,realform_g->bool1:

is_weakly_fair
-------------------------------------------------
| ``is_weakly_fair:Param p_L,RealForm G->bool`` Defined in line number 678.
| 
| Decide whether a parameter for L is in the weakly fair range for G; this only    makes sense if L is the Levi of a theta-stable parabolic, and is only defined    if p_L is one-dimensional.
| 

.. _goodness_param_p_l,realform_g->string1:

goodness
-------------------------------------------------
| ``goodness:Param p_L,RealForm G->string`` Defined in line number 690.
| 
| Determine the "goodness" of a parameter for L; returns "good", "weakly good",   "fair", "weakly fair", or "none"; only makes sense if L is Levi of theta-stable   parabolic.
| 

.. _aq_packet_realform_g,complexparabolic_p->[param]1:

Aq_packet
-------------------------------------------------
| ``Aq_packet:RealForm G,ComplexParabolic P->[Param]`` Defined in line number 706.
| 
| List all A_q(0) (actually: R_q(trivial): infinitesimal character rho(G))    modules with Q a theta-stable parabolic of type P.
| 

.. _aq_packet_realform_g,[int]_s->[param]:aq_packet(g,complexparabolic1:

Aq_packet
-------------------------------------------------
| ``Aq_packet:RealForm G,[int] S->[Param]:Aq_packet(G,ComplexParabolic`` Defined in line number 715.
| 
| List all A_q(0) (infinitesimal character rho(G)) modules   with Q a theta-stable parabolic of type S (list of simple roots).
| 

.. _aq_packet_realform_g,[*]_s->[param]:aq_packet(g,[int]1:

Aq_packet
-------------------------------------------------
| ``Aq_packet:RealForm G,[*] S->[Param]:Aq_packet(G,[int]`` Defined in line number 717.
| 
| 

.. _aq_zeros_realform_g->[param]1:

Aq_zeros
-------------------------------------------------
| ``Aq_zeros:RealForm G->[Param]`` Defined in line number 721.
| 
| List all good Aq(0) (inf. char. rho) of G; this is more or less   blocku (there may be duplications).
| 

.. _theta_stable_parabolics_max_kgbelt_x->[parabolic]1:

theta_stable_parabolics_max
-------------------------------------------------
| ``theta_stable_parabolics_max:KGBElt x->[Parabolic]`` Defined in line number 728.
| 
| Given a KGB element x, list all theta-stable parabolics in G   with maximal element x.
| 

.. _theta_stable_parabolics_with_kgbelt_x->[parabolic]1:

theta_stable_parabolics_with
-------------------------------------------------
| ``theta_stable_parabolics_with:KGBElt x->[Parabolic]`` Defined in line number 736.
| 
| Given a KGB element x, list all theta-stable parabolics in G   determined by x.
| 

.. _theta_stable_parabolics_with_[parabolic]_tsp,kgbelt_x->[parabolic]1:

theta_stable_parabolics_with
-------------------------------------------------
| ``theta_stable_parabolics_with:[Parabolic] tsp,KGBElt x->[Parabolic]`` Defined in line number 743.
| 
| Same as previous function, but takes the output of   theta_stable_parabolics(G) as additional input for efficiency.
| 

.. _is_theta_x_kgbelt_x->bool1:

is_theta_x
-------------------------------------------------
| ``is_theta_x:KGBElt x->bool`` Defined in line number 750.
| 
| Decide whether there is a theta-stable parabolic determined by x.
| 

.. _is_good_range_induced_from_param_p->[param]1:

is_good_range_induced_from
-------------------------------------------------
| ``is_good_range_induced_from:Param p->[Param]`` Defined in line number 754.
| 
| List of parameters p_L in the (weakly) good range for G so that p is   theta-induced from p_L; may be more than one.
| 

.. _reduce_good_range_param_p->(parabolic,param)1:

reduce_good_range
-------------------------------------------------
| ``reduce_good_range:Param p->(Parabolic,Param)`` Defined in line number 776.
| 
| Find the parabolic P and parameter p_L so that p is cohomologically induced,   in the (weakly) good range, from p_L, with L minimal (may be G).
| 

.. _is_good_aq_param_p->bool1:

is_good_Aq
-------------------------------------------------
| ``is_good_Aq:Param p->bool`` Defined in line number 797.
| 
| Determine whether p is a (weakly) good unitary Aq(lambda).
| 

.. _is_proper_aq_param_p->bool1:

is_proper_Aq
-------------------------------------------------
| ``is_proper_Aq:Param p->bool`` Defined in line number 802.
| 
| Determine whether p is a proper (weakly) good unitary Aq(lambda).
| 

.. _all_real_induced_one_dimensional_realform_g->[param]1:

all_real_induced_one_dimensional
-------------------------------------------------
| ``all_real_induced_one_dimensional:RealForm G->[Param]`` Defined in line number 807.
| 
| 

