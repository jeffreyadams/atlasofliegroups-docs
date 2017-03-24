Example: :math:`SL(2,\mathbb R)`
==================================

Let us start with the group :math:`G=SL(2,\mathbb C)`. For this group
set :\ math:`x_b = diag(i,-i)`.

Then :math:`(x_b)^2 =-Id \in Z(G)`. The stabilizer in :math:`K` of
this element is the diagonal torus

:math:`\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ K^{\theta }_x=\left\{ \left( \begin{array}{cc} 
z & 0 \\ 
0 & \frac{1}{z} \end{array}\right) :z\in {\mathbb C}^{\times }\right\}\cong
SO(2,\mathbb C)`

So the real points of this group is the compact real form
:math:`K(\mathbb R)=SO(2)` and the real form of :math:`G` with this
maximal compact subgroup is :math:`G(\mathbb R)=SL(2,\mathbb R)`

In this setting it is better to think of :math:`G(\mathbb R)` as
:math:`SU(1,1)`

Then, the :math:`K` orbits on :math:`G/B` consist of three elements:

:math:`\ \ \ \ \ \ \ \ \ \ x_b =\left( \begin{array}{cc}
i&0\\ 
0&-i
\end{array}\right),\quad-x_b=\left(\begin{array}{cc}
-i&0\\ 
0&i
\end{array}\right) ,\quad u=\left( \begin{array}{cc} 
0 & 1 \\ 
-1 & 0 
\end{array} \right)`

So, :math:`x_b` and :math:`-x_b` are all the elements of the cartan
that are conjugate to :math:`x_b`. And there is only one other
element, :math:`u`, up to conjugacy by :math:`H`, which is in the
normalizer of the Cartan and is conjugate to :math:`x_b`.

Note that :math:`x_b` and :math:`-x_b` are both fixed by conjugation
by :math:`H` and :math:`H` acts by conjugation on :math:`u`. Moreover,
we can replace :math:`u` by any element of the form

:math:`\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \left(\begin{array}{cc}
0 & z \\
-\frac{1}{z} & 0 \end{array} \right)`

So, :math:`K` acting on :math:`G/B` has three elements,
representatives of the :math:`K` orbits on the conjugacy classes of
Borel subgroups.

Observation: This is the usual action of :math:`Sl(2,\mathbb C)` on
the projective plane that gives three orbits, :math:`0`,
:math:`\infty` and :math:`{\mathbb C}^{\times }`.

Now as representatives of Borels we have:

:math:`\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ x_b \mapsto B=\left( \begin{array}{cc}
z & w \\
0 & \frac{1}{z} \end{array} \right),`

which is the Borel that was fixed at the begining. Now, taking an
element that conjugates $x_b$ to its negative we have:

:math:`\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ -x_b=s_{\alpha }(x_b) \mapsto
B'=s_{\alpha }(B)=\left( \begin{array}{cc} z & 0 \\ w & 1/z
\end{array} \right)`;

and for :math:`u`, the element that conjugates :math:`x_b` to
:math:`u` is

:math:`\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ g=\frac{1}{\sqrt{2}} \left( \begin{array}{cc}
1 & -1 \\
1 & 1 \end{array} \right)`.

Then

:math:`\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ B''=gBg^{-1} =\left(\begin{array}{cc} cosh(z) & sinh(z) \\
sinh(z) & cosh(z) \end{array} \right) + \frac{1}{2}
\left(\begin{array}{cc} w & w \\ -w & w \end{array} \right)`.

One of the key points comes from just looking at the Cartan part of
the last :math:`B''`:

.. math:: H''=\left(\begin{array}{cc}cosh(z)&sinh(z)\\ sinh(z)&cosh(z)\end{array}\right).

Since we fixed the Cartan involution :math:`{\theta }_{x_b} =
diag(i,-i)`, it is acting on this Cartan by :math:`-1` (i.e. by taking
the inverse). It acts trivially on the diagonal Cartan.

The set of real points of this Cartan is

:math:`H''(\mathbb R)=\left\{ \pm Id \left(\begin{array}{cc}
cosh(x) & sinh(x) \\
sinh(x) & cosh(x) \end{array} \right) | x\in \mathbb R \right\} \cong {\mathbb R}^{\times }`

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

.. math:: H\subset B,\quad x_b ,\quad \theta = int(x_b ),\quad \text{and}\quad K=G^{\theta };

we vary

.. math:: x\in \mathcal X ,\quad \text{and} \quad  {\theta }_x ;

and we map

.. math:: \{ (H',\theta ) \}/K \leftrightarrow \{ (H, {\theta }_{x} ) | x\in \mathcal X \}.

So, rather than talking about the Cartan subgroups of :math:`G` with
their action of the fixed :math:`\theta` up to conjugacy by :math:`K`,
we conjugate everything back to the fixed :math:`H` and we vary the
:math:`{\theta }_x`.

Similarly for the Borels we have:

.. math:: \{ (B',\theta )\}/K\leftrightarrow \{ (B,{\theta _x})|x\in \mathcal X \}
