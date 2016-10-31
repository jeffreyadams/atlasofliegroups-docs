.. _K_highest_weights.at:

K_highest_weights.at
=====================================

Functions involving K-types (final tempered limit parameters) and K-highest weights.
The main reference is Vogan, "Branching to a Maximal Compact Subgroup" [KHatHowe].
See also the notes on "K-types in atlas".

The main functions are

(x,lambda) -> {(x_K,mu)} multivalued,
(x_K,mu) is one value, then take the R(K)-orbit <-> R(K)/R(K,mu)

algorithm:
1) if G is relatively split, Cartan is (relatively) split, all roots in the
tau-invariant,
this is the "G-spherical" case of KHatHowe, section 8
2) if p is final standard limit tempered, it has a unique LKT,
use theta_stable_data to write p as cohomologically induced from a
relatively split L
3) apply 2) to all terms of finalize(p*0)

project vector mu on dominant cone (spanned by fundamental coweights)
algorithm from KHatHowe Section 13, modification of BGB Proposition 5.3.3
used in map from highest weights to LKT below


This is the Vogan algorithm, version in khatHowe Section 13,
which is a slight modification of BGB Proposition 5.3.3
given (x,mu) -> mu+2rho_K(x) ->
choose positive chamber for G -> mu+2rho_K(x)-rho
project on given dominant chamber
returns (x,mu+2rho_K(x)-rho,tau) where tau is dominant
need the second argument for the modified Vogan algorithm


**This script imported the following .at files:**

| :ref:`W_K.at<W_K.at>`
| :ref:`thetastable.at<thetastable.at>`
|


.. toctree::
   :maxdepth: 1

   K_highest_weights_index
   K_highest_weights_ref
