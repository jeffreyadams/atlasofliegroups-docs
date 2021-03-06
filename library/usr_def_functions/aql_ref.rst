.. _aql.at_ref:

aql.at Function References
=======================================================
|

.. _inf_chars_dom_for_l_param_p,_parabolic_p->[ratvec]1:

inf_chars_dom_for_L
-------------------------------------------------
| ``inf_chars_dom_for_L:Param p, Parabolic P->[ratvec]`` Defined in line number 9.
| 
| Given a parameter p for G and a real parabolic P, list all Weyl(G)   conjugates of the infinitesimal character of p that are dominant for L.
| 

.. _inf_chars_for_l_param_p,parabolic_p->[ratvec]1:

inf_chars_for_L
-------------------------------------------------
| ``inf_chars_for_L:Param p,Parabolic P->[ratvec]`` Defined in line number 18.
| 
| Given a parameter p for G and a theta-stable parabolic P, list all   infinitesimal characters v for L so that v+rho(u) is the infinitesimal   character of p.
| 

.. _inf_chars_for_l_ratvec_gamma,parabolic_p->[ratvec]1:

inf_chars_for_L
-------------------------------------------------
| ``inf_chars_for_L:ratvec gamma,Parabolic P->[ratvec]`` Defined in line number 28.
| 
| Given an infinitesimal character gamma for G and a theta-stable parabolic P, list  all infinitesimal characters v for L so that v+rho(u) is the infinitesimal   character of p.
| 

.. _one_dim_params_gamma_ratvec_ic,_parabolic_p->[param]1:

one_dim_params_gamma
-------------------------------------------------
| ``one_dim_params_gamma:ratvec ic, Parabolic P->[Param]`` Defined in line number 38.
| 
| List all one-dimensional unitary characters with given   infinitesimal character.
| 

.. _wf_one_dim_params_ratvec_ic,_parabolic_p->[param]1:

wf_one_dim_params
-------------------------------------------------
| ``wf_one_dim_params:ratvec ic, Parabolic P->[Param]`` Defined in line number 48.
| 
| List all one-dimensional unitary characters, in the weakly fair range,   of L, with given infinitesimal character.
| 

.. _wf_aqs_param_pol_param_p,_parabolic_p->[(param,parampol)]1:

wf_aqs_param_pol
-------------------------------------------------
| ``wf_aqs_param_pol:Param p, Parabolic P->[(Param,ParamPol)]`` Defined in line number 55.
| 
| Auxiliary function: List of all unitary weakly fair Aq(lambda) modules   with infinitesimal character of p, and induced from P.
| 

.. _wf_aqs_param_param_p,_parabolic_p->[(param,param)]1:

wf_aqs_param
-------------------------------------------------
| ``wf_aqs_param:Param p, Parabolic P->[(Param,Param)]`` Defined in line number 67.
| 
| Auxiliary function: As previous function, except a list of all    parameters occurring as constitutents of such modules.
| 

.. _is_weakly_fair_aq_from_p_param_p,_parabolic_p->bool1:

is_weakly_fair_Aq_from_P
-------------------------------------------------
| ``is_weakly_fair_Aq_from_P:Param p, Parabolic P->bool`` Defined in line number 77.
| 
| Decide whether p is the parameter of a (constituent of a) unitary   weakly fair Aq(lambda) induced from parabolic P.
| 

.. _special_theta_stable_parabolics_realform_g->[parabolic]1:

special_theta_stable_parabolics
-------------------------------------------------
| ``special_theta_stable_parabolics:RealForm G->[Parabolic]`` Defined in line number 82.
| 
| List all proper theta-stable parabolics for G that are not Borels.
| 

.. _all_wf_aq_with_ic_of_param_p->[param]1:

all_wf_Aq_with_ic_of
-------------------------------------------------
| ``all_wf_Aq_with_ic_of:Param p->[Param]`` Defined in line number 90.
| 
| List all parameters of constituents of weakly fair Aq(lambda) modules with   the same infinitesimal character as p.
| 

.. _is_weakly_fair_aq_param_p->bool1:

is_weakly_fair_Aq
-------------------------------------------------
| ``is_weakly_fair_Aq:Param p->bool`` Defined in line number 98.
| 
| Determine whether parameter p is that of a (constituent of a)   unitary weakly fair Aq(lambda) module.
| 

