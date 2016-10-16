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

The characters of $S^1$
------------------------

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
$(\theta, \gamma, \lambda)$. Here $gamma$ is the differential of the
character and ``\lambda`` is the restriction of the character to
$H^{\theta}$.

The real points are not necessarily connected. So we need to specify
not only the differential but also information of the disconnected
part which is encoded in the estriction to $H^{\theta}$.

The basic fact is that the characters of $H^{\theta}$ are parametrized by
$X^*/(1-theta)X^*$.

So the characters of $H(R)$ are parametrized by triples $(\theta, \lambda, \nu)$
where ``lambda`` is in $X^*/(1-theta)X^*``and ``nu`` is in $[X^*\otimes \mathbb Q]^{-\theta}$
 
So``\lambda`` is a character on $H^\theta$ and ``nu`` gives the
character on the Lie algebra of the split Cartan $A=H^{-\theta}$.

In the case of the circle, ``lambda is in $\mathbb Z/(1-\theta)\mathbb
Z=\mathbb Z$, since $\theta=1$; and ``nu`` is in $Q^{-1}=0$ 

So the characters for the compact torus ar given by the parameters ``(x=0,lambda, nu=0)`` and there is
one for each lambda in $\mathbb Z$ correspondintg to the character $e^{i\lambda} t$.

In the case of the trivial character the parameter is::

   atlas> p
   Value: final parameter (x=0,lambda=[0]/1,nu=[0]/1)
   atlas>

And for the character $e^{i 3} t$ of $S^1$ we have::

    atlas> q:=parameter (x,[3],[0])
    Value: final parameter (x=0,lambda=[3]/1,nu=[0]/1)
    atlas> 

Note that ``nu`` is fixed by $-\theta$. So, given any ``nu`` it will be replaced by $1-\theta)/2\nu \in (X^*_{\mathbb Q})^{-\theta}$ ::

    atlas> q:=parameter (x,[3],[2])
    Value: final parameter (x=0,lambda=[3]/1,nu=[0]/1)
    atlas> 

So they are equivalent modulo the above equivalence relation and parametrize the same character. For example, we can ask ``atlas`` ::

   atlas> parameter (x,[3],[3])= parameter (x,[3],[0])
   Value: true
   atlas> 

The characters of $R^x$
------------------------

Now lets take the most split one-dimensional torus::

    atlas> H:=torus(0,0,1)
    Value: disconnected split real group with Lie algebra 'gl(1,R)'
    atlas> p:=trivial (H)
    Value: final parameter (x=0,lambda=[0]/1,nu=[0]/1)
    atlas> set x=x(p)
    Identifier x: KGBElt (hiding previous one of type KGBElt)
    atlas> theta:=involution(x)
    Value: 
    | -1 |

So now our parameters ``(x, lambda, nu)`` satisfy 
``lambda`` is in $\mathbb Z/(1-\theta)\mathbb Z=\mathbb Z/2\mathbb Z$, and 
``nu`` is fixed by $-theta=1$. So, ``nu`` is in $\mathbb Q$

Note that the characters of $R^x$ are parametrized by the complex
numbers ``nu``. However, the software only works with rational
parameters. So we have to do some extra work in general, depending on
the information that we want. The idea is that some problems can be
reduced to the case of rational parameters.

Le's do some examples. For the trivial representation we have::

     atlas> p
     Value: final parameter (x=0,lambda=[0]/1,nu=[0]/1)
     atlas>

And for the representation $\nu :x \rightarrow |x|^{4/3}$ ::

    atlas> p:=parameter (x,[0],[4/3])
    Value: final parameter (x=0,lambda=[0]/1,nu=[4]/3)
    atlas>

Now suppose we want a representation with non trivial character on the
component group $\mathbb Z/2\mathbb Z$. For example, the sign
representation is given by::

    atlas> q:=parameter (x,[1],[0])
    Value: final parameter (x=0,lambda=[1]/1,nu=[0]/1)
    atlas>

    atlas> p:=trivial(H)
    Value: final parameter (x=0,lambda=[0]/1,nu=[0]/1)
    atlas> q
    Value: final parameter (x=0,lambda=[1]/1,nu=[0]/1)
    atlas> p
    Value: final parameter (x=0,lambda=[0]/1,nu=[0]/1)
    atlas>

Which differs from the trivial by the non trivial character on
$\mathbb Z/2\mathbb Z$. And note what happens when we change that
character to ``2``::

      atlas> q:=parameter (x,[2],[0])
      Value: final parameter (x=0,lambda=[0]/1,nu=[0]/1)
      atlas> p=q
      Value: true
      atlas>

Which is correct since $2=0(mod2)$. So, sometimes the software will replace the parameters you are using, but they will be equivalent.

Characters of $C^x$
-------------------


