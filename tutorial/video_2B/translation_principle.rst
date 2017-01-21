Translation Principle
----------------------

Now let's change infinitesimal character usintg the translation
principle. Let us start again with the trivial representation::

   atlas> set p=trivial(G)
   Variable p: Param (overriding previous instance, which had type Param)
   atlas> p
   Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
   atlas> infinitesimal_character(p)
   Value: [ 1 ]/1
   atlas> is_finite_dimensional(p)
   Value: true
   atlas> dimension(p)
   Value: 1

We need to use the command ``T`` ::

   atlas> whattype T ?
   Overloaded instances of 'T'
     (Param,ratvec)->Param
     (ParamPol,ratvec)->ParamPol
   atlas>

   atlas> set q= T(p,[2])
   Variable q: Param (overriding previous instance, which had type Param)

   atlas> q
   Value: final parameter (x=2,lambda=[2]/1,nu=[2]/1)
   atlas> p
   Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
   atlas>


This means translate p from ``nu = 1`` to ``nu=2`` by applying the Zuckerman
translation principle. Note that you also changed ``lambda``. This is
a feature of the translation principle. What representation is this new
translated one? ::

   atlas> is_finite_dimensional(q)
   Value: true
   atlas> dimension(q)
   Value: 2
   atlas> infinitesimal_character(q)
   Value: [ 2 ]/1
   atlas>

So, this way we obtain the two dimensional representation with
infinitesimal character ``2``.

The translation principle is a great tool to move around by
changing infinitesimal characters without changing the nature of the
representation. For example, a reducible will stay reducible.

In contrast, it is interesting to see what happens when we change ``nu`` but
keep ``lambda``::

   atlas> set q=parameter(KGB(G,2), [1], [0])
   Variable q: Param (overriding previous instance, which had type Param)
   atlas> q
   Value: final parameter (x=2,lambda=[1]/1,nu=[0]/1)
   atlas> infinitesimal_character(q)
   Value: [ 0 ]/1
   atlas>

Comparing composition series of these two we have::

   atlas> p
   Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
   atlas> show(composition_series(I(p)))
   1*J(x=0,lambda=[1/1],nu=[0/1])
   1*J(x=1,lambda=[1/1],nu=[0/1])
   1*J(x=2,lambda=[1/1],nu=[1/1])
   atlas> q
   Value: final parameter (x=2,lambda=[1]/1,nu=[0]/1)
   atlas> show(composition_series(I(q)))
   1*J(x=2,lambda=[1/1],nu=[0/1])
   atlas>

So ``q`` is an irreducible spherical principal series at ``0``. In other words,
changing ``nu`` without changing ``lambda`` changes the reducibility
feature of the representation.

