:math:`K` orbits on :math:`G/B`
================================

In order to explain how ``atlas`` uses the ``KGB`` machinery we need
to discuss the theory a little bit.

Recall that a parameter is a triple :math:`p=(x,\lambda, \nu)`

where :math:`x \in K\G/B` which determines an involution :math:`\theta _x` of the Cartan.

:math:`\lambda \in(X^* +\rho )/(1-{\theta }_x)X^*`

:math:`\nu \in {X}_{\mathbb Q} ^* /(1+{\theta }_x ) X_{\mathbb Q}^*
\cong (X_{\mathbb Q} ^*)^{-\theta _x}`


So we often see :math:`nu` as being an element in the space on the right hand side. But we can also think of it as being in the quotient space.


So the infinitesimal character can be written as

:math:`\gamma =\frac{1+\theta _x}{2}\lambda + \frac{1-\theta _x
}{2}\nu`

:math:`=\frac{1+\theta _x}{2}\lambda +\nu`

since :math:`\nu` is normally fixed by :math:`\theta`

Recall that roughly the :math:`KGB` element `x` determines a
:math:`G(\mathbb R)`-conjugacy class of Cartan subgroups :math:`H` and
we denote by :math:`\theta _x` the Cartan involution of
:math:`H(\mathbb R)`

Previously we focused on the case when :math:`\theta _x` is acting by
:math:`-Id` This corresponded to the split Cartan :math:`H(\mathbb
R)={\mathbb R}^{*n}`

In this case :math:`\lambda \in (X^* + \rho )/2X^*` gives a character of
:math:`H(\mathbb R)^{\theta _x}=(\mathbb Z/2\mathbb Z)^n`

So we get a character of the compact piece of the Cartan. 

Warning: we are assuming the :math:`\rho \in X^*`. Otherwise we need
to go to a covering.

Now :math:`\nu \in {X}_{\mathbb Q} ^*` and we had constructed the
induced representation

:math:`Ind_B ^G (\chi \otimes \nu)`,  where :math:`\chi=\rho -\lambda`
is in :math:`X^*`, since :math:`\lambda \in X^* + \rho`.

So 
:math:`\chi(exp(2\pi i\mu ^{\vee}))=exp(2\pi i(<\rho -\lambda ,
\mu^{\vee}>)`, 
with :math:`\mu^{\vee}\in \frac{1}{2}X_*`,
is a well defined pairing between :math:`X^*` and :math:`X_*`.

This pairing is the value of the character on the compact part of the
Cartan and it equals :math:`\pm 1`

Discrete Series
----------------

Now we can focus on the case when :math:`\theta _x` is acting by
:math:`Id` which corresponds to the discrete series representations.

So, let us assume that :math:`G=G(\mathbb C)` has discrete series representations. This is equivalent to having a distinguished involution equal to the Identity. 

We fix once and for all a Cartan subgroup :math:`H` included in a
Borel :math:`B`. This avoids having to work with different Cartans
and roots and different choices of identifications. We will be working
with the same Cartan all the time.

The choice of Cartan does not matter. We can think of :math:`H` as close to diagonal and :math:`B` upper triangular.

Now let us take a base point element :math:`x_b \in G`, so that :math:`x_b ^2 \in Z(G)`

Attached to :math:`x_b` is the involution 

:math:`\theta=int(x_b)`. 

By Cartan's theory of real forms this gives a real form of :math:`G`.
Denote by :math:`K=G^{\theta}`, the complexified maximal compact
subgroup of :math:`G(\mathbb R)`.

In other words the real form obtained by the involution is the one
whose complexified maximal compact subgroup is :math:`K`.

We are interested in the following space

:math:`K\G/B=\{K-\text{orbits on the flag variety } G/B\}`
:math:`=\{K \text{-conjugacy classes of Borel subgroups of } G\}`

:math:`G/B` is a complex projective variety and :math:`K` is an
algebraic group acting on it with finitely many orbits. And
:math:`G/B` is isomorphic to the space of Borel subgroups of :math:`G`
and the :math:`K`-orbits are the Borel subgroups up to conjugacy by
:math:`K`.

Theorem

:math:`K\G/B \leftrightarrow \{x\in Norm_G (H) | x{\backsim }_G
x_b\}/H`

This is a finite set. The map is given as follows:

If :math:`x=gx_b g^{-1}` then associate to x the element :math:`[g^{-1}Bg]`,
the :math:`K`-conjugacy class of the Borel subgroup.

Now we check the map is well defined:

If :math:`x=(gk)x_b (gk)^{-1} \rightarrow [k^{-1}(g^{-1}Bg)k]=[gBg]`