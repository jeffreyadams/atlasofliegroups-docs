:math:`K` orbits on :math:`G/B`
================================

In order to explain how ``atlas`` uses the ``KGB`` machinery we need
to discuss the theory a little bit.

Recall that a parameter is a triple :math:`p=(x,\lambda, \nu)`

where :math:`x \in K\backslash G/B` which determines an involution :math:`\theta _x` of the Cartan.

.. math:: \lambda \in(X^* +\rho )/(1-{\theta }_x)X^*

.. math:: \nu \in {X}_{\mathbb Q} ^* /(1+{\theta }_x ) X_{\mathbb Q}^*\cong (X_{\mathbb Q} ^*)^{-\theta _x}


So we often see :math:`\nu` as being an element in the space on the right hand side. But we can also think of it as being in the quotient space.


So the infinitesimal character can be written as

.. math:: \gamma =\frac{1+\theta _x}{2}\lambda + \frac{1-\theta _x }{2}\nu

.. math:: =\frac{1+\theta _x}{2}\lambda +\nu

since :math:`\nu` is normally fixed by :math:`\theta`.

Recall that roughly the :math:`KGB` element ``x`` determines a
:math:`G(\mathbb R)`-conjugacy class of Cartan subgroups :math:`H` and
we denote by :math:`\theta _x` the Cartan involution of
:math:`H(\mathbb R)`

Previously we focused on the case when :math:`\theta _x` is acting by
:math:`-Id` This corresponded to the split Cartan :math:`H(\mathbb
R)={\mathbb R}^{*n}`

In this case :math:`\lambda \in (X^* + \rho )/2X^*` gives a character
of 
.. math:: H(\mathbb R)^{\theta _x}=(\mathbb Z/2\mathbb Z)^n

So we get a character of the compact piece of the Cartan. 

Warning: we are assuming the :math:`\rho \in X^*` . Otherwise we need
to go to a covering.

Now :math:`\nu \in {X}_{\mathbb Q} ^*` and we had constructed the
induced representation

.. math:: Ind_B ^G (\chi \otimes \nu)`,  

where :math:`\chi=\rho -\lambda \in X^*`, since :math:`\lambda \in X^* + \rho`.

So, we have a well defined pairing between :math:`X^*` and :math:`X_*`:

.. math:: \chi(exp(2\pi i\mu ^{\vee}))=exp(2\pi i(<\rho -\lambda ,\mu^{\vee}>), 

with :math:`\mu^{\vee}\in \frac{1}{2}X_*`.


This pairing is the value of the character on the compact part of the
Cartan and it equals :math:`\pm 1`

:math:`KGB` elements
---------------------

We fix once and for all a Cartan subgroup :math:`H` included in a
Borel :math:`B`. This avoids having to work with different Cartans
and roots and different choices of identifications. We will be working
with the same Cartan all the time.

The choice of Cartan does not matter. We can think of :math:`H` as
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

Theorem

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
of Borels.

Definition.  Denote the above set by

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

Example: :math:`SL(2,\mathbb R)`.
----------------------------------

Let us start with the group :math:`G=SL(2,\mathbb C)`. For this group set :math:`x_b = diag(i,-i)`.

Then :math:`(x_b)^2 =-Id \in Z(G)`. The stabilizer in :math:`K` of this element is the diagonal torus 

.. math:: K^{\theta _x}=\left{\left(\begin{array}{cc}z & 0 \\ 0 & \frac{1}{z}\end{array}\right):z\in {\mathbb C}^{\times}\right}\cong SO(2,\mathbb C) 

So the real points of this group is the compact real form
:math:`K(\mathbb R)=SO(2)` and the real form of :math:`G` with this maximal compact subgroup is
:math:`G(\mathbb R)=SL(2,\mathbb R)`

In this setting it is better to think of :math:`G(\mathbb R)` as
:math:`SU(1,1)`

Then, the :math:`K` orbits on :math:`G/B` consist of three elements:

.. math:: x_b = \left( \begin{array}{cc}
i & 0 \\
0 & -i \end{array} \right) , \quad  -x_b=\left(\begin{array}{cc}
-i & 0 \\
0 & i \end{array} \right) , \quad u=\left(\begin{array}{cc}
0 & 1 \\
-1 & 0 \end{array} \right)

So, :math:`x_b` and :math:`-x_b` are all the elements of the cartan
that are conjugate to :math:`x_b`. And there is only one other
element, :math:`u`, up to conjugacy by :math:`H`, which is in the
normalizer of the Cartan and is conjugate to :math:`x_b`.

Note that :math:`x_b` and :math:`-x_b` are both fixed by conjugation
by :math:`H` and :math:`H` acts by conjugation on :math:`u`. Moreover,
we can replace :math:`u` by any element of the form

.. math:: \left(\begin{array}{cc}
0 & z \\
-\frac{1}{z} & 0 \end{array} \right)

So, :math:`K` acting on :math:`G/B` has three elements, representatives of the :math:`K` orbits on the conjugacy classes of Borel subgroups.

Observation: This is the usual action of :math:`Sl(2,\mathbb C)` on
the projective plane that gives three orbits, :math:`0`,
:math:`\infty` and :math:`{\mathbb C}^{\times }`.

Now as representatives of Borels we have:

.. math:: x_b \mapsto B=\left( \begin{array}{cc}
z & w \\
0 & \frac{1}{z} \end{array} \right), 

which is the Borel that was fixed at the begining. Now, taking an
element that conjugates $x_b$ to its negative we have:

.. math:: -x_b=s_{\alpha }(x_b) \mapsto B'=s_{\alpha }(B)=\left(
\begin{array}{cc} z & 0 \\ w & 1/z \end{array} \right)`;

