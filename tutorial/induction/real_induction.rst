Real Parabolic Induction
=========================

In order to calculate some induced representations using ``atlas``, we must
first define parabolic subgroups. The corresponding ``atlas`` data type is
``Parabolic``, or, equivalently, ``KGPElt``, and consists of a pair ``(S,x)``,
where ``S`` is a list of integers corresponding to the set of simple roots which
determine the conjugacy class of complex parabolics, and ``x`` is a ``KGB``
element. For some details, see the summary for the script file ``parabolics.at``
on the ``atlas Library`` page.

Let's do an example to see how this works.

Defining a Real Parabolic Subgroup
-----------------------------------

Suppose we want to define a real parabolic subgroup of :math:`G=Sp(4,\mathbb R)`
with Levi factor :math:`L\cong SL(2,\mathbb R)\times\mathbb R^{\times}`. This
Levi is attached to the long (simple) root in :math:`G` which in ``atlas`` is
numbered 1. In order to obtain a real parabolic subgroup, we choose ``x`` to
to be the ``KGB`` element associated to the maximally split Cartan, which
you may remember is the last element in ``KGB(G)``::


     atlas> set G=Sp(4,R)
     Variable G: RealForm

     atlas> #KGB(G)
     Value: 11
     atlas> set x=KGB(G,10)
     Variable x: KGBElt

     atlas> set P=Parabolic:([1],x)
     Variable P: ([int],KGBElt)
     atlas> P
     Value: ([1],KGB element #10)

To be sure that we have done this correctly, now check whether the parabolic
we have defined is indeed real, and that the Levi factor is the one we
wanted::


     atlas> is_parabolic_real(P)
     Value: true

     atlas> set L=Levi(P)
     Variable L: RealForm
     atlas> L
     Value: disconnected split real group with Lie algebra 'sl(2,R).gl(1,R)'

     atlas> simple_roots(L)
     Value:
     | 0 |
     | 2 |



An alternate way to define a (real) parabolic subgroup of a real group :math:`G`
is using a weight :math:`\lambda`. The simple roots orthogonal to the weight
determine the type of the (underlying complex) parabolic. For the resulting
parabolic subgroup to
be real, the weight :math:`\lambda` must satisfy
:math:`\theta_x(\lambda)=-\lambda`::



         atlas> set lambda=[1,0]
	 Variable lambda: [int]
	 atlas> set Q=parabolic(lambda,x)
	 Parabolic is real.
	 Variable Q: ([int],KGBElt)
	 atlas> Q
	 Value: ([1],KGB element #10)



Notice that if you define a parabolic subgroup using this command, ``atlas``
will tell you what kind of parabolic you have: real, theta-stable, or neither.
Let's check that we have defined the same parabolic as before::



         atlas> P=Q
	 Value: true


Real Induction
----------------

Real parabolic induction in ``atlas`` is normalized; the
infinitesimal character is preserved.

Now that we have a real parabolic subgroup of :math:`G`, let's compute an
induced representation.
First we need to choose and write down a representation,
i.e., a parameter, for the Levi subgroup :math:`L`. For example, let's take the
trivial representation::


          atlas> set t=trivial(L)
	  Variable t: Param
	  atlas> t
	  Value: final parameter (x=2,lambda=[0,1]/1,nu=[0,1]/1)

Keep in mind how :math:`L` is embedded in :math:`G`; the first coordinate
of lambda and nu corresponds to the :math:`\mathbb R^{\times}` factor, the
second is the parameter for :math:`SL(2,\mathbb R)`. You can see ``KGB`` for
:math:`L`::

        atlas> print_KGB(L)
	kgbsize: 3
	Base grading: [1].
	0:  0  [n]   1    2  (0,0)#0 e
	1:  0  [n]   0    2  (0,1)#0 e
	2:  1  [r]   2    *  (0,0)#1 1^e


There are two ways in ``atlas`` to induce a representation on :math:`L` to
:math:`G`. The command ``real_induce_standard`` takes the parameter for
:math:`L` to represent a standard module, and writes the answer as a standard
module for :math:`G`::


       atlas> real_induce_standard(t,G)
       Value: final parameter (x=10,lambda=[2,1]/1,nu=[0,1]/1)


If you start with a single parameter, the output will be a single parameter
as well. You can also apply this function to a ``ParamPol``. Probably of more
interest will be the command ``real_induce_irreducible`` which takes the
parameter of :math:`L` to represent an irreducible representation, and returns
the composition series of the induced representation of :math:`G`::



      atlas> real_induce_irreducible(t,G)
      Value:
      1*final parameter (x=4,lambda=[1,0]/1,nu=[1,-1]/2)
      1*final parameter (x=10,lambda=[2,1]/1,nu=[1,0]/1)

You see that this induced representation is reducible, with two pieces.

Let's look at a second example: this time, let's take the real parabolic with
Levi factor :math:`GL(2,\mathbb R)` and compute the representation of :math:`G`
obtained by inducing the trivial on this Levi::


       atlas> Q:=([0],x)
       Value: ([0],KGB element #10)
       atlas> L:=Levi(Q)
       Value: disconnected split real group with Lie algebra 'sl(2,R).gl(1,R)'


Although the description of :math:`L` is the same as in our first example, it
is a different group::

       atlas> simple_roots(L)
       Value:
       |  1 |
       | -1 |

       atlas> print_KGB(L)
       kgbsize: 2
       Base grading: [1].
       0:  0  [n]   0    1  (0,0)#0 e
       1:  1  [r]   1    *  (0,0)#1 1^e


These are indeed the data for :math:`GL(2,\mathbb R)`. Now let's induce::


       atlas> t:=trivial(L)
       Value: final parameter (x=1,lambda=[1,-1]/2,nu=[1,-1]/2)
       atlas> real_induce_irreducible(t,G)
       Value:
       1*final parameter (x=10,lambda=[2,1]/1,nu=[1,1]/2)


So this time, the induced representation is irreducible.

