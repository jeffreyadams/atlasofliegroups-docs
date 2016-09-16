``atlas`` choice of coordinates
========================================

Simple roots for ``SL(5,R)``
----------------------------

How do we interpret the way the software writes the simple roots for ``SL(n,R)``? Let us look at an example::

    atlas> set G= SL(5,R)
    Identifier G: RealForm (hiding previous one of type RealForm)
    atlas> simple_roots(G)
    Value:
    | 1, 0, 0, 1 |
    | -1, 1, 0, 1 |
    | 0, -1, 1, 1 |
    | 0, 0, -1, 2 |
    atlas> simple_coroots(G)
    Value:
    | 1, 0, 0, 0 |
    | -1, 1, 0, 0 |
    | 0, -1, 1, 0 |
    | 0, 0, -1, 1 |
    atlas> rho(G)
    Value: [ 4, 3, 2, 1 ]/1
    atlas>sum(simple_roots(G))
    Value: [ 2, 1, 1, 1 ]
    atlas>

So, atlas chooses a set of coordinates to work with. They were chosen
in the "roots.at" file so that the matrix of the simple_coroots for
the simply connected group is the identity matrix::

    atlas> set g=LieType: A4
    Identifier g: LieType (hiding previous one of type LieType)
    atlas> set rd=simply_connected(A4)
    Identifier rd: RootDatum (hiding previous one of type RootDatum)
    atlas> rd
    Value: simply connected root datum of Lie type 'A4'

    atlas> simple_coroots (rd)
    Value: 
    | 1, 0, 0, 0 |
    | 0, 1, 0, 0 |
    | 0, 0, 1, 0 |
    | 0, 0, 0, 1 |
    
    atlas>

But look what happens when we type::

    atlas> G:=SU(5)
    Value: compact connected real group with Lie algebra 'su(5)'
    atlas> simple_coroots (G)
    Value: 
    |  1,  0,  0, 0 |
    | -1,  1,  0, 0 |
    |  0, -1,  1, 0 |
    |  0,  0, -1, 1 |
    
    atlas>

If you want to ask atlas about a vector in the Cartan or say an
infinitesimal character, you need to write it in terms of the simple
roots. Then the software will give you the vector in terms of the ``atlas``
coordinates. For example::

	     atlas> rho(rd)
	     Value: [ 1, 1, 1, 1 ]/1
	     atlas> rho(G)
	     Value: [ 4, 3, 2, 1 ]/1
	     atlas> sum(simple_roots (G))
	     Value: [ 2, 1, 1, 1 ]
	     atlas>sum(simple_roots (rd))
	     Value: [ 1, 0, 0, 1 ]
	     atlas> 
Alternatively, you can try to phrase the question in a way that atlas will use coordinates you are familiar with:: 
	
       atlas> set G= GL(5,R)
       Identifier G: RealForm (hiding previous one of type RealForm)
       atlas> simple_coroots(G)
       Value:
       | 1, 0, 0, 0 |
       | -1, 1, 0, 0 |
       | 0, -1, 1, 0 |
       | 0, 0, -1, 1 |
       | 0, 0, 0, -1 |
       atlas> rho(G)
       Value: [ 2, 1, 0, -1, -2 ]/1

Remark: Once you defined a root datum or group atlas fixes some
coordinates. However, as we have seen, it is often possible to
redefine the group in a different way so that atlas' coordinates are
easier to work with::

       atlas> set rd=root_datum ([[6,2]],[[1,-2]])
       Identifier rd: RootDatum (hiding previous one of type RootDatum)
       atlas> simple_roots(rd)
       Value:
       | 6 |
       | 2 |
       atlas> simple_coroots(rd)
       Value:
       | 1 |
       | -2 |
       atlas> rho (rd)
       Value: [ 3, 1 ]/1
       atlas> ^simple_roots(rd)*simple_coroots(rd)
       Value:
       | 2 |
       atlas> rd
       Value: simply connected root datum of Lie type 'A1.T1'
       atlas>

Notice this is a version of the root_datum command that we had not seen. It says `please give me the root datum for the following set of simple roots and coroots'. That is what a root datum is in atlas. So you can define the root datum by giving the matrices you want for the simple roots and coroots and atlas will accept them as a root datum. It is not clear which of the three isomorphism classes of root data for this type this one is.

Now lets look at a another example.

    atlas> set rd=simply_connected (C4)
    Identifier rd: RootDatum (hiding previous one of type RootDatum)
    atlas> simple_roots (rd)
    Value:
    |  2, -1,  0,  0 |
    | -1,  2, -1,  0 |
    |  0, -1,  2, -2 |
    |  0,  0, -1,  2 |

    atlas> simple_coroots (rd)
    Value:
    | 1, 0, 0, 0 |
    | 0, 1, 0, 0 |
    | 0, 0, 1, 0 |
    | 0, 0, 0, 1 |

    atlas> ^simple_roots (rd)*simple_coroots (rd)
    Value:
    |  2, -1,  0,  0 |
    | -1,  2, -1,  0 |
    |  0, -1,  2, -1 |
    |  0,  0, -2,  2 |
    
    atlas>

Again these are not the usual simple roots and corroots. But as you
can see we get the Cartan matrix with the above product. These are the fundamental weights coordinates. Observe also that the simple coroots (resp. simple roots) give the identity matrix (resp. the Cartan matrix), which you would expect for the simply connected group of type ``C4``.

In these corrdinates ``rho`` is::

      atlas> rho(rd)
      Value: [ 1, 1, 1, 1 ]/1
      atlas>

So, in fundamental weight coordinates, the coordinates of ``rho`` are all ``1``.
You can also check that if you use the adjoint root datum for ``C4``, the simple
roots matrix will be the identity etc.

But now, if we use  the defined real form ``Sp(8)``, we get root data in the usual coordinates::

    atlas> G:=Sp(8,R)
    Value: connected split real group with Lie algebra 'sp(8,R)'
    atlas> simple_roots (G)
    Value:
    |  1,  0,  0, 0 |
    | -1,  1,  0, 0 |
    |  0, -1,  1, 0 |
    |  0,  0, -1, 2 |

    atlas> rho(G)
    Value: [ 4, 3, 2, 1 ]/1
    atlas>

These are isomorphic root data. They are equal up to a change of
coordinates. It just takes getting used to understanding which
coordinates ``atlas`` is using.


