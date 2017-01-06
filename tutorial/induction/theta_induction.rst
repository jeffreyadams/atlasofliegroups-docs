Cohomological Parabolic Induction
====================================

Defining :math:`\theta`-stable parabolic subalgebras for a given real group
:math:`G` is a little trickier than defining real parabolic subgroups
because there can be more that one :math:`K` conjugacy class of such
structures attached to a given (type of) complex parabolic subgroup.

Defining a :math:`\theta`-Stable Parabolic Subalgebra
---------------------------------------------------------------

In the section on Real Parabolic Induction we discussed two different ways of
defining a real parabolic subgroup: by giving the complex parabolic subgroup
type (i.e., a subset of the simple roots), and by giving a weight
:math:`\lambda`. Let's focus here on the second technique, which may seem
more natural and familiar. Since a :math:`\theta`-stable parabolic subalgebra
may be thought of as
:math:`\mathfrak q(\lambda)=\mathfrak l(\lambda)+\mathfrak u(\lambda)` for
a weight :math:`\lambda` in the compact part of the fundamental Cartan
subalgebra, the first step is to choose a ``KGB`` element ``x`` attached to
the fundamental Cartan. It also needs to be in the distinguished fiber (which
is automatic in the equal rank case). In order to obtain a
:math:`\theta`-stable parabolic subalgebra, you need to choose a weight
:math:`\lambda` that is fixed by the involution :math:`\theta_x`. In the
equal rank case, this is, of course, also automatic for this choice of ``x``.

