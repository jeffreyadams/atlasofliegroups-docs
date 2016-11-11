.. _induction.at_ref:

induction.at Function References
=======================================================
|

.. _embed_kgb_kgbelt_x_l,realform_g->kgbelt1:

embed_KGB
-------------------------------------------------
| ``embed_KGB:KGBElt x_L,RealForm G->KGBElt`` Defined in line number 44.
| 
| If L is a theta-stable Levi factor in G,  KGB for L embeds in KGB for G.
| 

.. _inverse_embed_kgb_kgbelt_x_g,realform_l->kgbelt1:

inverse_embed_KGB
-------------------------------------------------
| ``inverse_embed_KGB:KGBElt x_G,RealForm L->KGBElt`` Defined in line number 48.
| 
| Given a KGB element of G, find one for the theta-stable Levi L which maps to it.
| 

.. _makes_mat_theta,rootdatum_rd->mat1:

makeS
-------------------------------------------------
| ``makeS:mat theta,RootDatum rd->mat`` Defined in line number 57.
| 
| Given an involution theta and a root datum, return the set S of complex roots    containing the first positive representative of each quadruple    ( :math:`\pm`  alpha, :math:`\pm`  theta(alpha)).
| 

.. _makes_kgbelt_x->mat1:

makeS
-------------------------------------------------
| ``makeS:KGBElt x->mat`` Defined in line number 62.
| 
| As the previous function, with argument a KGB element x determining the involution    and root datum
| 

.. _rho_s_(mat,rootdatum)pair->ratvec1:

rho_S
-------------------------------------------------
| ``rho_S:(mat,RootDatum)pair->ratvec`` Defined in line number 65.
| 
| Half sum of roots in chosen set S of complex roots, described above.
| 

.. _rho_s_kgbelt_x->ratvec1:

rho_S
-------------------------------------------------
| ``rho_S:KGBElt x->ratvec`` Defined in line number 68.
| 
| As previous function, with argument KGB element x.
| 

.. _real_induce_standard_param_p_l,realform_g->param1:

real_induce_standard
-------------------------------------------------
| ``real_induce_standard:Param p_L,RealForm G->Param`` Defined in line number 72.
| 
| Real parabolic induction of a standard module of real Levi L to G
| 

.. _real_induce_standard_parampol_p,realform_g->parampol1:

real_induce_standard
-------------------------------------------------
| ``real_induce_standard:ParamPol P,RealForm G->ParamPol`` Defined in line number 81.
| 
| Real parabolic induction of standards, applied to a formal sum of    parameters (ParamPol).
| 

.. _real_induce_irreducible_as_sum_of_standards_param_p_l,_realform_g->parampol1:

real_induce_irreducible_as_sum_of_standards
-------------------------------------------------
| ``real_induce_irreducible_as_sum_of_standards:Param p_L, RealForm G->ParamPol`` Defined in line number 89.
| 
| Write the (real) induced of an irreducible J(p_L) of L as a formal sum of    standards for G; uses the character formula to write J(p_L)    as a formal sum of standards for L first. (Auxiliary function)
| 

.. _real_induce_irreducible_param_p_l,_realform_g->parampol1:

real_induce_irreducible
-------------------------------------------------
| ``real_induce_irreducible:Param p_L, RealForm G->ParamPol`` Defined in line number 98.
| 
| Write the (real) induced Ind(J(p_L)) of an irreducible of L as a sum of    irreducibles for G; uses composition series to convert    output of the previous function into sum of irreducibles.
| 

.. _cuspidal_data_param_p->(parabolic,param)1:

cuspidal_data
-------------------------------------------------
| ``cuspidal_data:Param p->(Parabolic,Param)`` Defined in line number 109.
| 
| Cuspidal data associated to a parameter p: a cuspidal parabolic subgroup P=MN    and parameter p_M for a relative limit of discrete series so that    Ind(I(p_M))=I(p); uses real_parabolic(x) of parabolics.at
| 

.. _theta_stable_data_param_p->(parabolic,param)1:

theta_stable_data
-------------------------------------------------
| ``theta_stable_data:Param p->(Parabolic,Param)`` Defined in line number 130.
| 
| Theta-stable data associated to a parameter p: a theta-stable parabolic P=LN    with L relatively split, and parameter p_L for a principal series representation    so that p is obtained by cohomological parabolic induction    from p_L; uses theta_stable_parabolic(x) of parabolics.at.
| 

.. _coherent_std_imaginary_w_word_w,param_p->parampol1:

coherent_std_imaginary
-------------------------------------------------
| ``coherent_std_imaginary:W_word w,Param p->ParamPol`` Defined in line number 147.
| 
| Auxiliary function
| 

.. _standardize_param_p->parampol1:

standardize
-------------------------------------------------
| ``standardize:Param p->ParamPol`` Defined in line number 163.
| 
| Convert a possibly non-standard parameter into a linear combination of   standard ones
| 

.. _standardize_parampol_p->parampol1:

standardize
-------------------------------------------------
| ``standardize:ParamPol P->ParamPol`` Defined in line number 174.
| 
| Standardize a formal linear combination of possibly non-standard parameters
| 

.. _theta_induce_standard_param_p_l,realform_g->parampol1:

theta_induce_standard
-------------------------------------------------
| ``theta_induce_standard:Param p_L,RealForm G->ParamPol`` Defined in line number 183.
| 
| Theta-stable (cohomological) parabolic induction of a standard module for    the Levi L of a theta-stable parabolic; if outside of weakly good range,    must apply standardize.
| 

.. _theta_induce_irreducible_as_sum_of_standards_param_p_l,_realform_g->parampol1:

theta_induce_irreducible_as_sum_of_standards
-------------------------------------------------
| ``theta_induce_irreducible_as_sum_of_standards:Param p_L, RealForm G->ParamPol`` Defined in line number 213.
| 
| Write the (theta-stable) induced of an irreducible J(p_L) of L as a formal    sum of standards for G; uses the character formula to write J(p_L)    as a formal sum of standards for L first. (Auxiliary function)
| 

.. _theta_induce_irreducible_param_p_l,_realform_g->parampol1:

theta_induce_irreducible
-------------------------------------------------
| ``theta_induce_irreducible:Param p_L, RealForm G->ParamPol`` Defined in line number 228.
| 
| Write the (theta-stable) induced Ind(J(p_L)) of an irreducible of L    as a sum of irreducibles for G; uses composition series to convert    output of the previous function into sum of irreducibles.
| 

.. _induce_standard_param_p_l,parabolic_p,realform_g->parampol1:

induce_standard
-------------------------------------------------
| ``induce_standard:Param p_L,Parabolic P,RealForm G->ParamPol`` Defined in line number 250.
| 
| Real or theta-stable parabolic induction of a standard module,    depending on whether P=LN a real or theta-stable parabolic    (returns error message if neither).
| 

.. _induce_irreducible_param_p_l,parabolic_p,realform_g->parampol1:

induce_irreducible
-------------------------------------------------
| ``induce_irreducible:Param p_L,Parabolic P,RealForm G->ParamPol`` Defined in line number 262.
| 
| Write the (real or theta-stable) induced Ind(J(p_L)) of an irreducible    of L as a sum of irreducibles for G; error message if P=LN is not a real    or theta-stable parabolic.
| 

.. _induce_standard_parampol_pol,parabolic_p,realform_g->parampol1:

induce_standard
-------------------------------------------------
| ``induce_standard:ParamPol pol,Parabolic P,RealForm G->ParamPol`` Defined in line number 273.
| 
| Real or theta-stable parabolic induction applied to a linear combination    of standard modules (error message if P is not real or theta-stable).
| 

