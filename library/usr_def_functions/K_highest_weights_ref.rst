.. _K_highest_weights.at_ref:

K_highest_weights.at Function References
=======================================================
|

.. _\=_khighestweight_(x,mu),_khighestweight_(y,tau)->bool1:

\=
-------------------------------------------------
| ``=:KHighestWeight (x,mu), KHighestWeight (y,tau)->bool`` Defined in line number 60.
| 
| Equality of KHighestWeights
| 

.. _is_split_spherical_param_p->bool1:

is_split_spherical
-------------------------------------------------
| ``is_split_spherical:Param p->bool`` Defined in line number 100.
| 
| Test if p is G-spherical: G rel. split, all roots in tau(p)
| 

.. _is_split_spherical_k_type_p->bool1:

is_split_spherical
-------------------------------------------------
| ``is_split_spherical:K_Type p->bool`` Defined in line number 109.
| 
| Test if a K-type is G-spherical: LKT of G-spherical p
| 

.. _highest_weight_split_spherical_k_type_p->khighestweight1:

highest_weight_split_spherical
-------------------------------------------------
| ``highest_weight_split_spherical:K_Type p->KHighestWeight`` Defined in line number 114.
| 
| Highest weight of a G-spherical K-type (is unique)
| 

.. _highest_weight_split_spherical_param_p->khighestweight1:

highest_weight_split_spherical
-------------------------------------------------
| ``highest_weight_split_spherical:Param p->KHighestWeight`` Defined in line number 128.
| 
| Highest weight of LKT of a G-spherical parameter (is unique)
| 

.. _highest_weight_split_spherical_k_type_p,kgbelt_x_k->khighestweight1:

highest_weight_split_spherical
-------------------------------------------------
| ``highest_weight_split_spherical:K_Type p,KGBElt x_K->KHighestWeight`` Defined in line number 132.
| 
| Highest weight of LKT of G-spherical K-type wrt x_K (is unique)
| 

.. _highest_weight_split_spherical_param_p,kgbelt_x_k->khighestweight1:

highest_weight_split_spherical
-------------------------------------------------
| ``highest_weight_split_spherical:Param p,KGBElt x_K->KHighestWeight`` Defined in line number 136.
| 
| Highest weight of LKT of a G-spherical parameter wrt x_K (is unique)
| 

.. _highest_weight_one_k_type_p->khighestweight1:

highest_weight_one
-------------------------------------------------
| ``highest_weight_one:K_Type p->KHighestWeight`` Defined in line number 145.
| 
| One KHighestWeight of a K-type
| 

.. _highest_weight_one_k_type_p,kgbelt_x_k->khighestweight1:

highest_weight_one
-------------------------------------------------
| ``highest_weight_one:K_Type p,KGBElt x_K->KHighestWeight`` Defined in line number 164.
| 
| One KHighestWeight of a K-type wrt x_K
| 

.. _highest_weights_k_type_p->[khighestweight]1:

highest_weights
-------------------------------------------------
| ``highest_weights:K_Type p->[KHighestWeight]`` Defined in line number 172.
| 
| All highest weights of a K-type
| 

.. _highest_weights_k_type_p,kgbelt_x_k->[khighestweight]1:

highest_weights
-------------------------------------------------
| ``highest_weights:K_Type p,KGBElt x_K->[KHighestWeight]`` Defined in line number 176.
| 
| All highest weights of a K-type wrt x_K
| 

.. _highest_weights_param_p->[khighestweight]1:

highest_weights
-------------------------------------------------
| ``highest_weights:Param p->[KHighestWeight]`` Defined in line number 181.
| 
| All highest weights of all LKTs of a parameter
| 

.. _highest_weights_param_p,kgbelt_x_k->[khighestweight]1:

highest_weights
-------------------------------------------------
| ``highest_weights:Param p,KGBElt x_K->[KHighestWeight]`` Defined in line number 187.
| 
| All highest weights of all LKTs of a parameter wrt x_K
| 

.. _highest_weight_k_type_p->khighestweight1:

highest_weight
-------------------------------------------------
| ``highest_weight:K_Type p->KHighestWeight`` Defined in line number 193.
| 
| Unique highest weight of a K-type (or error if not unique)
| 

.. _highest_weight_param_p->khighestweight1:

highest_weight
-------------------------------------------------
| ``highest_weight:Param p->KHighestWeight`` Defined in line number 199.
| 
| Unique highest weight of a parameter (or error if not unique)
| 

.. _centralizer_kgbelt_x,ratvec_v->(kgbelt,rootdatum)1:

centralizer
-------------------------------------------------
| ``centralizer:KGBElt x,ratvec v->(KGBElt,RootDatum)`` Defined in line number 218.
| 
| (internal function)
| 

.. _find_nci_root_kgbelt_x,ratvec_tau->int1:

find_nci_root
-------------------------------------------------
| ``find_nci_root:KGBElt x,ratvec tau->int`` Defined in line number 228.
| 
| (internal function)
| 

.. _project_on_dominant_cone_kgbelt_x,_ratvec_mu->(kgbelt,ratvec,ratvec)1:

project_on_dominant_cone
-------------------------------------------------
| ``project_on_dominant_cone:KGBElt x, ratvec mu->(KGBElt,ratvec,ratvec)`` Defined in line number 262.
| 
| Vogan algorithm to project KHighestWeight on dominant cone
| 

.. _project_on_dominant_cone_kgbelt_x,_vec_mu->(kgbelt,ratvec,ratvec)1:

