.. _K_highest_weights.at:

K_highest_weights.at
=====================================

Functions involving K-types (final tempered limit parameters) and K-highest weights.
The main reference is Vogan, "Branching to a Maximal Compact Subgroup" [KHatHowe].
See also the notes on "K-types in atlas" in dropbox.

The main functions are:

1) highest_weights: Given a K_type tau=(x,lambda), find all K-highest weights
corresponding to the K_#-types in the restriction of tau.

(x,lambda) -> {(x_K,mu)} multivalued; find one value (x_K,mu) is one value, then
take the R(K)-orbit <-> R(K)/R(K,mu) K-highest weights.

Algorithm:

i) If G is relatively split, Cartan is (relatively) split, all roots in the
tau-invariant, this is the "G-spherical" case of KHatHowe, section 8

ii) if p is final standard limit tempered, it has a unique LKT,
use theta_stable_data (see induction.at) to write p as cohomologically induced
from a relatively split L

iii) Apply ii) to all terms of finalize(p*0)


2) K_types: Given a KHighestWeight mu=(x,kappa), find all K_types containing
the corresponding K_#-type.

mu=(x_K,kappa) -> {(x,lambda)} multivalued; find :math:`\theta` -stable data
(Q=LU,p_L=(x_L,lambda_L,0)) for one K-type tau first, then
compute all (L-spherical) (L\cap K)-types p_L'=(x_L,lambda_L')
with the same infinitesimal character. There will be
|R(K,mu)| of them (the cardinality of the stabilizer of mu in the
R-group of K).

Algorithm:

This is the Vogan algorithm, version in [KHatHowe] Section 13, a
slight modification of Vogan's Big Green Book Prop. 5.3.3.

Given (x_K,kappa) -> kappa+2rho_K(x_K), choose positive chamber for G
-> kappa+2rho_K(x_K)-rho :math:`; project on the given dominant Weyl chamber -> xi;
then the simple roots contributing to difference between xi and
kappa +2rho_K-rho determine the ` \theta :math:`-stable parabolic Q=LU that is
part of the ` \theta :math:`-stable data for tau=(x,lambda). The parameter for
(relatively split) L is obtained from xi by a ` \rho$-shift.


**This script imported the following .at files:**

| :ref:`W_K.at<W_K.at>`
| :ref:`thetastable.at<thetastable.at>`
| :ref:`representations.at<representations.at>`
|


.. toctree::
   :maxdepth: 1

   K_highest_weights_index
   K_highest_weights_ref
