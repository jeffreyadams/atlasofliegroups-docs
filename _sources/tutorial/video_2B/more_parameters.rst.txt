More parameter commands
========================

Principal series commands
--------------------------
There is another command which we will use here to look at more
examples of minimal principal series. Namely, in addition to the
command ``all_minimal_principal_series``, the command
``minimal_principal_series`` helps us identify a particular
representation in the series. Let us compare their use with some
examples::

   atlas> set G=Sp(4,R)
   Variable G: RealForm
   atlas> whattype minimal_principal_series ?
   Overloaded instances of 'minimal_principal_series'
     (RealForm,ratvec,ratvec)->Param
     RealForm->Param

We will use the first syntax above::

   atlas> minimal_principal_series(G,rho(G),rho(G))
   Value: final parameter (x=10,lambda=[2,1]/1,nu=[2,1]/1)
   atlas>
   atlas> minimal_principal_series(G,rho(G),[0,0])
   Value: final parameter (x=10,lambda=[2,1]/1,nu=[0,0]/1)

So we get the single trivial or the representation with ``nu=0``. Now,
recall that for the first command, we need to provide a real form and
a rational vector::

   atlas> whattype all_minimal_principal_series ?
   Overloaded instances of 'all_minimal_principal_series'
     (RealForm,ratvec)->[Param]
   atlas> 

   atlas> set ps= all_minimal_principal_series (G,rho(G))
   Variable ps: [Param]
   atlas>

   atlas> void: for p in ps do prints(p) od
   final parameter (x=10,lambda=[2,1]/1,nu=[2,1]/1)
   final parameter (x=10,lambda=[3,1]/1,nu=[2,1]/1)
   final parameter (x=10,lambda=[2,2]/1,nu=[2,1]/1)
   final parameter (x=10,lambda=[3,2]/1,nu=[2,1]/1)
   atlas> 

So, in this case we obtain again the four principal series of
:math:`Sp(4,R)` at infinitesimal character ``rho``.

The ``nus`` all equal ``rho`` and the ``lambdas`` are all the possible lambdas in :math:`X^*/2X^*`.

Note that the group does not have to be semisimple::

   atlas> G:=GL(2,R)
   Value: disconnected split real group with Lie algebra 'sl(2,R).gl(1,R)'
   atlas> set ps= all_minimal_principal_series (G,rho(G))
   Variable ps: [Param] (overriding previous instance, which had type [Param])
   atlas> void: for p in ps do prints(p) od
   final parameter(x=1,lambda=[1,-1]/2,nu=[1,-1]/2)
   final parameter(x=1,lambda=[3,-1]/2,nu=[1,-1]/2)
   final parameter(x=1,lambda=[1,1]/2,nu=[1,-1]/2)
   final parameter(x=1,lambda=[3,1]/2,nu=[1,-1]/2)
   atlas> 

WARNING: This command does not work for non-split groups::

   atlas> G:=U(2,2)
   Value: connected quasisplit real group with Lie algebra 'su(2,2).u(1)'
   atlas> set ps= all_minimal_principal_series (G,rho(G))
   group is not split
   (in call at atlas-scripts/basic.at:8:57-71 of error@string, built-in)
     [b=false, message="group is not split"]
   (in call at atlas-scripts/all_parameters.at:109:4-44 of assert@(bool,string),
     defined at atlas-scripts/basic.at:8:4-74)
     [G=connected quasisplit real group with Lie algebra 'su(2,2).u(1)', gamma=
       [ 3,  1, -1, -3 ]/2]
     (in call at <standard input>:5:7-45 of all_minimal_principal_series@(RealForm,
       ratvec), defined at atlas-scripts/all_parameters.at:108:4--110:63)
     Command 'set ps' interrupted, nothing defined.
   atlas>


``all_parameters_gamma``
------------------------

