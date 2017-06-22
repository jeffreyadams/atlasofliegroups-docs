Introduction
=============

Recall that we had a parameter ``p`` determined by a triple ``p=(x,
lambda, nu)``, where 

.. math:: x\in K\backslash G/B \rightarrow \theta _x

so the Cartan involution is determined by ``x``

.. math:: \lambda \in(X^* +\rho )/(1-{\theta }_x)X^*

.. math:: \nu \in {X}_{\mathbb Q} ^* /(1+{\theta }_x ) X_{\mathbb Q}^*\cong (X_{\mathbb Q} ^*)^{-\theta _x}



So that each term in the expression of the infinitesimal character 

.. math:: \gamma =\frac{1+\theta _x}{2}\lambda + \frac{1-\theta _x }{2}\nu

.. math:: =\frac{1+\theta _x}{2}\lambda +\nu

is well defined.

Now we will talk a bit more about what the parameters mean. And there
is a notion of equivalence of parameters. For more details you can go
to

http://www.liegroups.org/papers/equivalenceOfParameters.pdf

The point is that the definition of equivalence is chosen so that we
have the following

.. Theorem:: 

   There are canonical bijections between
   
   1. Parameters for :math:`G`
   2. Standard modules for :math:`G`
   3. Irreducible representations of :math:`G`
   
   Moreover, the bijections are given as follows:
   
   .. math:: 1\rightarrow 2: p\rightarrow I(p)=Ind_P^G (\sigma ).
   
   The full induced from :math:`\sigma =` (limit of) discrete series
   This is called the standard module with parameter ``p``.
   
   .. math:: 2\rightarrow 3: Ind_P ^G (\sigma ) \rightarrow J
   
   where :math:`J` is the unique irreducible quotient of the standard
   module, which always exists in this setup. 
   
   Hence
   
   .. math:: 1\rightarrow 3: p\rightarrow J(p)
   
   the unique irreducible quotient of :math:`I(p)`


Composition series and character formulas
------------------------------------------

Now, if we have a standard module, which is a full induced
representation, it can be reducible and therefore it has a composition
series, which is given by Kazhdan-Lusztig theory (KL), as a formal
linear combination of irreducible modules. Conversely, given an
irreducible, we have, via KL, a character formula that gives the
irreducible as a formal linear combination of standard modules. The
coefficients of these combinations are the KL polynomials

This is what we will do the rest of the chapter.



