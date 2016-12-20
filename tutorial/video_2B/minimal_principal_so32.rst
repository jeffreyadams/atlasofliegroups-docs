Example :math:`G=SO(3,2)`

Let's study the minimal principal series for this group> ::

   atlas> G:SO(3,2)
   Variable G: RealForm (overriding previous instance, which had type RealForm)
   atlas> set parameters=all_parameters_gamma (G, rho(G))
   Variable parameters: [Param] (overriding previous instance, which had type [Param])
   atlas> rho(G)
   Value: [ 3, 1 ]/2
   atlas> #parameters
   Value: 12
   atlas> void: for p in parameters do prints(p) od
   final parameter (x=0,lambda=[3,1]/2,nu=[0,0]/1)
   final parameter (x=1,lambda=[3,1]/2,nu=[0,0]/1)
   final parameter (x=2,lambda=[3,1]/2,nu=[1,-1]/2)
   final parameter (x=3,lambda=[3,1]/2,nu=[0,1]/2)
   final parameter (x=3,lambda=[3,3]/2,nu=[0,1]/2)
   final parameter (x=4,lambda=[3,1]/2,nu=[3,0]/2)
   final parameter (x=4,lambda=[5,1]/2,nu=[3,0]/2)
   final parameter (x=5,lambda=[3,1]/2,nu=[1,1]/1)
   final parameter (x=6,lambda=[3,1]/2,nu=[3,1]/2)
   final parameter (x=6,lambda=[5,1]/2,nu=[3,1]/2)
   final parameter (x=6,lambda=[3,3]/2,nu=[3,1]/2)
   final parameter (x=6,lambda=[5,3]/2,nu=[3,1]/2)
   atlas>

We are looking only at the minimal principal series. So we are for the
moment only interested in the last four representations corresponding
to the ``KGB`` element ``x=6``.

Let us look at the tau invariants for these standard
representations::

    atlas> void: for p in parameters do prints(p, " ", tau(p)) od
    final parameter (x=0,lambda=[3,1]/2,nu=[0,0]/1) []
    final parameter (x=1,lambda=[3,1]/2,nu=[0,0]/1) [1]
    final parameter (x=2,lambda=[3,1]/2,nu=[1,-1]/2) [0]
    final parameter (x=3,lambda=[3,1]/2,nu=[0,1]/2) [1]
    final parameter (x=3,lambda=[3,3]/2,nu=[0,1]/2) [1]
    final parameter (x=4,lambda=[3,1]/2,nu=[3,0]/2) [0]
    final parameter (x=4,lambda=[5,1]/2,nu=[3,0]/2) [0]
    final parameter (x=5,lambda=[3,1]/2,nu=[1,1]/1) [1]
    final parameter (x=6,lambda=[3,1]/2,nu=[3,1]/2) [0,1]
    final parameter (x=6,lambda=[5,1]/2,nu=[3,1]/2) [1]
    final parameter (x=6,lambda=[3,3]/2,nu=[3,1]/2) [1]
    final parameter (x=6,lambda=[5,3]/2,nu=[3,1]/2) [0,1]
    atlas> 

Now if we look again only at the last four parameters we see that two
of them have tau invariant ``[0,1]``. This is because they are both
one-dimensional representations. the group is disconnected and has two
one-dimensional representations. Each is equivalent to the other one
tenssor the sign representation. This interchanges the two
representations. And likewise, the two representations labeled with
the tau invariant ``[1]`` get interchanged.

Now let us look at composition series for one of those pairs of
representations ::

    atlas> p:parameters[11]
    Variable p: Param (overriding previous instance, which had type Param)
    atlas> show(composition_series(I(p)))
    1*J(x=0,lambda=[3/2,1/2],nu=[0/1,0/1])
    1*J(x=2,lambda=[3/2,1/2],nu=[1/2,-1/2])
    1*J(x=3,lambda=[3/2,1/2],nu=[0/1,1/2])
    1*J(x=3,lambda=[3/2,3/2],nu=[0/1,1/2])
    1*J(x=4,lambda=[5/2,1/2],nu=[3/2,0/1])
    1*J(x=5,lambda=[3/2,1/2],nu=[1/1,1/1])
    1*J(x=6,lambda=[5/2,3/2],nu=[3/2,1/2])
    atlas>

    atlas> p:parameters[8]
    Variable p: Param (overriding previous instance, which had type Param)
    atlas> show(composition_series(I(p)))
    1*J(x=0,lambda=[3/2,1/2],nu=[0/1,0/1])
    1*J(x=2,lambda=[3/2,1/2],nu=[1/2,-1/2])
    1*J(x=3,lambda=[3/2,1/2],nu=[0/1,1/2])
    1*J(x=3,lambda=[3/2,3/2],nu=[0/1,1/2])
    1*J(x=4,lambda=[3/2,1/2],nu=[3/2,0/1])
    1*J(x=5,lambda=[3/2,1/2],nu=[1/1,1/1])
    1*J(x=6,lambda=[3/2,1/2],nu=[3/2,1/2])
    atlas>


These are almost identical except the ``lambdas`` are different in
lines 5 and 7.

Similarly if we look at parameters 9 and 10 we have ::

    atlas> p:parameters[9]
    Variable p: Param (overriding previous instance, which had type Param)
    atlas> show(composition_series(I(p)))
    1*J(x=0,lambda=[3/2,1/2],nu=[0/1,0/1])
    1*J(x=1,lambda=[3/2,1/2],nu=[0/1,0/1])
    1*J(x=2,lambda=[3/2,1/2],nu=[1/2,-1/2])
    1*J(x=3,lambda=[3/2,3/2],nu=[0/1,1/2])
    1*J(x=4,lambda=[5/2,1/2],nu=[3/2,0/1])
    1*J(x=6,lambda=[5/2,1/2],nu=[3/2,1/2])
    atlas>
    
    atlas> p:parameters[10]
    Variable p: Param (overriding previous instance, which had type Param)
    atlas> show(composition_series(I(p)))
    1*J(x=0,lambda=[3/2,1/2],nu=[0/1,0/1])
    1*J(x=1,lambda=[3/2,1/2],nu=[0/1,0/1])
    1*J(x=2,lambda=[3/2,1/2],nu=[1/2,-1/2])
    1*J(x=3,lambda=[3/2,1/2],nu=[0/1,1/2])
    1*J(x=4,lambda=[3/2,1/2],nu=[3/2,0/1])
    1*J(x=6,lambda=[3/2,3/2],nu=[3/2,1/2])
    atlas>

