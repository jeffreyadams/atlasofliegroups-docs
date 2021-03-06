Example: :math:`SL(2,\mathbb R)`
==================================

Let us start with the group :math:`G=SL(2,\mathbb C)`. For this group
set :math:`x_b = \operatorname{diag}(i,-i)`.

Then :math:`(x_b)^2 =-\operatorname{Id} \in Z(G)`. The stabilizer in :math:`K` of
this element is the diagonal torus

.. math:: K^{{\theta }_x}=\left\{ \begin{pmatrix} z & 0 \\ 0 & z^{-1}
	  \end{pmatrix} :z\in {\mathbb C}^{\times }\right\}
	  \cong SO(2,\mathbb C)

So the real points of this group is the compact real form
:math:`K(\mathbb R)=SO(2)` and the real form of :math:`G` with this
maximal compact subgroup is :math:`G(\mathbb R)=SL(2,\mathbb R)`

In this setting it is better to think of :math:`G(\mathbb R)` as
:math:`SU(1,1)`

Then, the :math:`K` orbits on :math:`G/B` consist of three elements:

.. math:: x_b =\left( \begin{pmatrix} i&0\\ 0&-i \end{pmatrix}\right),\quad-x_b=\left(\begin{pmatrix} -i&0\\ 0&i \end{pmatrix}\right) ,\quad u=\left( \begin{pmatrix} 0 & 1 \\ -1 & 0 \end{pmatrix} \right)


So, :math:`x_b` and :math:`-x_b` are all the elements of the Cartan subgroup
that are conjugate to :math:`x_b`. And there is only one other
element, :math:`u`, up to conjugacy by :math:`H`, which is in the
normalizer of the Cartan subgroup and is conjugate to :math:`x_b`.

Note that :math:`x_b` and :math:`-x_b` are both fixed by conjugation
by :math:`H` and :math:`H` acts by conjugation on :math:`u`. Moreover,
we can replace :math:`u` by any element of the form

.. math:: \left(\begin{pmatrix} 0 & z \\ -z^{-1} & 0 \end{pmatrix} \right)

So, :math:`K` acting on :math:`G/B` has three elements,
representatives of the :math:`K` orbits on the conjugacy classes of
Borel subgroups.

Observation: This is the usual action of :math:`Sl(2,\mathbb C)` on
the projective plane that gives three orbits, :math:`0`,
:math:`\infty` and :math:`{\mathbb C}^{\times }`.

To obtain these elements with the software there is a command
``print_KGB (G)``::

   atlas> whattype print_KGB ?
   Overloaded instances of 'print_KGB'
     RealForm->void
     KGBElt->void
   atlas>

   atlas> set G=SL(2,R)
   Variable G: RealForm
   atlas> G
   Value: connected split real group with Lie algebra 'sl(2,R)'
   atlas>
   atlas> print_KGB (G)
   kgbsize: 3
   Base grading: [1].
   0:  0  [n]   1    2  (0)#0 e
   1:  0  [n]   0    2  (1)#0 e
   2:  1  [r]   2    *  (0)#1 1^e
   atlas>

So :math:`KGB` has three elements labeled ``0, 1, 2`` and the second
to last column give the number of the Cartan subgroup. So the first two
elements correspond to the compact Cartan subgroup and the last one to the
split Cartan subgroup.

Now let us look at the block of the trivial representation of :math:`G`::

   atlas> set B=block_of (trivial (G))
   Variable B: [Param]
   atlas> void: for p in B do prints(p) od
   final parameter (x=0,lambda=[1]/1,nu=[0]/1)
   final parameter (x=1,lambda=[1]/1,nu=[0]/1)
   final parameter (x=2,lambda=[1]/1,nu=[1]/1)
   atlas>

Another way to do this is to define a new function, say ``show`` as
follows:: 

   atlas> set show([Param] params)= void: for p in params do prints(p) od 
   Added definition [6] of show: ([Param]->) 
   atlas> show(B)
   final parameter (x=0,lambda=[1]/1,nu=[0]/1) 
   final parameter (x=1,lambda=[1]/1,nu=[0]/1) 
   final parameter (x=2,lambda=[1]/1,nu=[1]/1)
   atlas>

Then you can use the same function ``show`` for different parameter sets.

So, the first two elements parametrize the discrete series with Harish Chandra parameters :math:`\rho` and :math:`-\rho`. More on this later.


Now as representatives of Borel subgroups we have:

.. math:: x_b \mapsto B=\left\{ \left( \begin{pmatrix} z & w \\ 0 & z^{-1} \end{pmatrix} \right)  |z\in {\mathbb C}^{\times },w\in \mathbb C \right\}

which is the Borel subgroup that was fixed at the begining. Now, taking an
element that conjugates $x_b$ to its negative we have:

.. math:: -x_b=s_{\alpha }(x_b) \mapsto B'=s_{\alpha }(B)=\left\{ \left( \begin{pmatrix} z & 0 \\ w & z^{-1} \end{pmatrix} \right) |z\in {\mathbb C}^{\times },w\in \mathbb C \right\};

and for :math:`u`, the element that conjugates :math:`x_b` to
:math:`u` is

.. math:: g=\frac{1}{\sqrt{2}} \left( \begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix} \right).

Then

.. math:: B''=gBg^{-1} =\left\{ \left(\begin{pmatrix} \cosh(z) &
	  \sinh(z) \\ \sinh(z) & \cosh(z) \end{pmatrix} \right) + \frac{1}{2}
	  \left(\begin{pmatrix} w & w \\ -w & w \end{pmatrix} \right)
	  |z\in {\mathbb C}^{\times },w\in \mathbb C \right\}.

One of the key points comes from just looking at the Cartan subgroup part of
the last :math:`B''`:

.. math:: H''=\left\{ \left(\begin{pmatrix}\cosh(z)&\sinh(z)\\
	  \sinh(z)&\cosh(z)\end{pmatrix}\right) |z\in {\mathbb C}^{\times}
	  \right\}.

Since we fixed the Cartan involution :math:`{\theta }_{x_b} =
\operatorname{diag}(i,-i)`, it is acting on this Cartan subgroup by :math:`-1` (i.e. by taking
the inverse). It acts trivially on the diagonal Cartan subgroup.

The set of real points of this Cartan subgroup is

.. math:: H''(\mathbb R)=\left\{ \pm \operatorname{Id} \left(\begin{pmatrix} \cosh(x)  & \sinh(x) \\ \sinh(x) & \cosh(x) \end{pmatrix} \right) | x\in \mathbb R \right\} \cong {\mathbb R}^{\times },

which is the usual way of writing split Cartan subgroup in :math:`SU(1,1)`.

The point is that the pair :math:`(H'', {\theta }_{x_b} )` is
conjugate under :math:`G` to the pair :math:`(H, {\theta }_u )`. That
is, to :math:`H` and the conjugation action of this element :math:`u`.

In other words, the first pair is how we normally think of this Cartan subgroup
in the real group: we fix a real form (determined by the Cartan subgroup
involution :math:`{\theta }_{x_b}`) and vary the Cartan subgroups within this
real group. And in this case there are two Cartan subgroups, one compact and
one split.

The second pair is how ``atlas`` thinks of it. That is, it fixes the
original (diagonal) Cartan subgroup and varies the Cartan involution which acts
by :math:`-1` on the fixed diagonal Cartan subgroup.

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

Similarly for the Borel subgroups we have:

.. math:: \{ (B',\theta )\}/K\leftrightarrow \{ (B,{\theta _x})|x\in \mathcal X \}
