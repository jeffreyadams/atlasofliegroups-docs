K_highest_weights.at References
====================================================

.. _\=_(KHighestWeight,KHighestWeight->bool):

\=
-------------------------------------------------------------------

``=: (KHighestWeight,KHighestWeight->bool)``

Short description: equality of KHighestWeights.

Defined in line number 59


.. _is_split_spherical_(Param->bool):

is_split_spherical
-------------------------------------------------------------------

``is_split_spherical: (Param->bool)``

Short description: test if p is G-spherical: G rel. split, all roots in tau(p)

Defined in line number 99


.. _is_split_spherical_(K_Type->bool):

is_split_spherical
-------------------------------------------------------------------

``is_split_spherical: (K_Type->bool)``

Short description: test if a K-type is G-spherical: LKT of G-spherical p

Defined in line number 108


.. _highest_weight_split_spherical_(K_Type->KHighestWeight):

highest_weight_split_spherical
-------------------------------------------------------------------

``highest_weight_split_spherical: (K_Type->KHighestWeight)``

Short description: highest weight of a G-spherical K-type (is unique)

Defined in line number 113


.. _highest_weight_split_spherical_(Param->KHighestWeight):

highest_weight_split_spherical
-------------------------------------------------------------------

``highest_weight_split_spherical: (Param->KHighestWeight)``

Short description: highest weight of LKT of a G-spherical parameter (is unique)

Defined in line number 127


.. _highest_weight_split_spherical_(K_Type,KGBElt->KHighestWeight):

highest_weight_split_spherical
-------------------------------------------------------------------

``highest_weight_split_spherical: (K_Type,KGBElt->KHighestWeight)``

Short description: highest weight of LKT of G-spherical K-type wrt x_K (is unique)

Defined in line number 131


.. _highest_weight_split_spherical_(Param,KGBElt->KHighestWeight):

highest_weight_split_spherical
-------------------------------------------------------------------

``highest_weight_split_spherical: (Param,KGBElt->KHighestWeight)``

Short description: highest weight of LKT of a G-spherical parameter wrt x_K (is unique)

Defined in line number 135


.. _highest_weight_one_(K_Type->KHighestWeight):

highest_weight_one
-------------------------------------------------------------------

``highest_weight_one: (K_Type->KHighestWeight)``

Short description: one KHighestWeight of a K-type

Defined in line number 144


.. _highest_weight_one_(K_Type,KGBElt->KHighestWeight):

highest_weight_one
-------------------------------------------------------------------

``highest_weight_one: (K_Type,KGBElt->KHighestWeight)``

Short description: one KHighestWeight of a K-type wrt x_K

Defined in line number 163


.. _highest_weights_(K_Type->[KHighestWeight]):

highest_weights
-------------------------------------------------------------------

``highest_weights: (K_Type->[KHighestWeight])``

Short description: all highest weights of a K-type

Defined in line number 171


.. _highest_weights_(K_Type,KGBElt->[KHighestWeight]):

highest_weights
-------------------------------------------------------------------

``highest_weights: (K_Type,KGBElt->[KHighestWeight])``

Short description: all highest weights of a K-type wrt x_K

Defined in line number 175


.. _highest_weights_(Param->[KHighestWeight]):

highest_weights
-------------------------------------------------------------------

``highest_weights: (Param->[KHighestWeight])``

Short description: all highest weights of all LKTs of a parameter

Defined in line number 180


.. _highest_weights_(Param,KGBElt->[KHighestWeight]):

highest_weights
-------------------------------------------------------------------

``highest_weights: (Param,KGBElt->[KHighestWeight])``

Short description: all highest weights of all LKTs of a parameter wrt x_K

Defined in line number 186


.. _highest_weight_(K_Type->KHighestWeight):

highest_weight
-------------------------------------------------------------------

``highest_weight: (K_Type->KHighestWeight)``

Short description: unique highest weight of a K-type (or error if not unique)

Defined in line number 192


.. _highest_weight_(Param->KHighestWeight):

highest_weight
-------------------------------------------------------------------

``highest_weight: (Param->KHighestWeight)``

Short description: unique highest weight of a parameter (or error if not unique)

Defined in line number 198


.. _centralizer_(KGBElt,ratvec->(KGBElt,RootDatum)):

centralizer
-------------------------------------------------------------------

``centralizer: (KGBElt,ratvec->(KGBElt,RootDatum))``

Short description: (internal function)

Defined in line number 217


.. _find_nci_root_(KGBElt,ratvec->int):

find_nci_root
-------------------------------------------------------------------

``find_nci_root: (KGBElt,ratvec->int)``

Short description: (internal function)

Defined in line number 227


.. _project_on_dominant_cone_(KGBElt,ratvec->(KGBElt,ratvec,ratvec)):

project_on_dominant_cone
-------------------------------------------------------------------

``project_on_dominant_cone: (KGBElt,ratvec->(KGBElt,ratvec,ratvec))``

Short description: Vogan algorithm to project KHighestWeight on dominant cone

Defined in line number 261


.. _project_on_dominant_cone_(KGBElt,vec->(KGBElt,ratvec,ratvec)):

project_on_dominant_cone
-------------------------------------------------------------------

``project_on_dominant_cone: (KGBElt,vec->(KGBElt,ratvec,ratvec))``

Short description: Vogan algorithm to project KHighestWeight on dominant cone

Defined in line number 305


.. _characters_order_2_(KGBElt->[vec]):

characters_order_2
-------------------------------------------------------------------

``characters_order_2: (KGBElt->[vec])``

Short description: (internal function)

Defined in line number 320


.. _all_G_spherical_same_differential_(K_Type->[K_Type]):

all_G_spherical_same_differential
-------------------------------------------------------------------

``all_G_spherical_same_differential: (K_Type->[K_Type])``

Short description: all G-spherical K-types with same differential as given one

Defined in line number 340


.. _all_G_spherical_same_differential_(Param->[K_Type]):

all_G_spherical_same_differential
-------------------------------------------------------------------

``all_G_spherical_same_differential: (Param->[K_Type])``

Short description: all G-spherical K-types with same differential as LKT of p

Defined in line number 357


.. _parabolic_(KHighestWeight->Parabolic):

parabolic
-------------------------------------------------------------------

``parabolic: (KHighestWeight->Parabolic)``

Short description: parabolic attached to KHighestWeight by Vogan algorithm

Defined in line number 369


.. _K_types_(KHighestWeight->[K_Type]):

K_types
-------------------------------------------------------------------

``K_types: (KHighestWeight->[K_Type])``

Short description: KHighestWeight -> array of K-types

Defined in line number 391


.. _K_type_(KHighestWeight->K_Type):

K_type
-------------------------------------------------------------------

``K_type: (KHighestWeight->K_Type)``

Short description: KHighestWeight -> unique K-type if unique (or error)

Defined in line number 428


.. _K0_highest_weight_(KHighestWeight->Param):

K0_highest_weight
-------------------------------------------------------------------

``K0_highest_weight: (KHighestWeight->Param)``

Short description: highest weight for K_0 to KHighestWeight

Defined in line number 437


.. _dimension_(KHighestWeight->int):

dimension
-------------------------------------------------------------------

``dimension: (KHighestWeight->int)``

Short description: dimension of KHighestWeight

Defined in line number 445


.. _dimension_(K_Type->int):

dimension
-------------------------------------------------------------------

``dimension: (K_Type->int)``

Short description: dimension of K-type

Defined in line number 448


