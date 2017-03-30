More on :math:`K\backslash G/B`
================================

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

Involutions and Conjugacy classes of Cartans
---------------------------------------------

Recall that we are fixing  :math:`x_b` and  :math:`\mathcal X =\mathcal X (\
x_b )`

This determines a fixed :math:`K` and :math:`\mathcal X` parametrizes:

.. math:: K\backslash G/B \leftrightarrow \mathcal X

And in the software, this gives a finite set of parameters:

.. math:: KGB= \mathcal X = \{x_0, \ldots x_{n-1} \}

Now the Weyl group :math:`W` acts naturally by conjugation
:math:`\mathcal X`. Then,

:math:\ \ \ \ \ \ `\mathcal X /W \leftrightarrow` conjugacy classes of Cartan
subgroups.  

This is how we associate a Cartan to an element :math:`x`. Namely, via this map from :math:`\mathcal X`.

Moreover

:math:`Stab_W (x) \simeq W(K,H) \simeq W(G(\mathbb R ), H(\mathbb
R))`,

This is the rational Weyl group of the real form of the group with
respect to the real Cartan, Which in the :math`\theta` world we think
of it as :math:`W(K,H)`.

Finally, there is a map :math:`\rho : \mathcal X \rightarrow {\mathcal
I}_W` (involutions in :math:`W`). The map is the obvious one:
:math:`x` is an element in the normalizer of :math:`H` so we take its
image in the Weyl group and that is an involution. Taking the
conjugacy cla\ sses of involutions in W gives a map:

:math:`\mathcal I /W \leftrightarrow \text{conjugacy classes of
Cartans in quasisplit group.}`

The map :math:`\rho` is not necessarily surjective. But it is
surjective if the group is quasisplit. So this :math:`\mathcal I` is
telling us about Cartans of the quasisplit form.

The Algorithms paper has a picture of the :math:`KGB` space for
:math:`Sp(4,R)`. There are 11 elements in the space. The picture gives
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
relations. 

There are four closed orbits at the bottom of the diagram which
correspond to the elements :math:`x_0 ,x_1 ,x_3` and :math:`x_4`,
which in turn get mapped to the identity involution. 

At the top of the diagram there is only one open orbit which is the
element :math:`x_{10}`, mapped to :math:`-Id`.  Below :math:`x_{10}`
we have the elements corresponding to :math:`x_7 ,x_8` and :math:`x_9`
and below them we have :math:`x_4 ,x_5` and :math:`x_6`.

The output of the software respects this partial order. More on this later.


