Real Forms of a Complex Group
==============================


We can also find out what are all the real forms of a Lie group. By this we mean the real forms of the complex Lie group of a given Lie type::

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

So for ``G=Sp(4,R)``, there are three real Lie algebras which are real forms of ``sp(2,C)``, which is the complexified Lie algebra of type ``C2``: the compact Lie algebra ``sp(2)``; a real Lie algebra ``sp(1,1)`` and a split real Lie algebra ``sp(4,R)``. For each one of these Lie algebras there is a real Lie group which is a real form of ``Sp(4,C)``, the complex Lie group of type ``C2``.

Now something interesting about real forms and Cartan classes is that The Cartan classes are the same across all real forms of the same complex group. In fact even though within the compact Cartan there is only one conjugacy class of Cartans (within the compact group). We will have the same Cartan classes for G=Sp(2) than for G=Sp(4,R)::


    atlas> rf[0]
    Value: compact connected real group with Lie algebra 'sp(2)'
    atlas> nr_of_Cartan_classes (rf[0])
    Value: 4
    atlas>
    set G0=rf[0]
    Identifier G0: RealForm
    atlas> G0
    Value: compact connected real group with Lie algebra 'sp(2)'
    atlas> Cartan_classes (G0)[0]
    Value: Cartan class #0, occurring for 3 real forms and for 1 dual real form
    atlas> Cartan_classes (G0)[1]
    Value: Cartan class #1, occurring for 2 real forms and for 1 dual real form
    atlas> Cartan_classes (G0)[3]
    Value: Cartan class #3, occurring for 1 real form and for 3 dual real forms
    atlas>

Now let's look at the real forms of G=SL(5,R). It turns out there is only one: G itself::

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

Note that the complexified Lie algebra of ``G``, ``g_{C}=sl(5,C)``. Has other real forms. However, associated to ``G``, there is only one. This is because atlas thinks always in terms of inner classes. That is a real form is a real form in a given inner class. And there is a distinquished involution in ``G`` which is non trivial and which atlas uses to determine the inner class of the group ``G``, and there is only one real form in this inner class.::

    atlas> distinguished_involution(G)
    Value:
    | 1, 0, 0, 0 |
    | 1, 0, 0, -1 |
    | 1, 0, -1, 0 |
    | 1, -1, 0, 0 |
    atlas>

Let's look at another real form of ``g_{C}``, namely ``su(3,2)``. THis gives us another inner class. it turns out this inner class has the rest of the real forms of ``g_{C}``::

    atlas> H
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

So, these three real groups are grouped together because they are all in the same inner class. Note that they all have a compact Cartan, whereas ``SL(5,R)`` does not. The distinguished involution or ``H=SU(3,2)`` is the identity::

    atlas> distinguished_involution (H)
    Value:
    | 1, 0, 0, 0 |
    | 0, 1, 0, 0 |
    | 0, 0, 1, 0 |
    | 0, 0, 0, 1 |
    atlas>

Inner classes are associated with outer involutions. That is a diagram automorphism. So, for ``G=SU(p,q)`` the inner forms are associated with the trivial automorphism of the Dynkin diagram of ``A_{p+q-1}``; and for ``G=SL(p+q,R)``, with the non trivial diagram automorphism.

So what will happen for G=SL(6,R)? We can see in the following example that there is another real form in the same inner class as SL(6,C). This will be true whenever p+q=2n, namely SL(n,H)::

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

In other words, delta exchanges ``alpha[0]`` and ``alpha[4]``; ``alpha[1]`` and ``alpha[3]`` and fixes ``alpha[2]``.