and for :math:`u`, the element that conjugates :math:`x_b` to
:math:`u` is

.. math:: g=\frac{1}{\sqrt{2}} \left( \begin{array}{cc} 
1 & -1 \\ 
1 & 1 \end{array} \right). 

Then

.. math:: B''=gBg^{-1} =\left(\begin{array}{cc} cosh(z) & sinh(z) \\
sinh(z) & cosh(z) \end{array} \right) + \frac{1}{2}
\left(\begin{array}{cc} w & w \\ -w & w \end{array} \right)

One of the key points comes from just looking at the Cartan part of
the last :math:`B''`:

.. math:: H''=\left(\begin{array}{cc}
cosh(z) & sinh(z) \\
sinh(z) & cosh(z) \end{array} \right).

Since we fixed the Cartan involution :math:`{\theta }_{x_b} =
diag(i,-i)`, it is acting on this Cartan by :math:`-1` (i.e. by taking
the inverse). It acts trivially on the diagonal Cartan.

The set of real points of this Cartan is 

.. math:: H''(\mathbb R)=\{ \pm Id \left(\begin{array}{cc}
cosh(x) & sinh(x) \\
sinh(x) & cosh(x) \end{array} \right) | x\in \mathbb R \} \cong {\mathbb R}^{\times }

Which is the ususal way of writing split Cartan in :math:`SU(1,1)`.

The point is that, the pair :math:`(H'', {\theta }_{x_b} )` is
conjugate under :math:`G` to the pair :math:`(H, {\theta }_u )`. That
is, to :math:`H` and the conjugation action of this element :math:`u`.

In other words, the first pair is how we normally think of this Cartan
in the real group: we fix a real form (determined by the Cartan
involution :math:`{\theta }_{x_b}`) and vary the Cartans within this
real group. And in this case there are two Cartans, one compact and
one split.

The second pair is how ``atlas`` thinks of it. That is, it fixes the
original (diagonal) Cartan and varies the Cartan involution which acts
by :math:`-1` on the fixed diagonal Cartan.

Moral of the Story 
------------------- 

To summarize, we always fix: 

.. math:: H\subset B, x_b ,\theta = int(x_b ), \text{and}
K=G^{\theta };

we vary 

.. math:: x\in \mathcal X , \text{and} \  {\theta }_x ;

and we map 

.. math:: \{ (H',\theta ) \}/K \leftrightarrow \{ (H, {\theta
}_{x} ) | x\in \mathcal X \}.

So, rather than talking about the Cartan subgroups of :math:`G` with
their action of the fixed :math:`\theta` up to conjugacy by :math:`K`, we
conjugate everything back to the fixed :math:`H` and we vary the :math:`{\theta }_x`.

Similarly for the Borels we have:

