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
Borel subgroups containing the Compact Cartan. So, these parametrize
the discrete series of :math:`Sp(4, \mathbb R)` with a fixed
infinitesimal character. That is, if we fix :math:`x_b`,

.. math:: x=wx_b \rightarrow \text{discete series with Harish-Chandra parameter} \ w\rho.

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

Again, as in the example of :math:`SL(2,R)`, these all have
``lambda=rho`` and ``nu=0``. The only difference is the element
``x``. In order to identify them with the usual parameters that we
know we do the following. We first fix a base element
:math:`x_b`. This determines an identity component of :math:`K` and we set this as our :math:`K` ::

   atlas> set x_b=KGB(G,0)
   Variable x_b: KGBElt
   atlas> K_0(x_b)
   Value: compact connected real group with Lie algebra 'su(2).u(1)'
   atlas>
   atlas> set K=K_0(x_b)
   Variable K: RealForm
   atlas> 

which is the standard maximal compact subgroup of :math:`Sp(4,R)`. Now when we ask for the simple roots for this element we get::

   atlas> simple_roots (K)
   Value: 
   | 1 |
   | 1 |
   
   atlas>

Which is not the canonical set of simple roots. So we try different
elements until we get the simple roots we want::

   atlas> x_b:=KGB(G,1)
   Value: KGB element #1
   atlas> simple_roots (K_0(x_b))
   Value: 
   | 1 |
   | 1 |
   
   atlas> x_b:=KGB(G,2)
   Value: KGB element #2
   atlas> simple_roots (K_0(x_b))
   Value: 
   |  1 |
   | -1 |
   
   atlas>
 
So we fix ``x_b`` as our base element. And now with respect to this parameter we find the Harish-Chandra parameter for each of the other discrete series ::

   atlas> void: for p in ds do prints(p," ", hc_parameter(p,x_b)) od
   final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1) [  2, -1 ]/1
   final parameter(x=1,lambda=[2,1]/1,nu=[0,0]/1) [  1, -2 ]/1
   final parameter(x=2,lambda=[2,1]/1,nu=[0,0]/1) [ 2, 1 ]/1
   final parameter(x=3,lambda=[2,1]/1,nu=[0,0]/1) [ -1, -2 ]/1
   atlas> 

So, this is a way to go from ``atlas`` parameters to the
Harish-Chandra parameters expressed, in the usual way, with
respect to the fixed base element. The one corresponding to ``x=2`` is
the holomorphic discrete series, the one for ``x=3`` is the
antiholomorphic one and the other two are the large discrete series.

To chek this we do the following ::

   atlas> void: for p in ds do prints(p," ", hc_parameter(p,x_b)," ", status_texts(x(p))) od
   final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1) [  2, -1 ]/1 ["nc","nc"]
   final parameter(x=1,lambda=[2,1]/1,nu=[0,0]/1) [  1, -2 ]/1 ["nc","nc"]
   final parameter(x=2,lambda=[2,1]/1,nu=[0,0]/1) [ 2, 1 ]/1 ["ic","nc"]
   final parameter(x=3,lambda=[2,1]/1,nu=[0,0]/1) [ -1, -2 ]/1 ["ic","nc"]
   atlas>

So, this gives us more information about each representation. Namely, the status of the simple roots for the corresponding ``x``. 

The software always chooses, for the quasisplit group, ``x=0`` to be
the large Borel; that is, both of the simple roots are non compact. In
this case the simple roots are :math:`e_1 + e_2` and
:math:`2e_2`. Similarly, for ``x=1``. So these correspond to the large
discrete series.  And since we chose the base element to be ``x=2`` and
the simple root for :math:`K` is :math:`[1,-1]`, then ``[2,1]`` is the usual
parameter for this choice of simple roots. The first simple root is
compact. so this corresponds to the holomorphic case.

Now to go the other way we use::

   atlas> whattype discrete_series ?
   Overloaded instances of 'discrete_series'
     (KGBElt,ratvec)->Param
     (RealForm,ratvec)->Param
     atlas>
     
     atlas> discrete_series (G, [2,1])
     Value: final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1)
     atlas> discrete_series (G, [2,-1])
     Value: final parameter(x=2,lambda=[2,1]/1,nu=[0,0]/1)
     atlas>