.. _is_wf_induced_from_one_dim_param_p->[(parabolic,param)]1:

is_wf_induced_from_one_dim
-------------------------------------------------
| ``is_wf_induced_from_one_dim:Param p->[(Parabolic,Param)]`` Defined in line number 114.
| 
| List all one-dimensional unitary parameters pL so that p is theta-induced   from pL in the weakly fair range.
| 

.. _one_dim_real_induced_param_pol_param_p,_parabolic_p->[(param,parampol)]1:

one_dim_real_induced_param_pol
-------------------------------------------------
| ``one_dim_real_induced_param_pol:Param p, Parabolic P->[(Param,ParamPol)]`` Defined in line number 137.
| 
| Auxiliary function: List of all modules with infinitesimal character   of p, that are induced from a unitary character on the Levi of P.
| 

.. _one_dim_real_induced_param_param_p,_parabolic_p->[(param,param)]1:

one_dim_real_induced_param
-------------------------------------------------
| ``one_dim_real_induced_param:Param p, Parabolic P->[(Param,Param)]`` Defined in line number 149.
| 
| Auxiliary function: As previous function, except a list of all    parameters occurring as constitutents of such modules.
| 

.. _is_real_induced_from_character_from_p_param_p,_parabolic_p->bool1:

is_real_induced_from_character_from_P
-------------------------------------------------
| ``is_real_induced_from_character_from_P:Param p, Parabolic P->bool`` Defined in line number 158.
| 
| Decide whether p is the parameter of a (constituent of a) module   induced from a unitary character on the real parabolic P.
| 

.. _is_real_induced_from_one_dimensional_param_p->bool1:

is_real_induced_from_one_dimensional
-------------------------------------------------
| ``is_real_induced_from_one_dimensional:Param p->bool`` Defined in line number 164.
| 
| Determine whether parameter p is that of a (constituent of a) module (real)   induced from a unitary character.
| 

.. _real_induced_from_one_dim_param_p->[(parabolic,param)]1:

real_induced_from_one_dim
-------------------------------------------------
| ``real_induced_from_one_dim:Param p->[(Parabolic,Param)]`` Defined in line number 175.
| 
| List all one-dimensional unitary parameters pL so that p is real-induced   from pL
| 

.. _wf_aqs_param_pol_ratvec_gamma,_parabolic_p->[(param,parampol)]1:

wf_aqs_param_pol
-------------------------------------------------
| ``wf_aqs_param_pol:ratvec gamma, Parabolic P->[(Param,ParamPol)]`` Defined in line number 187.
| 
| List of all unitary weakly fair Aq(lambda) modules   with infinitesimal character gamma, and induced from P.
| 

.. _wf_aqs_param_ratvec_gamma,_parabolic_p->[(param,param)]1:

wf_aqs_param
-------------------------------------------------
| ``wf_aqs_param:ratvec gamma, Parabolic P->[(Param,Param)]`` Defined in line number 199.
| 
| As previous function, except a list of all    parameters occurring as constitutents of such modules.
| 

.. _is_unitary_by_cases_param_p->bool1:

is_unitary_by_cases
-------------------------------------------------
| ``is_unitary_by_cases:Param p->bool`` Defined in line number 211.
| 
| Test whether the irreducible given by a parameter is unitary;    if strongly regular, then check if good Aq. Otherwise, check    whether it is real or theta induced from a unitary character;   if not, compute the hermitian form.
| 

.. _is_unitary_sr_param_p->bool1:

is_unitary_sr
-------------------------------------------------
| ``is_unitary_sr:Param p->bool`` Defined in line number 229.
| 
| Test whether a representation is unitary, checking first whether    it is strongly regular.
| 

.. _is_unitary_reduced_with_form_param_p->(parampol,bool)1:

is_unitary_reduced_with_form
-------------------------------------------------
| ``is_unitary_reduced_with_form:Param p->(ParamPol,bool)`` Defined in line number 240.
| 
| Test whether a representation is unitary, checking first whether    it is strongly regular; if not, reducing it in the (weakly) good range,    and inducing the hermitian form of the smaller group. This function    the hermitian form and a boolian.
| 

.. _is_unitary_reduced_param_p->bool1:

is_unitary_reduced
-------------------------------------------------
| ``is_unitary_reduced:Param p->bool`` Defined in line number 260.
| 
| As previous function, but only returns true/false.
| 

