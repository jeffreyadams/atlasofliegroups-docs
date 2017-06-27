.. _K.at:

K.at
=====================================

Embedding of the complex group K defined by compact imaginary root system

:math:`T_{K_0}=(H^{\delta})_0 =`  Cartan subgroup of :math:`K_0` 
:math:`T_{K_0}\subset T_K=H^{\delta} \subset H` 
:math:`T_{K_0} is a torus in ` T_K :math:` abelian (possibly disconnected)
` X^*(T_{K_0})= X^*/(X^*)^{-\delta} :math:`
` X^*(T_K)    = X^*/(1-\delta)X^* \twoheadrightarrow X^*(T_{K_0}) :math:`
(restriction map is surjective)
see W_K.at

K_0=identity component of K, with Cartan subgroup T_K0
B=basis of X_*(T_K0) (as columns) = cocharacter lattice for (K_0,T_K0)
returns a matrix B with rank(K_0) columns, rank(ic) rows
columns are a basis of the +1 left-eigenspace delta

This matrix ` B :math:` satisfies ` ^\delta*B=B :math:`
left multiplication by ` ^B :math:` is
projection ` X^*(H)  -> X^*(T_{K_0}) = X^*(H)/X^*(H)^{-\delta} :math:`
left multiplication by  ` B :math:` is
injection  ` X_*(T_{K_0})-> X_*(H) :math:`   [` ^\delta*v=v :math:` for ` v$ in image]


**This script imports the following .at files:**

| :ref:`sort.at<sort.at>`
| :ref:`matrix.at<matrix.at>`
| :ref:`Weylgroup.at<Weylgroup.at>`
|


.. toctree::
   :maxdepth: 1

   K_ref
   K_index
