More on minimal pricipal series.
=================================

There is another command which we will use here to look at more
examples of minimal principal series. Namely, in addition to the
command ``all_minimal_principal_series``, the command
``minimal_principal_series`` help us identify a particular
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

So we get the single trivial or the representation with ``nu=0``. Now, recall that with the first command, we need to provide a real form and a rational vector::

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

The ``nus`` are all ``rho`` and the ``lambdas`` are all possible lambdas in :math:`X^*/2X^*`.

The group does not have to be semisimple::

   atlas> G:=GL(2,R)
   Value: disconnected split real group with Lie algebra 'sl(2,R).gl(1,R)'
   atlas> set ps= all_minimal_principal_series (G,rho(G))
   Variable ps: [Param] (overriding previous instance, which had type [Param])
   atlas> void: for p in ps do prints(p) od
   final parameter (x=1,lambda=[1,-1]/2,nu=[1,-1]/2)
   final parameter (x=1,lambda=[3,-1]/2,nu=[1,-1]/2)
   final parameter (x=1,lambda=[1,1]/2,nu=[1,-1]/2)
   final parameter (x=1,lambda=[3,1]/2,nu=[1,-1]/2)

Also, :math:`G` does not have to be split either::

   atlas> G=U(2,2)
   Value: false
   atlas> G:=U(2,2)
   Value: connected quasisplit real group with Lie algebra 'su(2,2).u(1)'
   atlas> set ps= all_minimal_principal_series (G,rho(G))
   Variable ps: [Param] (overriding previous instance, which had type [Param])
   atlas> #ps
   Value: 3
   atlas> 
   atlas> void: for p in ps do prints(p) od
   final parameter (x=12,lambda=[3,1,-1,-3]/2,nu=[1,-1,1,-1]/2)
   final parameter (x=17,lambda=[3,1,-1,-3]/2,nu=[1,1,-1,-1]/1)
   final parameter (x=20,lambda=[3,1,-1,-3]/2,nu=[3,1,-1,-3]/2)

Recall the all Cartan subgroups of :math:`U(2,2)` are connected. And we can find the information on the Cartan subgroup associated to each parameter as follows:: 

   atlas> set p=ps[0]
   Variable p: Param
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

This is the most split Cartan subgroup in :math:`U(2,2)`. It is just two copies
of :math`{\mathbb C}^x. So it is connected. In fact this group has
three minimal principal series not comming from the disconnectedness
of the Cartan subgroup but from the Weyl group. We will address this later.


Now let us look at another command::

   atlas> whattype all_parameters_Cartan_gamma ?
   Overloaded instances of 'all_parameters_Cartan_gamma'
     (CartanClass,RealForm,ratvec)->[Param]

In other words, we hand in a Cartan Class, a real form and rational
vector and we obtain all the parameters with that infinitesimal
character coming from that Cartan subgroup. First we need a different syntax to
define our Cartan class. Note that above we picked a Cartan class
associated to a parameter ``p``. Here we want to take a particular
Cartan class, for example Cartan subgroup number 1 in the list of Cartan
classes for :math:`G`::

   atlas> G:=Sp(4,R)
   Value: connected split real group with Lie algebra 'sp(4,R)'
   atlas> whattype Cartan_class ?
   Overloaded instances of 'Cartan_class'
     (RealForm,int)->CartanClass
     (InnerClass,int)->CartanClass
     KGBElt->CartanClass
     (InnerClass,mat)->CartanClass
     Param->CartanClass

   atlas> H:=Cartan_class(G,1)
   Value: Cartan class #1, occurring for 2 real forms and for 1 dual real form
   atlas>

   atlas> print_Cartan_info (H)
   compact: 0, complex: 1, split: 0
   canonical twisted involution: 2,1,2
   twisted involution orbit size: 2; fiber size: 1; strong inv: 2
   imaginary root system: A1
   real root system: A1
   complex factor: empty
   atlas>


   atlas> set params=all_parameters_Cartan_gamma (H,G,rho(G))
   Variable params: [Param]
   atlas> #params
   Value: 2
   atlas> void: for p in params do prints(p) od
   final parameter (x=4,lambda=[2,1]/1,nu=[1,-1]/2)
   final parameter (x=9,lambda=[2,1]/1,nu=[3,3]/2)
   atlas>

Another example::

   atlas> H:=Cartan_class(G,2)
   Value: Cartan class #2, occurring for 1 real form and for 2 dual real forms
   atlas> params:=all_parameters_Cartan_gamma (H,G,rho(G))
   Value: [final parameter (x=5,lambda=[2,1]/1,nu=[0,1]/1),final parameter (x=5,lambda=[2,2]/1,nu=[0,1]/1),final parameter (x=6,lambda=[2,1]/1,nu=[0,1]/1),final parameter (x=6,lambda=[2,2]/1,nu=[0,1]/1),final parameter (x=7,lambda=[2,1]/1,nu=[2,0]/1),final parameter (x=7,lambda=[3,1]/1,nu=[2,0]/1),final parameter (x=8,lambda=[2,1]/1,nu=[2,0]/1),final parameter (x=8,lambda=[3,1]/1,nu=[2,0]/1)]
   atlas> void: for p in params do prints(p) od
   final parameter (x=5,lambda=[2,1]/1,nu=[0,1]/1)
   final parameter (x=5,lambda=[2,2]/1,nu=[0,1]/1)
   final parameter (x=6,lambda=[2,1]/1,nu=[0,1]/1)
   final parameter (x=6,lambda=[2,2]/1,nu=[0,1]/1)
   final parameter (x=7,lambda=[2,1]/1,nu=[2,0]/1)
   final parameter (x=7,lambda=[3,1]/1,nu=[2,0]/1)
   final parameter (x=8,lambda=[2,1]/1,nu=[2,0]/1)
   final parameter (x=8,lambda=[3,1]/1,nu=[2,0]/1)
   atlas>

So this is a list of representations which are similar and coming from
the same Cartan subgroup. So, we can study a representation by looking at similar ones and comparing them.

Another useful command helps you find all parameters with the same differential::

   atlas> p:= params[7]
   Value: final parameter (x=8,lambda=[3,1]/1,nu=[2,0]/1)
   atlas> p
   Value: final parameter (x=8,lambda=[3,1]/1,nu=[2,0]/1)
   atlas>
   atlas> set others=all_parameters (p)
   Variable others: [Param]
   atlas> void: for p in others do prints(p) od
   final parameter (x=8,lambda=[3,0]/1,nu=[2,0]/1)
   final parameter (x=8,lambda=[2,0]/1,nu=[2,0]/1)
   atlas>

This Cartan subgroup has two connected components. So if you hand in a parameter for this subgroup, the total number of parameters with the same differential is two and this commands gives the list of all of them