.. math:: \{ (B',\theta ) \}/K \leftrightarrow \{ (B, {\theta }_{x} )
| x\in \mathcal X \}

Effect on :math:`(\mathfrak g , K_x)` modules.
-----------------------------------------------

Another important point is that now we will be talking about
:math:`(\mathfrak g , K_x )` modules as we vary :math:`x`. The
:math:`x`'s are all conjugate to :math:`x_b`, but not literally equal.
 
Therefore, the :math:`K_x`  are all conjugate to K but they are not
equal. So, we get all these :math:`(\mathfrak g , K_x )` modules that
are all equivalent to :math:`(\mathfrak g , {K_x}_b )` modules; and by
using this conjugation we can conjugate them all back to a
:math:`(\mathfrak g , {K_x}_b )` module.

More precisely, if :math:`\pi` (resp. :math:`\pi '`) are
:math:`(\mathfrak g , K_x )` (resp. :math:`(\mathfrak g , K_{x'} )`
modules, then :math:`\pi \cong {\pi }'` if there is :math:`g \in G`
with

.. math:: gxg^{-1} =x'`, \quad {\pi }^g \cong {\pi}

In this way, the software is varying :math:`x`, but in the end you can
conjugate back to :math:`x_b`.

More About :math:`KGB`
-----------------------

Recall that we are fixing  :math:`x_b` and  :math:`\mathcal X =\mathcal X (x_b )`

This gives a fixed :math:`K` and :math:`\mathcal X` parametrizes:

.. math:: K\backslash G/B \leftrightarrow \mathcal X

And in the software, this gives a finite set of parameters:

.. math:: KGB= \mathcal X = \{x_0, \ldots x_{n-1} \}

Now the Weyl group :math:`W` acts naturally by conjugation
:math:`\mathcal X `. Then,

:math:`\mathcal X /W \leftrightarrow` conjugacy classes of Cartan
subgroups.  This is how we associate a Cartan to an element
:math:`x`. Namely, via this map from :math:`\mathcal X`.

Moreover

:math:`Stab_W (x) \simeq W(K,H) \simeq W(G(\mathbb R ), H(\mathbb
R))`,

This is the rational Weyl group of the real form of the group with
respect to the real Cartan, Which in the $\theta$ world we think of it
as :math:`W(K,H)`.

Finally, there is a map :math:`\rho : \mathcal X \rightarrow {\mathcal
I}_W` (involutions in :math:`W`). The map is the obvious one:
:math:`x` is an element in the normalizer of :math:`H` so we take its
image in the Weyl group and that is an involution. Taking the conjugacy classes of involutions in W gives a map:

:math:`\mathcal I /W \leftrightarrow \text{conjugacy classes of
Cartans in quasisplit group.}`

The map :math:`\rho` is not necessarily surjective. But it is
surjective if the group is quasisplit. So this :math:`\mathcal I` is
telling us about Cartans of the quasisplit form.

The Algorithms paper has a picture of the :math:`KGB` space for
:math:`Sp(4,R)`. They are 11 elements in the space. The picture gives
the fibers of elements in :math:`KGB` that go to the same conjugacy
class of involutions and in turn to the same Cartan:

Four elements get mapped to the identity involution which corresponds
to the compact Cartan; two are mapped to the involutions from the
short root reflections :math:`s_{\alpha _1}` and :math:`s_{\alpha _2}`
corresponding to the intermediate Cartan isomorphic to :math:`{\mathbb
C}^{\times}`; four are mapped to the long root reflections
:math:`s_{\beta _1}`, :math:`s_{\beta _2}`, which correspond to the
Cartan :math:`S^1 \times {\mathbb R}^\times`; and one element is
mapped to :math:`-Id`, corresponding to the split Cartan.

In terms of representations, looking at each fiber of :math:`KGB`
elements corresponding to a given Cartan, will give us representations
attached to that Cartan. For example all the representations attached
to the split Cartan correspond to the last element :math:`x_10` which
is the fiber above the involution :math:`-1`, etc.

KGB ordering
-------------

There is a partial order on the :math:`KGB` elements coming from the
closure relations of the corresponding orbits. For example in the
Hasse diagram for KGB for Sp(4,R), the vertical lines indicate closure
relations. There are four closed orbits at the bottom of the diagram
which correspond to the elements :math:`x_0 ,x_1 ,x_3 ` and
:math:`x_4` , which in turn get mapped to the identity involution. At
the top of the diagram there is only one open orbit which is the
element :math:`x_{10}`, mapped to :math:`-Id`.  Below :math:`x_{10}` we have the elements corresponding to  :math:`x_7 ,x_8` and :math:`x_9` and below them we have :math:`x_4 ,x_5` and :math:`x_6`.

The output of the software respects this partial order. More on this later.


Discrete Series
----------------

Now let us fix :math:`x_b` and define the set


:math:`\mathcal F := {\rho }^{-1}(Id)=\{x\in \mathcal X |x\in H \}`

This is the distinguished fiber above the identity element in the Weyl group or the identity involution in :math:`{\mathcal I}_W`
this just means that the elements in this preimage are in the Cartan. Hence it corresponds to those elements in :math:`\mathcal X` which are actually in the Cartan :math:`H`.

So, this :math:`\mathcal F` parametrizes the Borel subgroups
containing a compact Cartan up to conjugation by :math:`K`



Now we can focus on the case when :math:`\theta _x` is acting by
:math:`Id` which corresponds to the discrete series representations.

So, let us assume that :math:`G=G(\mathbb C)` has discrete series repr\
esentations. This is equivalent to having a distinguished involution e\
qual to the Identity.