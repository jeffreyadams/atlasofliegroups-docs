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

 
Example :math:`SL(2,R)`
-----------------------
 
Recall the :math:`K\backslash G/B` elements of :math:`SL(2,R)`::

atlas> set G=SL(2,R)
   Variable G: RealForm
   atlas> G
   Value: connected split real group with Lie algebra 'sl(2,R)'
   atlas>
   atlas> print_KGB (G)
   kgbsize: 3
   Base grading: [1].
   0:  0  [n]   1    2  (0)#0 e
   1:  0  [n]   0    2  (1)#0 e
   2:  1  [r]   2    *  (0)#1 1^e
   atlas>

If we again look at the block of the trivial ::

   atlas> set B=block_of (trivial (G))
   Variable B: [Param]
   atlas> set show([Param] params)= void: for p in params do prints(p) od
   Added definition [6] of show: ([Param]->)
   atlas> show(B)
   final parameter (x=0,lambda=[1]/1,nu=[0]/1)
   final parameter (x=1,lambda=[1]/1,nu=[0]/1)
   final parameter (x=2,lambda=[1]/1,nu=[1]/1)
   atlas>

We focus on the first two elements::

   atlas> B[0]
   Value: final parameter (x=0,lambda=[1]/1,nu=[0]/1)
   atlas> B[1]
   Value: final parameter (x=1,lambda=[1]/1,nu=[0]/1)
   atlas>

Recall that these are the (discrete series) representations associated
to the compact Cartan. Note that they both have parameter
``lambda=rho``. This is because the software is using a different
``x``. In order to understand which representation is which, we need
to conjugate ``x=1`` to ``x=0``. This will conjugate ``lambda`` to
``-lambda``.  Remember that we have to fix a ``KGB`` element ``x_b``
to fix a real group :math:`K`. Let us fix it to be ``x=0``::

   atlas> set x_b=KGB(G,0)
   Variable x_b: KGBElt
   atlas> x_b
   Value: KGB element #0
   atlas>

Then the harish chandra parameters of the discrete series with respect
to the fixed element ``x=0`` will be:: 

   atlas> hc_parameter(B[0],x_b)
   Value: [ 1 ]/1 
   atlas> hc_parameter(B[1],x_b) 
   Value: [ -1 ]/1 
   atlas>

But by choosing ``x_b =1`` we get the opposite situation for the Harish Chandra parameters. 

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