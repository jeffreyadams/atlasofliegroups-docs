Example :math:`SL(2,R)`
========================

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
to the compact Cartan. Note that they both have Harish-Chandra parameter
``lambda=rho``. This is because the software is using a different
``x``.   Remember that we have to fix a ``KGB`` element ``x_b``
to fix a real group :math:`K`. Let us fix it to be ``x=0``::

  atlas> set x_b=KGB(G,0)
   Variable x_b: KGBElt
   atlas> x_b
   Value: KGB element #0
   atlas>

Now, in order to identify the representation associated to ``x=1` with
a representation associated to ``x=0``, we need to conjugate ``x=1``
to ``x=0``. This will conjugate ``lambda`` to ``-lambda``.  Then the
harish chandra parameters of the discrete series with respect to the
fixed element ``x=0`` will be::

   atlas> hc_parameter(B[0],x_b)
   Value: [ 1 ]/1
   atlas> hc_parameter(B[1],x_b)
   Value: [ -1 ]/1
   atlas>

So, one is the holomorphic discrete series and the other is the anti
holomorphic one.  But by choosing ``x_b =1`` we get the opposite
situation for the Harish Chandra parameters and  holomorphic convention.




