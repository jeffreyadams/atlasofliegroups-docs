.. _kgp.at_ref:

kgp.at Function References
=======================================================
|

.. _sort_by_(kgbelt_->_int)_f->([kgbelt]_v)_[kgbelt]1:

sort_by
-------------------------------------------------
| ``sort_by:(KGBElt -> int) f->([KGBElt] v) [KGBElt]`` Defined in line number 51.
| 
| Given a list of KGB elements and a function f assigning integers to them, sort the list by weakly increasing value of f
| 

.. _kgp_elt_kgpelt_pair->kgpelt1:

KGP_elt
-------------------------------------------------
| ``KGP_elt:KGPElt pair->KGPElt`` Defined in line number 65.
| 
| 

.. _s_kgpelt(s,)->[int]1:

S
-------------------------------------------------
| ``S:KGPElt(S,)->[int]`` Defined in line number 68.
| 
| The list S of simple roots of a KGP element
| 

.. _root_datum_kgpelt(,x)->rootdatum1:

root_datum
-------------------------------------------------
| ``root_datum:KGPElt(,x)->RootDatum`` Defined in line number 71.
| 
| The root datum of the RealForm G of a KGP element
| 

.. _real_form_kgpelt(,x)->realform1:

real_form
-------------------------------------------------
| ``real_form:KGPElt(,x)->RealForm`` Defined in line number 74.
| 
| The RealForm G of a KGP element
| 

.. _complement_int_n,[int]_s->[int]1:

complement
-------------------------------------------------
| ``complement:int n,[int] S->[int]`` Defined in line number 77.
| 
| Complement of subset of simple roots in rank n
| 

.. _find_ascent_[int]_s,_kgbelt_x->[kgbelt]1:

find_ascent
-------------------------------------------------
| ``find_ascent:[int] S, KGBElt x->[KGBElt]`` Defined in line number 81.
| 
| An ascent of x by a generator in S, if any exist
| 

.. _down_neighbors_[int]_s,kgbelt_x->[int]1:

down_neighbors
-------------------------------------------------
| ``down_neighbors:[int] S,KGBElt x->[int]`` Defined in line number 89.
| 
| All descents of x by generators in S, there may be duplicates
| 

.. _is_maximal_in_partial_order_[int]_s,kgbelt_x->bool1:

is_maximal_in_partial_order
-------------------------------------------------
| ``is_maximal_in_partial_order:[int] S,KGBElt x->bool`` Defined in line number 100.
| 
| Decide whether x is maximal in the partial order defined by S
| 

.. _maxima_in_partial_order_realform_g,[int]_s->[kgbelt]1:

maxima_in_partial_order
-------------------------------------------------
| ``maxima_in_partial_order:RealForm G,[int] S->[KGBElt]`` Defined in line number 103.
| 
| List maximal KGB elements in the partial order defined by S
| 

.. _maximal_[int]_s,_kgbelt_x->kgbelt1:

maximal
-------------------------------------------------
| ``maximal:[int] S, KGBElt x->KGBElt`` Defined in line number 109.
| 
| (unique) maximal element in equivalence class of x
| 

.. _canonical_representative_kgpelt_y->kgpelt1:

canonical_representative
-------------------------------------------------
| ``canonical_representative:KGPElt y->KGPElt`` Defined in line number 114.
| 
| The representative of a KGP element with maximal x
| 

.. _\=_KGPElt_(S,x),KGPElt_(T,y)->bool1:

\=
-------------------------------------------------
| ``=:KGPElt (S,x),KGPElt (T,y)->bool`` Defined in line number 121.
| 
| Equality of KGP elements: (S,x)=(T,y) if these give the same K-orbit of parabolics
| 

.. _equivalence_class_of_kgpelt(s,x):y->[kgbelt]1:

equivalence_class_of
-------------------------------------------------
| ``equivalence_class_of:KGPElt(S,x):y->[KGBElt]`` Defined in line number 126.
| 
| The equivalence class of a KGB element in partial order defined by S
| 

.. _x_min_kgpelt_p->kgbelt1:

x_min
-------------------------------------------------
| ``x_min:KGPElt P->KGBElt`` Defined in line number 141.
| 
| A minimal KGB element from an equivalence class defined by S (unlike x_max, it is not unique)
| 

.. _kgp_realform_g,[int]_s->[kgpelt]1:

KGP
-------------------------------------------------
| ``KGP:RealForm G,[int] S->[KGPElt]`` Defined in line number 146.
| 
| The set of KGP elements associated to a RealForm and a set of simple roots S; KGP(G,S) is in bijection with :math:`K\backslash G/P_S` 
| 

.. _kgp_numbers_realform_g,[int]_s->[int]1:

KGP_numbers
-------------------------------------------------
| ``KGP_numbers:RealForm G,[int] S->[int]`` Defined in line number 150.
| 
| Just the index numbers (maximal x) of KGP(G,S)
| 

.. _is_open_kgpelt_y->bool1:

is_open
-------------------------------------------------
| ``is_open:KGPElt y->bool`` Defined in line number 155.
| 
| Test whether y in :math:`K\backslash G/P_S`  is open: <=> last element of y is last element of KGB
| 

.. _is_closed_kgpelt_p->bool1:

is_closed
-------------------------------------------------
| ``is_closed:KGPElt P->bool`` Defined in line number 158.
| 
| Test whether y in :math:`K\backslash G/P_S`  is closed: <=> length(first element)=0
| 

.. _kgp_elt_ratvec_lambda,kgbelt_x->kgpelt1:

KGP_elt
-------------------------------------------------
| ``KGP_elt:ratvec lambda,KGBElt x->KGPElt`` Defined in line number 161.
| 
| Parabolic determined by (the stabilizer in W of) a weight lambda
| 

.. _KGPElt:

KGPElt
-----------------------------------------
| ``([int], KGBElt)`` Defined in line number 46.
| 
| 

.. _Parabolic:

Parabolic
-----------------------------------------
| ``([int], KGBElt)`` Defined in line number 47.
| 
| 

