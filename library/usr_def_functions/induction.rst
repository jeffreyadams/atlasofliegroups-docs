.. _induction.at:

induction.at
=====================================

Parabolic induction from real and :math:`\theta` -stable parabolics; cuspidal and
:math:`\theta` -stable data of a parameter, and some functions related to :math:`\theta` -stable parabolics.

Parabolic induction:
_________________________

| If L is a :math:`\theta` -stable Levi subgroup of G, then KGB for L embeds into KGB for G.
| For parabolic induction, a parameter p_L for the Levi L is assigned a parameter p_G for G:
|
| p_L=(x_L,lambda,nu) -> p_G=(embed_KGB(x_L,G),lambda + appropriate rho-shift,nu).
|
| For real parabolic induction, the rho-shift is: :math:`\rho_r(G)-\rho_r(L)+(1-\theta)(\rho_S(G)-\rho_S(L))` .
| (Here :math:`\rho_S`  is a certain half sum of complex roots.)
|
| For :math:`\theta` -stable induction, the rho-shift is:
| :math:`\rho_i(G)-\rho_i(L)+\rho_{complex}(G)-\rho_{complex}(L)  =\rho(G)-\rho_r(G)-\rho(L)+\rho_r(L)` .
|  Since :math:`\mathfrak q`  is :math:`\theta`  -stable, :math:`\rho_r(G)-\rho_r(L)=0` , so the shift is :math:`\rho(G)-\rho(L)=\rho(\mathfrak u)` .
| Then :math:`\operatorname{Ind}_P^G I(p_L)=I(p_G)` .
| In the :math:`\theta` -stable case, the shifted parameter p_G may be non-standard and needs to be standardized:
| If p=(x,lambda,nu), and :math:`\langle \text{lambda},\alpha^{\vee}\rangle <0`  for some imaginary root :math:`\alpha`  (i.e. non-standard),
| let i_root_system=imaginary roots for x(p). Find :math:`w`  so that :math:`w^{-1}\cdot` lambda is dominant for
| imaginary roots, set p_dom=parameter(x, :math:`w^{-1}\cdot` lambda,nu) and return coherent continuation
| action (wrt imaginary roots) of :math:`w`  on p_dom.

:math:`A_q(\lambda)`  construction:
_______________________________

| Note: theta_induce_irreducible(pi_L,G) has infinitesimal character:
| infinitesimal character(pi_L)+rho(u).
| Aq(x,lambda,lambda_q) is defined as follows:
| if lambda_q is weakly dominant set q=q(x,lambda_q),
| apply derived functor to the one-dimensional lambda-rho(u) of L.
|
| REQUIRE: lambda-rho(u) must be in X^*.
|
| Aq(x,lambda,lambda_q) has infinitesimal character lambda+rho_L,
| thus the one-dimensional with weight lambda has infinitesimal character
| lambda+rho_L for L, and goes to a representation with
| infinitesimal character lambda+rho_L for G; i.e., Aq takes infinitesimal
| character gamma_L to SAME infinitesimal character for G.
| If lambda_q is not weakly dominant, define
| Aq(x,lambda,lambda_q)=Aq(wx,w\lambda,w\lambda_q),
| where w\lambda_q is weakly dominant.
|

Good/Fair conditions:
________________________

| Condition on the roots of :math:`\mathfrak u` :
| For theta_induce(pi_L,G), gamma_L -> gamma_G=gamma_L+rho_u.
| Then:
| GOOD:  <gamma_L+rho_u,alpha^vee> > 0;
| WEAKLY GOOD:  <gamma_L+rho_u,alpha^vee> \ge 0;
| FAIR: <gamma_L-rho_L+rho_u,alpha^vee> > 0.
|
| For  Aq(x,lambda,lambda_q): gamma_L=lambda+rho_L;
| gamma_L -> gamma_G=gamma_L = lambda+rho_L
| Aq(x,lambda)=theta_induce(x,lambda-rho_u)
| Then:
| GOOD: <lambda+rho_L,alpha^vee> > 0;
| WEAKLY GOOD: <lambda+rho_L,alpha^vee> >= 0;
| FAIR: <lambda,alpha^vee> > 0;
| WEAKLY FAIR: <lambda,alpha^vee> \ge 0.
|
| theta_induce(pi_L,G) = Euler-Poincare characteristic of the
| cohomological induction functor.
|
| fair => vanishing outside middle degree => honest representation
| weakly fair: same implication.
| NB: <gamma_L-rho_L_rho_u,alpha^vee> >= 0 does NOT imply vanishing (in general) if pi_L is not
| one-dimensional, hence "weakly fair" is only defined if pi_L is one-dimensional.


**This script imports the following .at files:**

| :ref:`misc.at<misc.at>`
| :ref:`parabolics.at<parabolics.at>`
| :ref:`kl.at<kl.at>`
| :ref:`coherent.at<coherent.at>`
| :ref:`synthetic.at<synthetic.at>`
| :ref:`K.at<K.at>`
| :ref:`finite_dimensional.at<finite_dimensional.at>`
|


.. toctree::
   :maxdepth: 1

   induction_ref
   induction_index
