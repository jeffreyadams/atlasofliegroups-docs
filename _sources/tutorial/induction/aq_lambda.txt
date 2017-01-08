:math:`A_{\mathfrak q}(\lambda)` Construction
================================================

An alternate way to define an :math:`A_{\mathfrak q}(\lambda)` module is by
specifying a ``KGB`` element (attached to the fundamental Cartan), a weight
:math:`\lambda_q` to define the :math:`\theta`-stable Cartan, and the weight
:math:`\lambda` specifying the one-dimensional representation on :math:`L`.
For this construction, the weight :math:`\lambda` must satisfy that
:math:`\lambda-\rho(\mathfrak u)` is integral, and of course, it must be
orthogonal to the roots of :math:`L`.

Let's look at some examples in :math:`G=U(2,2)`. A convenient choice for ``x``
is ``KGB`` element 2, and we consider :math:`A_{\mathfrak q}(\lambda)` modules
attached to a :math:`\theta`-stable parabolic with Levi factor
:math:`U(2,1)\times U(0,1)`::

    atlas> G:=U(2,2)
    Value: connected quasisplit real group with Lie algebra 'su(2,2).u(1)'
    atlas> x:=KGB(G,2)
    Value: KGB element #2

    atlas> set lamq=[1,1,1,0]
    Variable lamq: [int]
    atlas> P:=parabolic(lamq,x)
    Parabolic is theta-stable.
    Value: ([0,1],KGB element #2)
    atlas> rho_u(P)
    Value: [  1,  1,  1, -3 ]/2


Since :math:`\rho(\mathfrak u)` is half-integral, we must choose
:math:`\lambda` to be half-integral as well::


   atlas> set M1=Aq(x,[1,1,1,-1]/2,lamq)
   Parabolic is theta-stable.
   Parabolic is theta-stable.
   Parabolic is theta-stable.
   Variable M1: Param
   atlas> M1
   Value: final parameter (x=15,lambda=[3,1,-1,-1]/2,nu=[1,0,-1,0]/1)

   atlas> goodness(x,[1,1,1,-1]/2,lamq)
   Parabolic is theta-stable.
   Parabolic is theta-stable.
   Parabolic is theta-stable.
   Weakly good


The function ``Aq(x,lam,lamq)`` computes
:math:`\mathcal R_{\mathfrak q}(\mathbb C_{\lambda})`, but with a different
normalization; there is a shift of :math:`\rho(\mathfrak u)` so that the
functor preserves infinitesimal characters: the resulting module shares the
infinitesimal character with the one-dimensional representation
:math:`\mathbb C_{\lambda}` of (possibly a double cover of) :math:`L`. One
advantage of this normalization is that it is easy to see whether
:math:`\lambda` is in the weakly fair range for :math:`\mathfrak u`: it
must be weakly dominant::


   atlas> goodness(x,[1,1,1,1]/2,lamq)
   Parabolic is theta-stable.
   Parabolic is theta-stable.
   Parabolic is theta-stable.
   Weakly fair

   atlas> goodness(x,[1,1,1,3]/2,lamq)
   Parabolic is theta-stable.
   Parabolic is theta-stable.
   Parabolic is theta-stable.
   None


Let's look at another example; this is discussed in Chapter 9 of Knapp-Vogan,
"Cohomological Induction and Unitary Representations".
Here :math:`G=SO(5,4)`, and :math:`P` is the unique :math:`\theta`-stable parabolic with Levi factor :math:`U(2,2)`::


     atlas> set G=SO(5,4)
     Variable G: RealForm
     atlas> set x=KGB(G,5)
     Variable x: KGBElt
     atlas> set lamq=[1,1,1,1]
     Variable lamq: [int]

     atlas> set P=parabolic(lamq,x)
     Parabolic is theta-stable.
     Variable P: ([int],KGBElt)
     atlas> P
     Value: ([0,1,2],KGB element #5)
     atlas> rho_u(P)
     Value: [ 2, 2, 2, 2 ]/1

     atlas> set L=Levi(P)
     Variable L: RealForm
     atlas> L
     Value: connected quasisplit real group with Lie algebra 'su(2,2).u(1)'

We can construct the good :math:`A_{\mathfrak q}(\lambda)` at infinitesimal
character :math:`\rho` using the two methods learned; let's do that, just to
check and confirm::


      atlas> theta_induce_irreducible(trivial(L),G)
      Value:
      1*final parameter (x=43,lambda=[7,5,3,1]/2,nu=[3,1,-1,-3]/2)

      atlas> Aq(x,[2,2,2,2],lamq)
      Parabolic is theta-stable.
      Parabolic is theta-stable.
      Parabolic is theta-stable.
      Value: final parameter (x=43,lambda=[7,5,3,1]/2,nu=[3,1,-1,-3]/2)

Notice that our :math:`\lambda=(2,2,2,2)` could also serve to define the
parabolic; in this case, we could have omitted the additional entry ``lamq``::

       atlas> Aq(x,[2,2,2,2])
       Parabolic is theta-stable.
       Parabolic is theta-stable.
       Parabolic is theta-stable.
       Value: final parameter (x=43,lambda=[7,5,3,1]/2,nu=[3,1,-1,-3]/2)

If we now move to the edge of the weakly fair range, Knapp/Vogan predict
that the module will be reducible. The command ``Aq(x,lam,lamq)`` returns
a parameter PROVIDED that the module is irreducible::

      atlas> Aq(x,[0,0,0,0],lamq)
      Parabolic is theta-stable.
      Parabolic is theta-stable.
      ....
      Parabolic is real.
      Parabolic is real.
      Runtime error:
      Aq is not irreducible. Use Aq_param_pol(x,lambda) instead
      (in call at basic.at:8:57-71 of error@string, built-in)
      ...(output truncated)

Here (as well as below) we have deleted many lines of output, such as messages
about parabolics in the middle
and parts of the error message at the end. Since the module is reducible, we
need to use the command ``Aq_param_pol`` instead::


     atlas> Aq_param_pol(x,[0,0,0,0],lamq)
     Parabolic is theta-stable.
     Parabolic is theta-stable.
     ...
     Parabolic is real.
     Parabolic is real.
     Value:
     1*final parameter (x=84,lambda=[7,7,1,1]/2,nu=[3,3,0,0]/2)
     1*final parameter (x=101,lambda=[7,7,3,3]/2,nu=[3,3,1,1]/2)

This weakly fair :math:`A_{\mathfrak q}(\lambda)` module is indeed reducible,
with two constituents.