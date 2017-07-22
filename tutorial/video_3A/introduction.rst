Introduction on :math:`K` orbits on :math:`G/B`
================================================

In order to explain how ``atlas`` uses the ``KGB`` machinery we need
to discuss the theory a little bit. KGB is the heart of the theory on which the software is based and it takes some time to get used to understanding how it works. 

Previously we focused on the minimal principal series representations
of a Lie group, which are defined using a character on the maximally
split Cartan subgroup. In the coming sections we will talk about the
discrete series representations which are at the other end of the
spectrum of representations in the sense that they are based on a
compact Cartan subgroup of G and with some rather different
features. After that, we will talk about the more general
representations defined using characters of intermediate Cartan
subgroups and which are in a way a combination of the two first
constructions. So, understanding these separately will help us see the
general case.

Recall that a parameter is a triple :math:`p=(x,\lambda, \nu)`, where :math:`x \in K\backslash G / B` and which determines an involution :math:`\theta _x` of the Cartan subgroup.

.. math:: \lambda \in(X^* +\rho )/(1-{\theta }_x)X^*

.. math:: \nu \in {X}_{\mathbb Q} ^* /(1+{\theta }_x ) X_{\mathbb Q}^*\cong (X_{\mathbb Q} ^*)^{-\theta _x}


So we often see :math:`\nu` as being an element in the space on the right hand side. But we can also think of it as being in the quotient space.


So the infinitesimal character can be written as

.. math:: \gamma =\frac{1+\theta _x}{2}\lambda + \frac{1-\theta _x }{2}\nu

.. math:: =\frac{1+\theta _x}{2}\lambda +\nu

since :math:`\nu` is normally fixed by :math:`1-\theta_x`.

Recall that roughly the :math:`KGB` element ``x`` determines a
:math:`G(\mathbb R)`-conjugacy class of Cartan subgroups :math:`H` and
we denote by :math:`\theta _x` the Cartan involution of
:math:`H(\mathbb R)`

Previously we focused on the case when :math:`\theta _x` is acting by
:math:`-Id` This corresponded to the split Cartan subgroup :math:`H(\mathbb
R)={\mathbb R}^{*n}`

In that case the parameter :math:`\lambda \in (X^* + \rho )/2X^*`
gives a character of

.. math:: H(\mathbb R)^{\theta _x} ={(\mathbb Z)/2\mathbb Z}^n


So we get a character of the compact piece of the Cartan subgroup. 

Now :math:`\nu \in {X}_{\mathbb Q} ^*` and we had constructed the
induced representation

.. math:: Ind_B ^G (\chi \otimes \nu),  

where :math:`\chi=\rho -\lambda \in X^*`, since :math:`\lambda \in X^* + \rho`.

So, we have a well defined pairing between :math:`X^*` and :math:`X_*`:

.. math:: \chi(exp(2\pi i\mu ^{\vee}))=exp(2\pi i(<\rho -\lambda ,\mu^{\vee}>), 

with :math:`\mu^{\vee}\in \frac{1}{2}X_*`.


This pairing is the value of the character on the compact part of the
Cartan subgroup and it equals :math:`\pm 1`

:math:`KGB` elements
---------------------

In order to talk about all the representations of our group, we fix
once and for all a Cartan subgroup :math:`H` included in a Borel
subgroup :math:`B`. This avoids having to work with different Cartan
subgroups and roots and different choices of identifications. We will
be working with the same Cartan subgroup all the time.

The choice of Cartan subgroup does not matter. We can think of :math:`H` as
close to diagonal and :math:`B` upper triangular.

Now let us take a base point element :math:`x_b \in G`, so that
:math:`x_b ^2 \in Z(G)`. Attached to :math:`x_b` is the involution
:math:`\theta=int(x_b)`.

By Cartan's theory of real forms this gives a real form,
:math:`G(\mathbb R)`, of :math:`G`.  Denote by :math:`K=G^{\theta}`,
the complexified maximal compact subgroup of :math:`G(\mathbb R)`.

In other words the real form obtained by the involution is the one
whose complexified maximal compact subgroup is :math:`K`.

We are interested in the following space

.. math:: K\backslash G/B=\{K-\text{orbits on the flag variety G/B }\}
.. math:: =\{K \text{-conjugacy classes of Borel subgroups of G }\}.

:math:`G/B` is a complex projective variety and :math:`K` is an
algebraic group acting on it with finitely many orbits. And
:math:`G/B` is isomorphic to the space of Borel subgroups of :math:`G`
and the :math:`K`-orbits are the Borel subgroups up to conjugacy by
:math:`K`.

Parametrization Theorem
------------------------

.. math:: K\backslash G/B \leftrightarrow \{x\in Norm_G (H)|x{\backsim }_G x_b\}/H

This is a finite set. The map is given as follows:

If :math:`x=gx_b g^{-1}` then associate to x the element
:math:`[g^{-1}Bg]`, the :math:`K`-conjugacy class of the Borel
subgroup.

Now we check the map is well defined on :math:`K`-conjugcy classes of
Borel subgroups:

.. math:: x=(gk)x_b (gk)^{-1} \mapsto [k^{-1}(g^{-1}Bg)k]=[gBg]

On the right hand side the brackets mean :math:`K`-conjugacy
class. So, by conjugating by :math:`K` we get the same conjugacy class
of Borel subgroupns.

Parameter Set
--------------

Denote the above set by

.. math:: \mathcal X =\{x\in Norm_G (H) | x{\backsim }_G x_b\}/H

(Note: this set is really denoted :math:`\mathcal X [x_b]` in other
sources and :math:`\mathcal X` is the collection of all the sets for
all the base points; which give all strong real forms of
:math:`G`. The above set only has to do with one strong real form.

NOTE: FOR MORE INFORMATION ON STRONG REAL FORMS SEE: "Algorithms for
Representation Theory of Real Reductive Groups", by Adams and du
Cloux, in www.liegroups.org/papers/.

Since this set is finite, it makes sense to have an ``atlas`` command
``KGB`` that will give a finite list of the elements in :math:`\mathcal X`

.. math:: KGB \leftrightarrow \{x_0 , \dots ,x_{n-1} \}

