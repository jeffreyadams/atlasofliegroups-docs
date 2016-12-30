.. _K_highest_weights.at_ref:

K_highest_weights.at Function References
=======================================================
|

.. _\=_KHighestWeight_(x,mu),_KHighestWeight_(y,tau)->bool1:

\=
-------------------------------------------------
| ``=:KHighestWeight (x,mu), KHighestWeight (y,tau)->bool`` Defined in line number 98.
| 
| Equality of KHighestWeights; (x,mu)=(x',mu') iff x=x', and mu and mu'    differ by (1-theta)X^* or compact Weyl group action.
| 

.. _lkts_param_p->[k_type]1:

LKTs
-------------------------------------------------
| ``LKTs:Param p->[K_Type]`` Defined in line number 124.
| 
| List of LKTs (as final tempered limit parameters) of a module given by a    parameter.
| 

.. _lkt_param_p->k_type1:

LKT
-------------------------------------------------
| ``LKT:Param p->K_Type`` Defined in line number 127.
| 
| LKT of module given by a parameter, if it is unique (otherwise error message)
| 

.. _is_split_spherical_param_p->bool1:

is_split_spherical
-------------------------------------------------
| ``is_split_spherical:Param p->bool`` Defined in line number 134.
| 
| Test if parameter p for G is G-spherical: G must be rel. split, all roots    in tau(p).
| 

.. _is_split_spherical_k_type_p->bool1:

is_split_spherical
-------------------------------------------------
| ``is_split_spherical:K_Type p->bool`` Defined in line number 143.
| 
| Test if a K-type is G-spherical: must be LKT of G-spherical p.
| 

.. _highest_weight_split_spherical_k_type_p->khighestweight1:

highest_weight_split_spherical
-------------------------------------------------
| ``highest_weight_split_spherical:K_Type p->KHighestWeight`` Defined in line number 147.
| 
| Highest weight of a G-spherical K-type (necessarily unique).
| 

.. _highest_weight_split_spherical_param_p->khighestweight1:

highest_weight_split_spherical
-------------------------------------------------
| ``highest_weight_split_spherical:Param p->KHighestWeight`` Defined in line number 161.
| 
| Highest weight of LKT of a G-spherical parameter (is unique).
| 

.. _highest_weight_split_spherical_k_type_p,kgbelt_x_k->khighestweight1:

highest_weight_split_spherical
-------------------------------------------------
| ``highest_weight_split_spherical:K_Type p,KGBElt x_K->KHighestWeight`` Defined in line number 165.
| 
| Highest weight of LKT of G-spherical K-type w.r.t. x_K (is unique).
| 

.. _highest_weight_split_spherical_param_p,kgbelt_x_k->khighestweight1:

highest_weight_split_spherical
-------------------------------------------------
| ``highest_weight_split_spherical:Param p,KGBElt x_K->KHighestWeight`` Defined in line number 169.
| 
| Highest weight of LKT of a G-spherical parameter w.r.t. x_K (is unique).
| 

.. _highest_weight_one_k_type_p->khighestweight1:

highest_weight_one
-------------------------------------------------
| ``highest_weight_one:K_Type p->KHighestWeight`` Defined in line number 173.
| 
| This function returns just ONE KHighestWeight of a K-type (auxiliary function).
| 

.. _highest_weight_one_k_type_p,kgbelt_x_k->khighestweight1:

highest_weight_one
-------------------------------------------------
| ``highest_weight_one:K_Type p,KGBElt x_K->KHighestWeight`` Defined in line number 192.
| 
| ONE KHighestWeight of a K-type w.r.t. x_K (auxiliary function).
| 

.. _highest_weights_k_type_p->[khighestweight]1:

highest_weights
-------------------------------------------------
| ``highest_weights:K_Type p->[KHighestWeight]`` Defined in line number 197.
| 
| All highest weights of a K-type; R-group acts on one KHighestWeight of    previous function (number of terms is |R(K)/R(K,mu)|).
| 

.. _highest_weights_k_type_p,kgbelt_x_k->[khighestweight]1:

highest_weights
-------------------------------------------------
| ``highest_weights:K_Type p,KGBElt x_K->[KHighestWeight]`` Defined in line number 201.
| 
| All highest weights of a K-type w.r.t. x_K.
| 

.. _highest_weights_param_p->[khighestweight]1:

highest_weights
-------------------------------------------------
| ``highest_weights:Param p->[KHighestWeight]`` Defined in line number 205.
| 
| List of all highest weights of all LKTs of a parameter.
| 

.. _highest_weights_param_p,kgbelt_x_k->[khighestweight]1:

