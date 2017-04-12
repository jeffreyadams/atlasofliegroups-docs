Discrete Series
================

Recall that there is a map :math:`\rho :\mathcal X\rightarrow
{\mathcal I}_W` (involutions in :math:`W`). And the conjugacy classes
of involutions in W give a map:

:math:`{\mathcal I}_W /W\leftrightarrow \text{conjugacy classes of
Cartans in quasisplit group.}`

Now let us fix :math:`x_b` and define the set

.. math:: \mathcal F := {\rho }^{-1}(Id)=\{x\in \mathcal X |x\in H \}

This is the distinguished fiber above the identity element in the Weyl
group or the identity involution in :math:`{\mathcal I}_W` this just
means that the elements in this preimage are in the Cartan :math:`H`. 

So, this :math:`\mathcal F` parametrizes the Borel subgroups
containing a compact Cartan up to conjugation by :math:`K`. And these
in turn parametrize the discrete series with fixed infinitesimal
character.

Explicitly, if we fix infinitesimal character :math:`\rho`,
:math:`x=wx_b`, corresponds to the discrete series with Harish Chandra
parameter :math:`w\rho`.

So when talking about representations associated to a non split
Cartan, the element :math:`x` not only gives you the Cartan but also a
:math:`K`-conjugacy class of Borels for that Cartan.

Now we can focus on the case when :math:`\theta _x` is acting by
:math:`Id` which corresponds to the discrete series representations.

In other words, assuming that :math:`G=G(\mathbb C)` has discrete
series representations is equivalent to having a distinguished
involution equal to the Identity.

Example :math:`Sp(4,R)`
-----------------------

There are a couple of commands that will give you discrete series::

   atlas> whattype discrete_series ?
   Overloaded instances of 'discrete_series'
     (KGBElt,ratvec)->Param
     (RealForm,ratvec)->Param
   atlas>
   atlas> 
   atlas> whattype all_discrete_series_gamma ?
   No overloads for 'all_discrete_series_gamma'
   atlas>