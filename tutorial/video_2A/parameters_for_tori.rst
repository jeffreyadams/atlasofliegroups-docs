Parameters for Tori
====================

To study characters of Tori we first need to know how ``atlas``
understands what a torus is. In order to specify which torus we want
we use the command ``torus``. There are two ways of using this
command, which we can check as follows::

	atlas> whattype torus ?
	Overloaded instances of 'torus'
	  (int,int,int)->RealForm
	  CartanClass->RealForm
 	atlas>

We are interested in the first oprtion. So, we can determine a particular torus by assigning three integers::

	atlas> set H=torus(1,0,0)
	Identifier H: RealForm (hiding previous one of type string (constant))
	atlas> H
	Value: compact connected quasisplit real group with Lie algebra 'u(1)'
	atlas> set H=torus(0,1,0)
	Identifier H: RealForm (hiding previous one of type RealForm)
	atlas> H
	Value: connected quasisplit real group with Lie algebra 'gl(1,C)'
	atlas>  H:=torus(0,0,1)
	Value: disconnected split real group with Lie algebra 'gl(1,R)'
	atlas>

	atlas> H:=torus(1,2,3) 
	Value: disconnected quasisplit real group with Lie algebra
	'u(1).gl(1,C).gl(1,C).gl(1,R).gl(1,R).gl(1,R)' 
	atlas>

That is, the command ``torus(a,b,c)`` specifies a torus with ``a``
$S^1$ factors, ``b`` $C^x$ factors and ``c`` $R^x$ factors.

Starting with the circle, let us discuss its representations. From the
theory we know that they are parametrized by integers. So, starting
from the trivial representation we can see how the software
parametrizes them::

	 atlas>  H:=torus(1,0,0)
	 Value: compact connected quasisplit real group with Lie algebra 'u(1)'
	 atlas> set p=trivial(H)
	 Identifier p: Param
	 atlas> p
	 Value: final parameter (x=0,lambda=[0]/1,nu=[0]/1)
	 atlas>

This is the parameter for the trivial representation. The first element ``x`` is a KGB element. But it is not important for now. Let us see what involution it corresponds to::

   atlas> set x=x(p)
   Identifier x: KGBElt 
   atlas> set theta=involution(x)
   Identifier theta: mat
   atlas> theta
   Value: 
   | 1 |

   atlas> 

In this case it is the identity involution. That is, the torus has a
Cartan involution whose information is encoded in this element ``x``
and in the case of a compact torus it is the identity.

Now to understand the rest of the parameters, suppose that $H$ is a
complex torus with Cartan involution $\theta$, and defined over $\mathbb R$. Let
$H(R)$ be the corresponding real group. Denote by $X^* (H)$ the
characters of $H(R)$. Then these characters are parametrized by triples
$(\theta, \gamma, \lambda)$. Here ``gamma`` is the differential of the
character and $\lambda$ is the restriction of the character to
$H^{\theta}$.

The real points are not necessarily connected. So we need to specify
not only the differential but also information of the disconnected
part which is encoded in the estriction to $H^{\theta}$.

The basic fact is that the characters of $H^{\theta}$ are parametrized by
$X^*/(1-theta)X^*$.

So the characters of $H(R)$ are parametrized by triples $(\theta, \lambda, \nu)$
where $\lambda \in X^*/(1-theta)X^*``and $nu \in [X^*\otimes Q]^{-theta}$
 
So $\lambda$ is a character on $H^theta$ and $nu$ gives the
character on the Lie algebra of ``A=H^theta``.

In the case of the circle, ``lambda`` is in ``Z/(1-theta)Z=Z``, since
``theta=1`` and ``nu`` is in ``Q^{-1}=0``, So the parameter for these
character is ``(x=0,lambda, nu=0)`` and there is one for each lambda in
``Z`` correspondintg to the character ``e^{i lambda} t``. 

In the case of the trivial character the parameter is::

   atlas> p
   Value: final parameter (x=0,lambda=[0]/1,nu=[0]/1)
   atlas>

And for the character ``e^{i 3} t``::

   atlas> set q=parameter(x,[3],[0])
   Identifier q: Param (hiding previous one of type vec (constant))
   atlas> q
   Value: final parameter (x=0,lambda=[3]/1,nu=[0]/1)
   atlas>


