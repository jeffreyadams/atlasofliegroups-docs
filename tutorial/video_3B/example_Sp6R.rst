Example :math:`Sp(6,\mathbb R)`
================================

Let us find the discrete series for this group::

   atlas> G:=Sp(6,R)
   Value: connected split real group with Lie algebra 'sp(6,R)'
   atlas> set F=distinguished_fiber (G)
   Variable F: [int]
   atlas> F
   Value: [0,1,2,3,4,5,6,7]
   atlas>

   atlas> ds:=all_discrete_series (G,rho(G)) Value: [final
   parameter(x=0,lambda=[3,2,1]/1,nu=[0,0,0]/1),final
   parameter(x=1,lambda=[3,2,1]/1,nu=[0,0,0]/1),final
   parameter(x=2,lambda=[3,2,1]/1,nu=[0,0,0]/1),final
   parameter(x=3,lambda=[3,2,1]/1,nu=[0,0,0]/1),final
   parameter(x=4,lambda=[3,2,1]/1,nu=[0,0,0]/1),final
   parameter(x=5,lambda=[3,2,1]/1,nu=[0,0,0]/1),final
   parameter(x=6,lambda=[3,2,1]/1,nu=[0,0,0]/1),final
   parameter(x=7,lambda=[3,2,1]/1,nu=[0,0,0]/1)] 

   atlas> show(ds)
   final parameter(x=0,lambda=[3,2,1]/1,nu=[0,0,0]/1)
   final parameter(x=1,lambda=[3,2,1]/1,nu=[0,0,0]/1)
   final parameter(x=2,lambda=[3,2,1]/1,nu=[0,0,0]/1)
   final parameter(x=3,lambda=[3,2,1]/1,nu=[0,0,0]/1)
   final parameter(x=4,lambda=[3,2,1]/1,nu=[0,0,0]/1)
   final parameter(x=5,lambda=[3,2,1]/1,nu=[0,0,0]/1)
   final parameter(x=6,lambda=[3,2,1]/1,nu=[0,0,0]/1)
   final parameter(x=7,lambda=[3,2,1]/1,nu=[0,0,0]/1)   

Again, like in the case of :math:`Sp(4,\mathbb R)` we can try to write
each parameter in terms of a single ``x`` that has the usual compact
simple roots. By looking at each ``x``.

A more efficient way to do this is the following::

   atlas> void: for i in F do prints(i," ",rho_K(KGB(G,i))) od
   0 [ 1, 1, 0 ]/1
   1 [ 1, 1, 0 ]/1
   2 [ 1, 0, 1 ]/1
   3 [ 1, 1, 0 ]/1
   4 [ 1, 1, 0 ]/1
   5 [  1,  0, -1 ]/1
   6 [ 1, 0, 1 ]/1
   7 [  1,  0, -1 ]/1
   atlas> 

We have two choices of ``x`` with the standard ``rho``: ``x=5`` and
``x=7``. We choose one::

   atlas> x_b:=KGB(G,5)
   Value: KGB element #5
   atlas> simple_roots(K_0(x_b))
   Value: 
   |  1,  0 |
   | -1,  1 |
   |  0, -1 |
   
   atlas>

   atlas> void: for p in ds do prints(x(p), " ", hc_parameter (p, x_b)) od
   KGB element #0 [  3,  1, -2 ]/1
   KGB element #1 [  2,  1, -3 ]/1
   KGB element #2 [  3,  2, -1 ]/1
   KGB element #3 [  3, -1, -2 ]/1
   KGB element #4 [  2, -1, -3 ]/1
   KGB element #5 [ 3, 2, 1 ]/1
   KGB element #6 [  1, -2, -3 ]/1
   KGB element #7 [ -1, -2, -3 ]/1
   atlas>

These ``lambdas`` are the conjugates of ``rho`` which are
:math:`K`-dominant. That is, modulo :math:`W_K`. They are all
decreasing. So they are the usual Harish-Candra parameters for the
eight discrete series of :math:`Sp(6,\mathbb R)`.

Now, as for previous examples we can write::

   atlas> p:=discrete_series (x_b,[-1,-2,-3])
   Value: final parameter(x=7,lambda=[3,2,1]/1,nu=[0,0,0]/1)
   atlas>

So ``atlas`` knows what this is and makes ``lambda`` dominant and conjugates ``x_b`` to ``x_7``.