highest_weights
-------------------------------------------------
| ``highest_weights:Param p,KGBElt x_K->[KHighestWeight]`` Defined in line number 211.
| 
| List of all highest weights of all LKTs of a parameter w.r.t. x_K.
| 

.. _highest_weight_k_type_p->khighestweight1:

highest_weight
-------------------------------------------------
| ``highest_weight:K_Type p->KHighestWeight`` Defined in line number 215.
| 
| Unique highest weight of a K-type (or error if not unique).
| 

.. _highest_weight_k_type_p,kgbelt_x_k->khighestweight1:

highest_weight
-------------------------------------------------
| ``highest_weight:K_Type p,KGBElt x_K->KHighestWeight`` Defined in line number 221.
| 
| Unique highest weight of a K-type w.r.t. x_K (or error if not unique).
| 

.. _highest_weight_param_p->khighestweight1:

highest_weight
-------------------------------------------------
| ``highest_weight:Param p->KHighestWeight`` Defined in line number 227.
| 
| Unique highest weight of (unique) LKT of a parameter (or error if not unique).
| 

.. _centralizer_kgbelt_x,ratvec_v->(kgbelt,rootdatum)1:

centralizer
-------------------------------------------------
| ``centralizer:KGBElt x,ratvec v->(KGBElt,RootDatum)`` Defined in line number 243.
| 
| (Auxiliary function)
| 

.. _find_nci_root_kgbelt_x,ratvec_tau->int1:

find_nci_root
-------------------------------------------------
| ``find_nci_root:KGBElt x,ratvec tau->int`` Defined in line number 253.
| 
| (Auxiliary function)
| 

.. _tworho_k_kgbelt_x->ratvec1:

tworho_K
-------------------------------------------------
| ``tworho_K:KGBElt x->ratvec`` Defined in line number 287.
| 
| Sum of the roots of K as an element of :math:`(X^*)^{\delta}\otimes\mathbb Q`  (this may be half-integral); x must be in the distinguished fiber.
| 

.. _project_on_dominant_cone_kgbelt_x,_ratvec_mu->(kgbelt,ratvec,ratvec)1:

