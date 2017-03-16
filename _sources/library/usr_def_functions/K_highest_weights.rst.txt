.. _K_highest_weights.at:

K_highest_weights.at
=====================================

Functions involving K-types (final tempered limit parameters) and K-highest weights.
The main reference is Vogan, "Branching to a Maximal Compact Subgroup" [KHatHowe].
See also the notes on "K-types in atlas" in the Dropbox.

The main functions are:

1) highest_weights: Given a K_type tau=(x,lambda), find all K-highest weights
corresponding to the K_#-types in the restriction of tau.

(x,lambda) -> {(x_K,mu)} multivalued; find one value (x_K,mu), then
take the R(K)-orbit <-> |R(K)/R(K,mu)| K-highest weights. Here R(K,mu) is
the stabilizer of mu in the R-group R(K) of K.

Algorithm:

i) If G is relatively split, Cartan is (relatively) split, all roots in the
tau-invariant, this is the "G-spherical" case of KHatHowe, Section 8.

ii) If p is final standard limit tempered, it has a unique LKT,
use theta_stable_data (see induction.at) to write p as cohomologically induced
from a relatively split L.

iii.) Apply ii) to all terms of finalize(p*0).


2) K_types: Given a KHighestWeight mu=(x,kappa), find all K_types containing
the corresponding K_#-type.

(x_K,mu) -> {tau=(x,lambda)} multivalued; find :math:`\theta` -stable data
(Q=LU,p_L=(x_L,lambda_L,0)) for one K-type tau first, then
compute all (L-spherical) :math:`(L\cap K)` -types p_L'=(x_L,lambda_L')
with the same infinitesimal character. There will be
|R(K,mu)| of them.

Algorithm:

This is the Vogan algorithm, version in [KHatHowe] Section 13, a
slight modification of Vogan's Big Green Book Prop. 5.3.3.

Given (x_K,mu), compute mu+2rho_K(x_K), choose positive chamber for G,
-> mu_0=mu+2rho_K(x_K)-rho; project on the given dominant Weyl chamber -> xi;
then the simple roots contributing to difference between xi and
mu_0 determine the :math:`\theta` -stable parabolic Q=LU that is
part of the :math:`\theta` -stable data for tau=(x,lambda). The parameter for
(relatively split) L is obtained from xi by a :math:`\rho` -shift.


**This script imports the following .at files:**

| :ref:`W_K.at<W_K.at>`
| :ref:`induction.at<induction.at>`
| :ref:`representations.at<representations.at>`
|


.. toctree::
   :maxdepth: 1

   K_highest_weights_ref
   K_highest_weights_index