Let's look at an example: Let :math:`G=Sp(4,\mathbb R)` once again, and let's
choose ``x`` to be ``KGB`` element 2. This is the element attached to the
holomorphic (or antiholomorphic) discrete series of :math:`G`, so that the
simple root #0, :math:`e_1-e_2`, is compact.
Then the unique :math:`\theta`-stable parabolic subalgebra with Levi factor
:math:`U(1,1)` is the one attached to, for example, the weight
:math:`\lambda=(1,-1)`::


  atlas> set G=Sp(4,R)
  Variable G: RealForm
  atlas> set x=KGB(G,2)
  Variable x: KGBElt

  atlas> set P=parabolic([1,-1],x)
  Parabolic is theta-stable.
  Variable P: ([int],KGBElt)

  atlas> P
  Value: ([0],KGB element #0)

  atlas> set L=Levi(P)
  Variable L: RealForm
  atlas> L
  Value: connected quasisplit real group with Lie algebra 'sl(2,R).u(1)'


Notice that ``atlas`` prints a message that the parabolic is indeed
:math:`\theta`-stable. Notice also that ``atlas`` conjugates the weight
:math:`\lambda` and ``x`` simultaneously to make the weight dominant before
calculating ``P``; we could have defined this parabolic using the dominant
weight :math:`(1,1)` and the ``KGB`` element #0::

  atlas> set Q=parabolic([1,1],KGB(G,0))
  Parabolic is theta-stable.
  Variable Q: ([int],KGBElt)
  atlas> P=Q
  Value: true

If we use the weight :math:`(1,1)` with our original ``x`` to construct a
parabolic, we get one with compact Levi factor::

  atlas> set P2=parabolic([1,1],x)
  Parabolic is theta-stable.
  Variable P2: ([int],KGBElt)
  atlas> P2
  Value: ([0],KGB element #2)
  atlas> Levi(P2)
  Value: compact connected real group with Lie algebra 'su(2).u(1)'

and :math:`\lambda=(-1,-1)` would give the opposite parabolic.

You can get a list of all :math:`\theta`-stable parabolics for :math:`G`
using the command ``theta_stable_parabolics``::

  atlas> set tsp=theta_stable_parabolics(G)
  Variable tsp: [([int],KGBElt)]

  atlas> void: for P@i in tsp do prints(i," ",P) od
  0 ([],KGB element #0)
  1 ([],KGB element #1)
  2 ([],KGB element #2)
  3 ([],KGB element #3)
  4 ([0],KGB element #2)
  5 ([0],KGB element #3)
  6 ([0],KGB element #4)
  7 ([1],KGB element #5)
  8 ([1],KGB element #6)
  9 ([0,1],KGB element #10)

Notice that there are four :math:`\theta`-stable parabolics corresponding to
the empty set of simple roots, i.e., to the Borel, one for each discrete series.
You can also get a list of the parabolics of a certain type only::

  atlas> set tsp_0=theta_stable_parabolics_type(G,[0])
  Variable tsp_0: [([int],KGBElt)]

  atlas> void: for P@i in tsp_0 do prints(i," ",P) od
  0 ([0],KGB element #2)
  1 ([0],KGB element #3)
  2 ([0],KGB element #4)

In this list, the ``KGB`` element given is the maximal element in the
equivalence class on ``KGB(G)`` defined by the set of simple roots ``[0]``;
our parabolic ``P`` defined earlier is #2 in this list::

  atlas> P=tsp_0[2]
  Value: true
  atlas> equivalence_class_of(P)
  Value: [KGB element #0,KGB element #1,KGB element #4]

The equivalence class of ``P`` is the set of ``KGB`` elements obtained from
``x`` by cross actions and Cayley transforms through simple root #0 (in general,
through any of the simple roots listed). Each of
these ``KGB`` elements will define the same parabolic. (See the summary for the
script file ``parabolics.at`` on the ``atlas Library`` page for more details.)


Theta-Stable Induction
--------------------------

The commands for theta-stable, or cohomological parabolic, induction work in
a similar fashion to the corresponding commands in the real parabolic case. We
can theta-induce standard modules (``theta_induce_standard``) or irreducibles,
and the answers need to be understood in those terms. Let's focus here on the
second
type of induction: inducing an irreducible representation of :math:`L` to get
the composition series of the resulting representation of :math:`G`.

Let's stay with :math:`G=Sp(4,\mathbb R)`, and :math:`P` the
:math:`\theta`-stable parabolic with Levi factor :math:`L=U(1,1)`. First take
the trivial representation of :math:`L`::

  atlas> t:=trivial(L)
  Value: final parameter (x=2,lambda=[1,-1]/2,nu=[1,-1]/2)
  atlas> set p=theta_induce_irreducible(t,G)
  Variable p: ParamPol
  atlas> p
  Value:
  1*final parameter (x=4,lambda=[2,1]/1,nu=[1,-1]/2)Variable p: ParamPol

  atlas> goodness(t,G)
  Good

This is of course an :math:`A_{\mathfrak q}(\lambda)` module in the good range,
and therefore, as expected, irreducible. Theta-induction takes representations
of infinitesimal character :math:`\gamma` to representations of infinitesimal
character :math:`\gamma+\rho(\mathfrak u)`::

  atlas> infinitesimal_character (t)
  Value: [  1, -1 ]/2
  atlas> infinitesimal_character (p)
  Value: [ 2, 1 ]/1
  atlas> rho_u(P)
  Value: [ 3, 3 ]/2


The output is of type ``ParamPol``. Next, let's induce the one-dimensional
:math:`det^{-1}` of :math:`L`::

  atlas> set p1=parameter(L,2,[-1,-3]/2,[-1,-3]/2)
  Variable p1: Param
  atlas> goodness(p1,G)
  Weakly good
  atlas> theta_induce_irreducible(p1,G)
  Value:
  1*final parameter (x=4,lambda=[1,0]/1,nu=[1,-1]/2)

Of course, we can choose any irreducible representation on :math:`L` at all. For
a non-unitary example, here is a finite dimensional representation::


  atlas> set p=parameter(L,2,[1,-5]/2,[1,-5]/2)
  Variable p: Param (overriding previous instance, which had type Param)
  atlas> dimension(p)
  Value: 3
  atlas> goodness (p,G)
  None

  atlas> theta_induce_irreducible(p,G)
  Parabolic is theta-stable.
  Parabolic is theta-stable.
  Value:
  1*final parameter (x=4,lambda=[2,1]/1,nu=[1,-1]/2)
  1*final parameter (x=9,lambda=[2,1]/1,nu=[3,3]/2)


This parameter is outside the fair range, and the induced representation is
reducible. The calculation involves wall crossings and coherent continuation
action. The messages "Parabolic is theta-stable." are
created because during this calculation certain new parabolics are defined.
(See the summary for the
script file ``induction.at`` on the ``atlas  Library`` page for more details.)

Notice that the induction functions will accept only parameters on Levi factors
of the right kind of parabolics; entering a parameter on a Levi subgroup that
does not come from a real parabolic subgroup will result in an error message::


       atlas> real_induce_irreducible(t,G)
       Runtime error:
       L is not Levi of real parabolic
       (in call at basic.at:8:57-71 of error@string, built-in)
       [b=false, message="L is not Levi of real parabolic"]
       ...(output truncated)


Similarly, the function ``theta_induce_irreducible`` requires the input of
a parameter on a Levi subgroup coming from a :math:`\theta`-stable parabolic
subalgebra. Indeed, a Levi subgroup of :math:`G` uniquely defines the parabolic
it came from. The command ``make_parabolic(L,G)`` reverses the function
``Levi(P)``.