project_on_dominant_cone
-------------------------------------------------
| ``project_on_dominant_cone:KGBElt x, ratvec mu->(KGBElt,ratvec,ratvec)`` Defined in line number 296.
| 
| Vogan algorithm to project KHighestWeight (x,mu) on dominant cone; returns    (x',mu+2rho_K(x)-rho,tau) with tau dominant and x' corresponding to the new    Weyl chamber.
| 

.. _project_on_dominant_cone_kgbelt_x,_vec_mu->(kgbelt,ratvec,ratvec)1:

project_on_dominant_cone
-------------------------------------------------
| ``project_on_dominant_cone:KGBElt x, vec mu->(KGBElt,ratvec,ratvec)`` Defined in line number 340.
| 
| Vogan algorithm; previous function in case mu is given as a vec, rather than ratvec.
| 

.. _characters_order_2_kgbelt_x->[vec]1:

characters_order_2
-------------------------------------------------
| ``characters_order_2:KGBElt x->[vec]`` Defined in line number 355.
| 
| (Auxiliary function)
| 

.. _all_g_spherical_same_differential_k_type_p->[k_type]1:

all_G_spherical_same_differential
-------------------------------------------------
| ``all_G_spherical_same_differential:K_Type p->[K_Type]`` Defined in line number 375.
| 
| All G-spherical K-types with same differential as given one.
| 

.. _all_g_spherical_same_differential_param_p->[k_type]1:

all_G_spherical_same_differential
-------------------------------------------------
| ``all_G_spherical_same_differential:Param p->[K_Type]`` Defined in line number 392.
| 
| All G-spherical K-types with same differential as the LKT of parameter p.
| 

.. _parabolic_lkt_khighestweight_(x,mu)->parabolic1:

parabolic_LKT
-------------------------------------------------
| ``parabolic_LKT:KHighestWeight (x,mu)->Parabolic`` Defined in line number 404.
| 
| Parabolic attached to KHighestWeight by Vogan algorithm.
| 

.. _make_strongly_dominant_khighestweight_mu,kgbelt_x_q->khighestweight1:

make_strongly_dominant
-------------------------------------------------
| ``make_strongly_dominant:KHighestWeight mu,KGBElt x_Q->KHighestWeight`` Defined in line number 419.
| 
| (Auxiliary function)
| 

.. _k_types_khighestweight_mu_in->[k_type]1:

K_types
-------------------------------------------------
| ``K_types:KHighestWeight mu_in->[K_Type]`` Defined in line number 427.
| 
| All K_types with the same KHighestWeight.
| 

.. _k_type_khighestweight(x,mu)->k_type1:

K_type
-------------------------------------------------
| ``K_type:KHighestWeight(x,mu)->K_Type`` Defined in line number 464.
| 
| K_type with given KHighestWeight if unique (otherwise error).
| 

.. _k0_highest_weight_khighestweight(x,mu)->param1:

K0_highest_weight
-------------------------------------------------
| ``K0_highest_weight:KHighestWeight(x,mu)->Param`` Defined in line number 474.
| 
| Parameter for (the RealForm K_0) of the K_0-type with highest weight    (the restriction of) KHighestWeight mu.
| 

.. _dimension_khighestweight_mu->int1:

dimension
-------------------------------------------------
| ``dimension:KHighestWeight mu->int`` Defined in line number 482.
| 
| Dimension of the K_#-type with KHighestWeight mu.
| 

.. _dimension_k_type_p->int1:

dimension
-------------------------------------------------
| ``dimension:K_Type p->int`` Defined in line number 485.
| 
| Dimension of a K-type.
| 

.. _h_weight_kgbelt_x,vec_mu_k->khighestweight1:

H_weight
-------------------------------------------------
| ``H_weight:KGBElt x,vec mu_K->KHighestWeight`` Defined in line number 496.
| 
| (Auxiliary function)
| 

.. _fundamental_weights_k_h_kgbelt_x->[ratvec]1:

fundamental_weights_K_H
-------------------------------------------------
| ``fundamental_weights_K_H:KGBElt x->[ratvec]`` Defined in line number 501.
| 
| (Auxiliary function)
| 

.. _k0_param_k_type_p,kgbelt_x_k->param1:

K0_param
-------------------------------------------------
| ``K0_param:K_Type p,KGBElt x_K->Param`` Defined in line number 507.
| 
| ONE K_0-type in the restriction of a K_type to the identity component K_0 of K    (auxiliary function).
| 

.. _k0_param_k_type_p->param1:

K0_param
-------------------------------------------------
| ``K0_param:K_Type p->Param`` Defined in line number 513.
| 
| ONE K_0-type in the restriction of a K_type to the identity component K_0 of K    (auxiliary function).
| 

.. _k0_params_param_p,kgbelt_x_k->[param]1:

K0_params
-------------------------------------------------
| ``K0_params:Param p,KGBElt x_K->[Param]`` Defined in line number 521.
| 
| All K_0-types in the restriction of the LKTs of parameter p K_0.
| 

.. _k0_params_param_p->[param]1:

K0_params
-------------------------------------------------
| ``K0_params:Param p->[Param]`` Defined in line number 526.
| 
| All K_0-types in the restriction of the LKTs of parameter p to K_0.
| 

.. _k0_param_param_p,kgbelt_x_k->param1:

K0_param
-------------------------------------------------
| ``K0_param:Param p,KGBElt x_K->Param`` Defined in line number 530.
| 
| Unique K_0-type in the restriction of (unique) LKT to K_0 (error if not unique).
| 

.. _k0_param_param_p->param1:

K0_param
-------------------------------------------------
| ``K0_param:Param p->Param`` Defined in line number 536.
| 
| Unique K_0-type in the restriction of (unique) LKT to K_0 (error if not unique).
| 

.. _fundamental_weight_coordinates_khighestweight_(x,mu)->vec1:

fundamental_weight_coordinates
-------------------------------------------------
| ``fundamental_weight_coordinates:KHighestWeight (x,mu)->vec`` Defined in line number 543.
| 
| (Auxiliary function)
| 

.. _k_highest_weight_from_fundamental_weights_kgbelt_x,vec_tau->khighestweight1:

K_highest_weight_from_fundamental_weights
-------------------------------------------------
| ``K_highest_weight_from_fundamental_weights:KGBElt x,vec tau->KHighestWeight`` Defined in line number 549.
| 
| (Auxiliary function)
| 

.. _dimensions_param_p,_kgbelt_x_k->[int]1:

dimensions
-------------------------------------------------
| ``dimensions:Param p, KGBElt x_K->[int]`` Defined in line number 558.
| 
| List of the dimensions of the K_0-types in the restriction of the LKTs of parameter p.
| 

.. _dimensions_param_p->[int]1:

dimensions
-------------------------------------------------
| ``dimensions:Param p->[int]`` Defined in line number 562.
| 
| List of the dimensions of the K_0-types in the restriction of the LKTs of parameter p.
| 

.. _dimensions_[param]_b->[[int]]1:

dimensions
-------------------------------------------------
| ``dimensions:[Param] B->[[int]]`` Defined in line number 566.
| 
| List of the dimensions of the K_0-types in the restriction of the LKTs of    a list of parameters.
| 

