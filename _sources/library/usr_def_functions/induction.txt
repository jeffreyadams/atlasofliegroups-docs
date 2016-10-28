.. _induction.at:

induction.at
=====================================

Parabolic induction from real and :math:`\theta` -stable parabolics; cuspidal and
:math:`\theta` -stable data of a parameter.

If L is a :math:`\theta` -stable Levi subgroup of G, then KGB for L embeds into KGB for G.

For parabolic induction, a parameter p_L for the Levi L is assigned a parameter
p_G for G:

p_L=(x_L,lambda,nu) -> p_G=(embed_KGB(x_L,G),lambda + appropriate rho-shift,nu).

For real parabolic induction, the rho-shift is:
:math:`\rho_r(G)-\rho_r(L)+(1-\theta)(\rho_S(G)-\rho_S(L))` . (Here :math:`\rho_S`  is a certain
half sum of complex roots.)

For :math:`\theta` -stable induction, the rho-shift is:
:math:`\rho_i(G)-\rho_i(L)+\rho_{complex}(G)-\rho_{complex}(L)
=\rho(G)-\rho_r(G)-\rho(L)+\rho_r(L)` .
Since :math:`\mathfrak q`  is :math:`\theta`  -stable, :math:`\rho_r(G)-\rho_r(L)=0` , so the
shift is :math:`\rho(G)-\rho(L)=\rho(\mathfrak u)` .

Then :math:`\operatorname{Ind}_P^G I(p_L)=I(p_G)` .

In the :math:`\theta` -stable case, the shifted parameter p_G may be non-standard
and needs to be standardized:

If p=(x,lambda,nu), and :math:`\langle \text{lambda},\alpha^{\vee}\rangle <0`  for
some imaginary root :math:`\alpha`  (i.e. non-standard), let
i_root_system=imaginary roots for x(p). Find :math:`w`  so
that :math:`w^{-1}\cdot` lambda is dominant for imaginary roots, set
p_dom=parameter(x, :math:`w^{-1}\cdot` lambda,nu) and return coherent continuation action
(wrt imaginary roots) of :math:`w`  on p_dom.


**This script imported the following .at files:**

| :ref:`basic.at<basic.at>`
| :ref:`parabolics.at<parabolics.at>`
| :ref:`kl.at<kl.at>`
| :ref:`coherent.at<coherent.at>`
| :ref:`synthetic.at<synthetic.at>`
| :ref:`K.at<K.at>`
|


.. toctree::
   :maxdepth: 1

   induction_index
   induction_ref
