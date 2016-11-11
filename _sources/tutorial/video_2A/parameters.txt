Parameters
===========

Introduction
------------

The basic object in ``atlas`` is a ``parameter`` and the ``parameter
space`` parametrizes both, the irreducible representations of a
reductive algebraic group as well as the standard modules. In other
words, for each ``p`` in the ``parameter space`` there are an
irreducible module $J(p)$ and a standard module $I(p)$ associated
to ``p``. Namely :math:`I(p)` is a representation induced from a limit of
discrete series and things are set up, following Langlands
classification, so that this standard module has a unique
irrudicible quotient $J(p)$. This quotient is also parametrized by the same
parameter ``p``.

So this parameter ``p`` is the basic object behind this classification theory.

In Adams' and DuCloux's paper, "Algorithms for representations of real
groups", Section 1, the authors use Langlands classification to describe the
algorithm that will associate, to each real group, the parameter space
in question.

More precisely, assume for the moment that ``rho`` exponentiates to a
character of a torus in $G(\\mathbb C )$. Then, the representations of
$G(\mathbb R)$, with a fixed (regular) infinitesimal
character``lambda`` are parametrized by $G(\mathbb R)$-orbits of
pairs $(H(\mathbb R ), \chi )$; where $H(\mathbb R )$ is a Cartan
subgroup of $G(\mathbb R )$ and $\chi$ is a character of $H(\mathbb R
)$ so that the differential of $\chi$ equals ``lambda`` up to
$G(\mathbb C )$-conjugacy.


Parameters for ``SL(2,R)``
--------------------------

Let's look at ``G=SL(2,R)`` and representations with infinitesimal
character ``rho`` How many are there? We need to look at conjugacy
classes of cartans and their characters.

Let's review a few things we know about ``SL(2,R)``::


      atlas> G:=SL(2,R)
      Value: connected split real group with Lie algebra 'sl(2,R)'

      atlas> root_datum (G)
      Value: simply connected root datum of Lie type 'A1'
      atlas> simple_roots(G)
      Value:
      | 2 |

      atlas> rho(G)
      Value: [ 1 ]/1

      atlas> nr_of_Cartan_classes (G)
      Value: 2

      atlas> void: for H in Cartan_classes (G) do prints(H) od
      Cartan class #0, occurring for 2 real forms and for 1 dual real form
      Cartan class #1, occurring for 1 real form and for 2 dual real forms
      atlas>

      atlas> set T= Cartan_classes (G)[0]
      Identifier T: CartanClass
      atlas> T
      Value: Cartan class #0, occurring for 2 real forms and for 1 dual real form
      atlas> set A= Cartan_classes (G)[1]
      Identifier A: CartanClass (hiding previous one of type mat)
      atlas> A
      Value: Cartan class #1, occurring for 1 real form and for 2 dual real forms
      atlas>


      atlas> occurrence_matrix (G)
      Value:
      | 1, 0 |
      | 1, 1 |

      atlas> void: for H in real_forms (G) do prints(H) od
      compact connected real group with Lie algebra 'su(2)'
      connected split real group with Lie algebra 'sl(2,R)'
      atlas>


So, the split form of type ``A1`` has two Cartans, the compact one,
$T=S^1$ and the split one, $A={\mathbb R}^x$.

Now, the characters for $T$ are of the form $e^{ik\theta}$ with $k \in \mathbb Z$``.
The ones corresponding to ``rho`` are ${e{^i\theta }, e^{-i\theta }}$ and they
are not conjugate under the Weyl group of $T$, since ``-1`` is not in this Weyl group.

On the other hand, for $A={\mathbb R}^x$, the characters whose differential is
equal to ``rho`` are ${x\rightarrow x, x^{-1},|x|, |x|^{-1} : x\in A}$, where
$|x|=sign(x)x$.

In this case ``-1`` is in the Weyl group of $A$. So, up to conjugacy, we
have that ${\chi \in \widehat A}= {x, |x|}$.

This says that we have exactly four representations of ``SL(2,R)``
with infinitesimal character ``rho``; two from each Cartan.

Let us look for those representations of ``SL(2,R)``. The command
``parameters_gamma (G,[1])`` looks for all the parameters of ``G``
with that infinitesimal character ``[1]``::

    atlas> set P=all_parameters_gamma (G,[1])
    Identifier P: [Param]
    atlas> #P
    Value: 4
    atlas>
    atlas> void: for p in P do prints(p) od
    final parameter (x=0,lambda=[1]/1,nu=[0]/1)
    final parameter (x=1,lambda=[1]/1,nu=[0]/1)
    final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    final parameter (x=2,lambda=[2]/1,nu=[1]/1)
    atlas>

This is the set of parameters for representations of ``SL(2,R)`` with
infinitesimal character ``rho``. Each parameter is a triple. ``(x,
lambda, nu)``. We will explain each of these later. But for now we can
say that the representation theory of ``SL(2,R)`` tells us that there
are four representations with infinitesimal character ``rho``. Two of
them are the discrete series associated to the compact Cartan and
correspond to the two parameters above with ``nu=0``; the other two
are the trivial representation and an irreducible principal series;
both, attached to the split Cartan and correspond to the parameters
with ``nu=1``.

We will say more about the representations of ``SL(2,R)`` later. But,
as it is illustrated here, the theory tells us we first need to
understand the characters of Tori. We do this in the next section.
