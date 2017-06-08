Example :math:`G=PSL(2,\mathbb R)`
-----------------------------------

Another group we can look at is::

   atlas> G:PSL(2,R)
   Variable G: RealForm (overriding previous instance, which had type RealForm)
   atlas> G
   Value: disconnected split real group with Lie algebra 'sl(2,R)'
   atlas>

Here the complex Lie group is :math:`G(\mathbb C )=PSL(2,\mathbb C
)=SL(2,\mathbb C)/{\pm 1}`. Its real points are disconnected, and they
are the group :math:`PSL(2, \mathbb R ) \cong SO(2,1)`::

  atlas> rho(G)
  Value: [ 1 ]/2
  atlas> set parameters=all_parameters_gamma (G,rho(G))
  Variable parameters: [Param] (overriding previous instance, which had type [Param])
  atlas>

Note we can use ``rho(G)`` instead of the vector value for
:math:`\rho\ `.  The parameters for this group are almost like those
for :math:`SL(2,\mathbb R)`, except that the Weyl group of the compact
Cartan subgroup has changed and the number of parameters is now just three::

    atlas> #parameters
    Value: 3
    atlas> void: for p in parameters do prints(p) od
    final parameter (x=0,lambda=[1]/2,nu=[0]/1)
    final parameter (x=1,lambda=[1]/2,nu=[1]/2)
    final parameter (x=1,lambda=[3]/2,nu=[1]/2)
    atlas>

We still have two principal series with infinitesimal character
:math:`\rho`. But we now only have one discrete series representation
associated to the compact Cartan subgroup, namely the sum of the two discrete
series for :math:`SL(2,\mathbb R)` are now a single irreducible
representation of :math:`PSL(2, \mathbb R )`.

Now let us look at the trivial representation ::

   atlas> p:trivial(G)
   Variable p: Param
   atlas> p
   atlas> dimension (p)
   Value: 1
   atlas>

One thing to have in mind is that the trivial representation is
 always given by the maximal number ``x`` and ``lambda=nu=rho``

This parameter has composition series::

   Value: final parameter (x=1,lambda=[1]/2,nu=[1]/2)
   atlas> composition_series(I(p))
   Value: (
   1*final parameter (x=0,lambda=[1]/2,nu=[0]/1)
   1*final parameter (x=1,lambda=[1]/2,nu=[1]/2),"irr")
   atlas>

Actually it is best to use the command ``show(composition_series(I(p))))`` ::

   atlas> show(composition_series(I(p)))
   1*J(x=0,lambda=[1/2],nu=[0/1])
   1*J(x=1,lambda=[1/2],nu=[1/2])
   atlas>

So, this induced representation for :math:`PSL(2,\mathbb R )` has two
factors: the trivial representation (with ``x=1`` and
:math:`\lambda=\nu=\rho` ) and a discrete series (with ``x=0``).

What is the other principal series attached to the split Cartan subgroup?  For
:math:`SL(2,\mathbb R )` the other representation attached to the
split Cartan subgroup was an infinite demensional irreducible principal
series. However here we have::

   atlas> q:parameters[2]
   Variable q: Param
   atlas> q
   Value: final parameter (x=1,lambda=[3]/2,nu=[1]/2)
   atlas> is_finite_dimensional (q)
   Value: true
   atlas> p=q
   Value: false
   atlas>
   atlas> p
   Value: final parameter (x=1,lambda=[1]/2,nu=[1]/2)
   atlas> q
   Value: final parameter (x=1,lambda=[3]/2,nu=[1]/2)
   atlas>

This is another one dimensional representation of G not equivalent to
the trivial representation. Recall that :math:`PSL (2,\mathbb R )` is
disconnected, so ``q`` is the parameter for the sign
representation. In other words the standard module attached to this
parameter is a principal series which has as its unique irreducible
quotient the sign representation of :math:`PSL (2,\mathbb R )`.

Now for another example::

   atlas> set p=parameter(KGB(G,1),[1]/2,[1])
   Variable p: Param
   atlas> p
   Value: final parameter (x=1,lambda=[1]/2,nu=[1]/1)
   atlas> show(composition_series (I(p)))
   1*J(x=1,lambda=[1/2],nu=[1/1])
   atlas>

So, the composition series gives an irreducible. Even though ``nu``
is an integer this is not an irreducibility point.


