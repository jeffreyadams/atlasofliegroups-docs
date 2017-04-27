Example :math:`Sp(4,R)`
=======================

Let us find all the :math:`K\backslash G/B` elements of
:math:`Sp(2,\mathbb R)`::

   atlas> G:=Sp(4,R)
   Value: connected split real group with Lie algebra 'sp(4,R)'
   atlas> print_KGB (G)
   kgbsize: 11
   Base grading: [11].
    0:  0  [n,n]    1   2     4   5  (0,0)#0 e
    1:  0  [n,n]    0   3     4   6  (1,1)#0 e
    2:  0  [c,n]    2   0     *   5  (0,1)#0 e
    3:  0  [c,n]    3   1     *   6  (1,0)#0 e
    4:  1  [r,C]    4   9     *   *  (0,0) 1 1^e
    5:  1  [C,r]    7   5     *   *  (0,0) 2 2^e
    6:  1  [C,r]    8   6     *   *  (1,0) 2 2^e
    7:  2  [C,n]    5   8     *  10  (0,0)#2 1x2^e
    8:  2  [C,n]    6   7     *  10  (0,1)#2 1x2^e
    9:  2  [n,C]    9   4    10   *  (0,0)#1 2x1^e
   10:  3  [r,r]   10  10     *   *  (0,0)#3 1^2x1^e
   atlas>

The first four elements form the "distinguished fiber" :math:`\mathcal
F`. That is, those who, map to the (conjugacy class of) the identity
involution in the Weyl group. The ``0`` in the last collumn next to
the # sign tells us that these :math:`K\backslash G/B` elements are in
the Compact Cartan and, up to conjugacy by :math:`K`, parametrize the
Borel subgroups containing the Compact Cartan. so, these parametrize
the discrete series of :math:`Sp(4, \mathbb R)` with a fixed
infinitesimal character. That is, if we fix :math:`x_b`,

.. math:: x=wx_b \rightarrow \text{discete series with Harish-Chandra parameter} w\rho.

There are a couple of commands that will
give you discrete series::

   atlas> whattype discrete_series ?
   Overloaded instances of 'discrete_series'
     (KGBElt,ratvec)->Param
     (RealForm,ratvec)->Param
   atlas> 
   
   atlas> whattype all_discrete_series ?
   Overloaded instances of 'all_discrete_series'
     (RealForm,ratvec)->[Param]
   atlas> 

The first command deals with a single principal series. We want the last command that will list all discrete series with a fixed infinitesimal character. First let us setup a ``show`` function::

   atlas> set show([Param] params)=void:for p in params do prints(p) od
   Added definition [6] of show: ([Param]->)
   atlas>

Now we can list all the discrete series of :math:`G`::

   atlas> set ds=all_discrete_series (G,rho(G))
   Variable ds: [Param]
   atlas> show (ds)
   final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1)
   final parameter(x=1,lambda=[2,1]/1,nu=[0,0]/1)
   final parameter(x=2,lambda=[2,1]/1,nu=[0,0]/1)
   final parameter(x=3,lambda=[2,1]/1,nu=[0,0]/1)
   atlas>

Again, as in the example of :math:`SL(2,R)`, these all have the same
``lambda=rho`` and ``nu=0``. In order to identify them with the usual
parameters that we know we do the following. We first fix a base
element :math:`x_b`. this will determine an identity component of
:math:`K` ::

atlas> set x_b=KGB(G,0)
Variable x_b: KGBElt
atlas> K_0(x_b)
Value: compact connected real group with Lie algebra 'su(2).u(1)'
atlas>

Which is the maximal compact subgroup of :math:`Sp(4,R)`. Now we set this as our fixed :math:`K`. 



The last command lists all discrete series with the same parameters. The
only thing that is different is the element ``x``.




