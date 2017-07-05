Real Forms
===========

We can also find out what are all the real forms of a Lie group::

    atlas> set G=Sp(4,R)
    Identifier G: RealForm
    atlas> set rf=real_forms(G)
    Identifier rf: [RealForm]
    atlas>
    atlas> #rf
    Value: 3
    atlas> for H in rf do prints(H) od
    compact connected real group with Lie algebra 'sp(2)'
    connected real group with Lie algebra 'sp(1,1)'
    connected split real group with Lie algebra 'sp(4,R)'
    Value: [(),(),()]
    atlas>

Note the ``for loop`` that uses the command ``prints`` discussed
earlier in the section of basic ``atlas`` commands. It tells the software to go through the string of real forms of :math:`G` and print the list.

So, for :math:`G=Sp(4,\mathbb R)`, we have a list of three real forms:
the compact real form :math:`Sp(2)=Sp(2,0)`, an intermediate real form
:math:`Sp(1,1)` and the split real form :math:`Sp(4,\mathbb R)`. One corresponding to
each Lie algebra above.


Cartan Classes Accross Real Forms
----------------------------------

Now something interesting about real forms and Cartan classes is that
The Cartan classes are the same across all real forms of the same
complex group. In fact even though within the compact real form there
is only one conjugacy class of Cartan subgroups, we will have the same Cartan
classes for :math:`G=Sp(2)` than for :math:`G=Sp(4,\mathbb R)`::

    atlas> rf[0]
    Value: compact connected real group with Lie algebra 'sp(2)'
    atlas> nr_of_Cartan_classes (rf[0])
    Value: 4
    atlas>set Gc=rf[0]
    Identifier Gc: RealForm
    atlas> Gc
    Value: compact connected real group with Lie algebra 'sp(2)'
    atlas> Cartan_classes (Gc)[0]
    Value: Cartan class #0, occurring for 3 real forms and for 1 dual real form
    atlas> Cartan_classes (Gc)[1]
    Value: Cartan class #1, occurring for 2 real forms and for 1 dual real form
    atlas> Cartan_classes (Gc)[3]
    Value: Cartan class #3, occurring for 1 real form and for 3 dual real forms
    atlas>

Inner Classes and Outer Involutions
------------------------------------

Now let's look at the real forms of :math:`G=SL(5,\mathbb R)`. It
turns out there is only one, :math:`G` itself::

    atlas> set G=SL(5,R)
    Identifier G: RealForm (hiding previous one of type RealForm)
    atlas> set rf =real_forms(G)
    Identifier rf: [RealForm] (hiding previous one of type [RealForm])
    atlas>
    atlas> #rf
    Value: 1
    atlas> rf[0]
    Value: connected split real group with Lie algebra 'sl(5,R)'
    atlas>

Note that the Lie algebra, :math:`\mathfrak{sl}(5,\mathbb C)`, has
other real forms. However, associated to :math:`G`, there is only
one. This is because atlas thinks always in terms of inner
classes. That is, a real form is a real form in a given inner
class. And there is a distinquished involution in :math:`G` which is
non trivial and which atlas uses to determine the inner class of the
group :math:`G`. In this case there is only one real form in this
inner class::

    atlas> distinguished_involution(G)
    Value:
    | 1, 0, 0, 0 |
    | 1, 0, 0, -1 |
    | 1, 0, -1, 0 |
    | 1, -1, 0, 0 |
    atlas>

Let's look at another real form of type ``A4``, namely
:math:`SU(3,2)`. THis gives us another inner class. This inner class
has the rest of the real forms of :math:`\mathfrak{sl}(5,\mathbb C)`::

    atlas> H:=SU(3,2)
    Value: connected quasisplit real group with Lie algebra 'su(3,2)'
    atlas> set rfH=real_forms (H)
    Identifier rfH: [RealForm]
    atlas> #rfH
    Value: 3
    atlas> for a in rfH do prints(a) od
    compact connected real group with Lie algebra 'su(5)'
    connected real group with Lie algebra 'su(4,1)'
    connected quasisplit real group with Lie algebra 'su(3,2)'
    Value: [(),(),()]
    atlas>

So, these three real groups are grouped together because they are all
in the same inner class. Note that they all have a compact Cartan subgroup,
whereas :math:`SL(5,\mathbb R)` does not. Also, the same result is
achieved if we choose :math:`H` to be either of the other two groups
in the above list. The distinguished involution for :math:`H=SU(3,2)`
is the identity::

    atlas> distinguished_involution (H)
    Value:
    | 1, 0, 0, 0 |
    | 0, 1, 0, 0 |
    | 0, 0, 1, 0 |
    | 0, 0, 0, 1 |
    atlas>

Inner classes are associated with outer involutions; that is, with a
diagram automorphism. So, for :math:`SU(p,q)` the inner forms are
associated with the trivial automorphism of the Dynkin diagram of
``A{p+q-1}``; and for :math:`SL(p+q,\mathbb R)`, with the non trivial
diagram automorphism.

So what will happen for :math:`G=SL(6,\mathbb R)`? We can see in the
following example that there is another real form in the same inner
class as :math:`SL(6,\mathbb R)`, namely :math:`SL(3,\mathbb H)`. This
will be true whenever ``p+q=2n``::

    atlas> set G=SL(6,R)
    Identifier G: RealForm (hiding previous one of type RealForm)
    atlas> set rf=real_forms (G)
    Identifier rf: [RealForm] (hiding previous one of type [RealForm])
    atlas> #rf
    Value: 2
    atlas>
    atlas> for a in rf do prints(a) od
    connected real group with Lie algebra 'sl(3,H)'
    connected split real group with Lie algebra 'sl(6,R)'
    Value: [(),()]
    atlas>

More generally, for :math:`SL(2n,\mathbb R)` has another real form in
its inner class, the group SL(n,H).

In fact the distinguished involution is the one attached to the non trivial diagram automorphism. And in this case it flips all the roots except the central root::

    atlas> set delta=distinguished_involution (G)
    Identifier delta: mat
    atlas> delta
    Value:
    | 1, 0, 0, 0, 0 |
    | 1, 0, 0, 0, -1 |
    | 1, 0, 0, -1, 0 |
    | 1, 0, -1, 0, 0 |
    | 1, -1, 0, 0, 0 |
    atlas>
    atlas> simple_roots (G)
    Value:
    | 1, 0, 0, 0, 1 |
    | -1, 1, 0, 0, 1 |
    | 0, -1, 1, 0, 1 |
    | 0, 0, -1, 1, 1 |
    | 0, 0, 0, -1, 2 |
    atlas> delta*simple_roots (G)
    Value:
    | 1, 0, 0, 0, 1 |
    | 1, 0, 0, 1, -1 |
    | 1, 0, 1, -1, 0 |
    | 1, 1, -1, 0, 0 |
    | 2, -1, 0, 0, 0 |
    atlas>

In other words, ``delta`` is the outer automorphism that exchanges ``alpha[0]`` and ``alpha[4]``; ``alpha[1]`` and ``alpha[3]`` and fixes ``alpha[2]``.

This gives another way of thinking about coordinates. That is, trying
to understand the automorphism ``delta`` by looking at what it does to
the simple roots.