Or we could use the other format using the ``KGBElt``::

   atlas> set p=discrete_series (x_b,[2,1])
   Variable p: Param
   atlas> p
   Value: final parameter(x=2,lambda=[2,1]/1,nu=[0,0]/1)
   atlas> p:=discrete_series (x_b,[1,-2])
   Value: final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1)
   atlas>
   atlas> p:=discrete_series (x_b,[2,-1])
   Value: final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1)
   
So, the software conjugates the Harish-Chandra parameter ``[1,-2]`` to ``[2,1]``
and conjugates, via the reflection on the long simple root, the base element to ``x=0``. 

To find the elements in W that do this we do the following::

   atlas> set W=generate_W (G)
   Variable W: [(RootDatum,[int])]
   atlas> #W
   Value: 8
   atlas> void: for w in W do prints(w) od
   simply connected root datum of Lie type 'C2'[]
   simply connected root datum of Lie type 'C2'[0]
   simply connected root datum of Lie type 'C2'[1]
   simply connected root datum of Lie type 'C2'[1,0]
   simply connected root datum of Lie type 'C2'[0,1]
   simply connected root datum of Lie type 'C2'[0,1,0]
   simply connected root datum of Lie type 'C2'[1,0,1]
   simply connected root datum of Lie type 'C2'[1,0,1,0]

This is the entire Weyl group of type ``C2`` in the form of a list of pairs ``root datum, product of simple roots, starting from the identity and ending in the long element of the Weyl group``. Now to find out how these elements act on ``x_b=2`` we do::


   atlas> void: for w in W do prints(cross(w,x_b)) od
   KGB element #2
   KGB element #2
   KGB element #0
   KGB element #0
   KGB element #1
   KGB element #1
   KGB element #3
   KGB element #3
   atlas> 

This lists the cross action of each element of :math:`W` on
``x_b=2``. The ``Id`` takes ``x=2`` to itself, the simple reflection by
root [0], which is the compact root, also fixes it. The other
simple root, ``[1]`` sends ``x=2`` to ``x=0`` and so on. 

Note that the action of :math:`W` on this set is transitive and the stabilizer of ``x_b`` is :math:`W_K`

Also, by contrast notice the action on the element ``x=10``::

   atlas> void: for w in W do prints(cross(w,KGB(G,10))) od
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   atlas> 

The action on the split Cartan is trivial. There is only one
:math:`K\backslash G/B` element and the stabilizer is the entire Weyl
group.


Now, recall the command to write the Harish-Chandra parameter in the
usual way::
 
   atlas> void: for p in ds do prints(p," ", hc_parameter(p,x_b)) od
   final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1) [  2, -1 ]/1
   final parameter(x=1,lambda=[2,1]/1,nu=[0,0]/1) [  1, -2 ]/1
   final parameter(x=2,lambda=[2,1]/1,nu=[0,0]/1) [ 2, 1 ]/1
   final parameter(x=3,lambda=[2,1]/1,nu=[0,0]/1) [ -1, -2 ]/1

and suppose we use ``x=0`` as our base point. Then we get a strange
set of parameters because the compact root is now ``[1,1]`` instead of
the usual one. So, the Harish-Chandrra parameters are not what we
expect::

   atlas> void: for p in ds do prints(p," ", hc_parameter(p,KGB(G,0))) od
   final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1) [ 2, 1 ]/1
   final parameter(x=1,lambda=[2,1]/1,nu=[0,0]/1) [ 1, 2 ]/1
   final parameter(x=2,lambda=[2,1]/1,nu=[0,0]/1) [  2, -1 ]/1
   final parameter(x=3,lambda=[2,1]/1,nu=[0,0]/1) [ -1,  2 ]/1
   atlas>

That is what we get if we decide to define our group where :math:`K`
is given by ``x=0``. The compact root in this case is ``[1,1]`` and if
you we start with ``[2,1]`` you apply the Weyl group, modulo the
action of :math:`W_K` to it, you get the above representatives.