For this group we need to use the command that lists all
representations with a given parameter for :math:`G` ::

   atlas> G:=U(2,2)
   Value: connected quasisplit real group with Lie algebra 'su(2,2).u(1)'
   atlas> set params=all_parameters_gamma (G,rho(G))
   Variable params: [Param] (overriding previous instance, which had type [Param])
   atlas> #params
   Value: 21
   atlas>
   atlas> void: for p in params do prints(p) od
   final parameter(x=20,lambda=[3,1,-1,-3]/2,nu=[3,1,-1,-3]/2)
   final parameter(x=19,lambda=[3,1,-1,-3]/2,nu=[3,0,0,-3]/2)
   final parameter(x=18,lambda=[3,1,-1,-3]/2,nu=[3,0,0,-3]/2)
   final parameter(x=17,lambda=[3,1,-1,-3]/2,nu=[1,1,-1,-1]/1)
   final parameter(x=16,lambda=[3,1,-1,-3]/2,nu=[1,0,-1,0]/1)
   final parameter(x=15,lambda=[3,1,-1,-3]/2,nu=[1,0,-1,0]/1)
   final parameter(x=14,lambda=[3,1,-1,-3]/2,nu=[0,1,0,-1]/1)
   final parameter(x=13,lambda=[3,1,-1,-3]/2,nu=[0,1,0,-1]/1)
   final parameter(x=12,lambda=[3,1,-1,-3]/2,nu=[1,-1,1,-1]/2)
   final parameter(x=11,lambda=[3,1,-1,-3]/2,nu=[1,-1,0,0]/2)
   final parameter(x=10,lambda=[3,1,-1,-3]/2,nu=[1,-1,0,0]/2)
   final parameter(x=9,lambda=[3,1,-1,-3]/2,nu=[0,1,-1,0]/2)
   final parameter(x=8,lambda=[3,1,-1,-3]/2,nu=[0,1,-1,0]/2)
   final parameter(x=7,lambda=[3,1,-1,-3]/2,nu=[0,0,1,-1]/2)
   final parameter(x=6,lambda=[3,1,-1,-3]/2,nu=[0,0,1,-1]/2)
   final parameter(x=5,lambda=[3,1,-1,-3]/2,nu=[0,0,0,0]/1)
   final parameter(x=4,lambda=[3,1,-1,-3]/2,nu=[0,0,0,0]/1)
   final parameter(x=3,lambda=[3,1,-1,-3]/2,nu=[0,0,0,0]/1)
   final parameter(x=2,lambda=[3,1,-1,-3]/2,nu=[0,0,0,0]/1)
   final parameter(x=1,lambda=[3,1,-1,-3]/2,nu=[0,0,0,0]/1)
   final parameter(x=0,lambda=[3,1,-1,-3]/2,nu=[0,0,0,0]/1)
   atlas> 

Recall that all Cartan subgroups of :math:`U(2,2)` are connected. And we can find the information on the Cartan subgroup associated to each parameter as follows :: 

   atlas> p:=trivial(G)
   Value: final parameter(x=20,lambda=[3,1,-1,-3]/2,nu=[3,1,-1,-3]/2)
   atlas>
   atlas> H:=Cartan_class(p)
   Value: Cartan class #2, occurring for 1 real form and for 2 dual real forms
   atlas>
   atlas> print_Cartan_info (H)
   compact: 0, complex: 2, split: 0
   canonical twisted involution: 2,1,3,2
   twisted involution orbit size: 3; fiber size: 1; strong inv: 3
   imaginary root system: empty
   real root system: A1.A1
   complex factor: A1
   atlas>

This is the most split Cartan subgroup in :math:`U(2,2)`. It is just
two copies of :math:`{\mathbb C}^x`. So it is connected. In fact this
group has three minimal principal series (with ``x=17`` and ``x=12``)
not comming from the disconnectedness of the Cartan subgroup but from
the Weyl group. We will address this later.


``all_parameters``
-------------------

This command helps us find representations with the same differential ::

   atlas> G:=Sp(4,R)
   Value: connected split real group with Lie algebra 'sp(4,R)'
   atlas> set params=all_parameters_gamma (G,rho(G))
   Variable params: [Param] (overriding previous instance, which had type [Param])
   atlas> void: for p in params do prints(p) od
   final parameter(x=10,lambda=[2,1]/1,nu=[2,1]/1)
   final parameter(x=10,lambda=[3,1]/1,nu=[2,1]/1)
   final parameter(x=10,lambda=[2,2]/1,nu=[2,1]/1)
   final parameter(x=10,lambda=[3,2]/1,nu=[2,1]/1)
   final parameter(x=9,lambda=[2,1]/1,nu=[3,3]/2)
   final parameter(x=8,lambda=[2,1]/1,nu=[2,0]/1)
   final parameter(x=8,lambda=[3,1]/1,nu=[2,0]/1)
   final parameter(x=7,lambda=[2,1]/1,nu=[2,0]/1)
   final parameter(x=7,lambda=[3,1]/1,nu=[2,0]/1)
   final parameter(x=6,lambda=[2,1]/1,nu=[0,1]/1)
   final parameter(x=6,lambda=[2,2]/1,nu=[0,1]/1)
   final parameter(x=5,lambda=[2,1]/1,nu=[0,1]/1)
   final parameter(x=5,lambda=[2,2]/1,nu=[0,1]/1)
   final parameter(x=4,lambda=[2,1]/1,nu=[1,-1]/2)
   final parameter(x=3,lambda=[2,1]/1,nu=[0,0]/1)
   final parameter(x=2,lambda=[2,1]/1,nu=[0,0]/1)
   final parameter(x=1,lambda=[2,1]/1,nu=[0,0]/1)
   final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1)
   atlas>
   atlas> p:=params[8]
   Value: final parameter(x=7,lambda=[3,1]/1,nu=[2,0]/1)
   atlas> set others=all_parameters (p)
   Variable others: [Param] (overriding previous instance, which had type [Param])
   atlas> void: for p in others do prints(p) od
   final parameter(x=7,lambda=[3,1]/1,nu=[2,0]/1)
   final parameter(x=7,lambda=[2,1]/1,nu=[2,0]/1)
   atlas> void: for q in others do prints(q) od
   final parameter(x=7,lambda=[3,1]/1,nu=[2,0]/1)
   final parameter(x=7,lambda=[2,1]/1,nu=[2,0]/1)
   atlas>

This Cartan subgroup has two connected components. So if you hand in a parameter for this subgroup, the total number of parameters with the same differential is two and this command gives the list of all of them