project_on_dominant_cone
-------------------------------------------------
| ``project_on_dominant_cone:KGBElt x, vec mu->(KGBElt,ratvec,ratvec)`` Defined in line number 306.
| 
| Vogan algorithm to project KHighestWeight on dominant cone
| 

.. _characters_order_2_kgbelt_x->[vec]1:

characters_order_2
-------------------------------------------------
| ``characters_order_2:KGBElt x->[vec]`` Defined in line number 321.
| 
| (internal function)
| 

.. _all_g_spherical_same_differential_k_type_p->[k_type]1:

all_G_spherical_same_differential
-------------------------------------------------
| ``all_G_spherical_same_differential:K_Type p->[K_Type]`` Defined in line number 341.
| 
| All G-spherical K-types with same differential as given one
| 

.. _all_g_spherical_same_differential_param_p->[k_type]1:

all_G_spherical_same_differential
-------------------------------------------------
| ``all_G_spherical_same_differential:Param p->[K_Type]`` Defined in line number 358.
| 
| All G-spherical K-types with same differential as LKT of p
| 

.. _parabolic_khighestweight_(x,mu)->parabolic1:

parabolic
-------------------------------------------------
| ``parabolic:KHighestWeight (x,mu)->Parabolic`` Defined in line number 370.
| 
| Parabolic attached to KHighestWeight by Vogan algorithm
| 

.. _make_strongly_dominant_khighestweight_mu,kgbelt_x_q->khighestweight1:

make_strongly_dominant
-------------------------------------------------
| ``make_strongly_dominant:KHighestWeight mu,KGBElt x_Q->KHighestWeight`` Defined in line number 384.
| 
| 

.. _k_types_khighestweight_mu_in->[k_type]1:

K_types
-------------------------------------------------
| ``K_types:KHighestWeight mu_in->[K_Type]`` Defined in line number 392.
| 
| KHighestWeight -> array of K-types
| 

.. _k_type_khighestweight(x,mu)->k_type1:

K_type
-------------------------------------------------
| ``K_type:KHighestWeight(x,mu)->K_Type`` Defined in line number 429.
| 
| KHighestWeight -> unique K-type if unique (or error)
| 

.. _k0_highest_weight_khighestweight(x,mu)->param1:

K0_highest_weight
-------------------------------------------------
| ``K0_highest_weight:KHighestWeight(x,mu)->Param`` Defined in line number 438.
| 
| Highest weight for K_0 to KHighestWeight
| 

.. _dimension_khighestweight_mu->int1:

dimension
-------------------------------------------------
| ``dimension:KHighestWeight mu->int`` Defined in line number 446.
| 
| Dimension of KHighestWeight
| 

.. _dimension_k_type_p->int1:

dimension
-------------------------------------------------
| ``dimension:K_Type p->int`` Defined in line number 449.
| 
| Dimension of K-type
| 

.. _h_weight_kgbelt_x,vec_mu_k->khighestweight1:

H_weight
-------------------------------------------------
| ``H_weight:KGBElt x,vec mu_K->KHighestWeight`` Defined in line number 463.
| 
| 

.. _fundamental_weights_k_h_kgbelt_x->[ratvec]1:

fundamental_weights_K_H
-------------------------------------------------
| ``fundamental_weights_K_H:KGBElt x->[ratvec]`` Defined in line number 467.
| 
| 

.. _k0_param_k_type_p,kgbelt_x_k->param1:

K0_param
-------------------------------------------------
| ``K0_param:K_Type p,KGBElt x_K->Param`` Defined in line number 471.
| 
| 

.. _k0_param_k_type_p->param1:

K0_param
-------------------------------------------------
| ``K0_param:K_Type p->Param`` Defined in line number 475.
| 
| 

.. _k0_params_param_p,kgbelt_x_k->[param]1:

K0_params
-------------------------------------------------
| ``K0_params:Param p,KGBElt x_K->[Param]`` Defined in line number 482.
| 
| 

.. _k0_params_param_p->[param]1:

K0_params
-------------------------------------------------
| ``K0_params:Param p->[Param]`` Defined in line number 485.
| 
| 

.. _k0_param_param_p,kgbelt_x_k->param1:

K0_param
-------------------------------------------------
| ``K0_param:Param p,KGBElt x_K->Param`` Defined in line number 488.
| 
| 

.. _k0_param_param_p->param1:

K0_param
-------------------------------------------------
| ``K0_param:Param p->Param`` Defined in line number 493.
| 
| 

.. _fundamental_weight_coordinates_khighestweight_(x,mu)->vec1:

fundamental_weight_coordinates
-------------------------------------------------
| ``fundamental_weight_coordinates:KHighestWeight (x,mu)->vec`` Defined in line number 499.
| 
| 

.. _k_highest_weight_from_fundamental_weights_kgbelt_x,vec_tau->khighestweight1:

K_highest_weight_from_fundamental_weights
-------------------------------------------------
| ``K_highest_weight_from_fundamental_weights:KGBElt x,vec tau->KHighestWeight`` Defined in line number 504.
| 
| 

.. _dimensions_param_p,_kgbelt_x_k->[int]1:

dimensions
-------------------------------------------------
| ``dimensions:Param p, KGBElt x_K->[int]`` Defined in line number 512.
| 
| 

.. _dimensions_param_p->[int]1:

dimensions
-------------------------------------------------
| ``dimensions:Param p->[int]`` Defined in line number 514.
| 
| 

.. _dimensions_[param]_b->[[int]]1:

dimensions
-------------------------------------------------
| ``dimensions:[Param] B->[[int]]`` Defined in line number 515.
| 
| 
