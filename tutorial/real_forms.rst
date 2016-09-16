Real Forms
============


Now we can load another file called ``groups.at``. After doing this
you can scroll up and see the list of all the real forms of all the
familiar complex reductive Lie groups that are defined. This way you
can work with a particular group that you are interested in. For
example::

      atlas> set G=SL(2,R)
      Identifier G: RealForm (hiding previous one of type RealForm)
      atlas> simple_roots(G)
      Value:
      | 2 |
      atlas>simple_coroots(G)
      Value:
      | 1 |
      atlas>

These is a real Lie group , so the data type is a RealForm. Again the underlying root datum of G, which is the one for the simply connected group of type ``A1``::

      atlas> set rd=root_datum (G)
      Identifier rd: RootDatum (hiding previous one of type RootDatum)
      atlas> rd
      Value: simply connected root datum of Lie type 'A1'

Note that SL(2,R) is NOT simply connected. However, it is the Lie group whose complexified Lie algebra is is type A1 and its root datum corresponds to the the roots of the simply connected complex group SL(2,C). 


Now let's take the non semisimple Lie group GL(2,R). We can define it
in two ways. Note the different type of information we obtain::

    atlas> set G=SL(2,R)
    Identifier G: RealForm
    atlas> set rd=root_datum (G)
    Identifier rd: RootDatum (hiding previous one of type RootDatum)
    atlas> rd
    Value: simply connected root datum of Lie type 'A1'
    atlas> G:=GL(2,R)
    Value: disconnected split real group with Lie algebra 'sl(2,R).gl(1,R)'
    
    atlas> simple_roots (G)
    Value: 
    |  1 |
    | -1 |
    
    atlas> simple_coroots (G)
    Value: 
    |  1 |
    | -1 |
    
    atlas>

These are the roots in the basis {e_1, e_2} of the torus T. 

Now for PSL(2,R) we have::

    atlas> set G=PSL(2,R)
    Identifier G: RealForm (hiding previous one of type RealForm)
    atlas> simple_roots(G)
    Value:
    | 1 |
    atlas> simple_coroots(G)
    Value:
    | 2 |
    atlas>

On the other hand if we type::

   atlas> set G=SL(2,C)
   Identifier G: RealForm
   atlas> simple_roots(G)
   Value:
   | 2, 0 |
   | 0, 2 |
   atlas> simple_coroots(G)
   Value:
   | 1, 0 |
   | 0, 1 |
   atlas>


Which makes sense since ``SL(2,C)`` is the real Lie group with complexified Lie algebra of type ``A2 x A2``, 


So, in general, if we use the standard real form notation for the groups, atlas normally gives the usual coordinates. So we can for example do things like this::


    atlas> set G=Sp(4,R)
    Identifier G: RealForm (hiding previous one of type RealForm)
    atlas> set rd=root_datum(G)
    Identifier rd: RootDatum (hiding previous one of type RootDatum)
    atlas> rd
    Value: simply connected root datum of Lie type 'C2'
    atlas> simple_roots(rd)
    Value:
    | 1, 0 |
    | -1, 2 |
    atlas> simple_coroots(rd)
    Value:
    | 1, 0 |
    | -1, 1 |

These are the usual simple roots for Sp(4). So, using these
pre-defined groups to define our real form gives us, in most cases, the
familiar coordinates to work with. So we can look at all the positive
roots and coroots and rho::

     atlas> posroots(rd)
     Value:
     | 1, 0, 1, 2 |
     | -1, 2, 1, 0 |
     atlas> poscoroots(rd)
     Value:
     | 1, 0, 1, 1 |
     | -1, 1, 1, 0 |


     atlas> rho(rd)
     Value: [ 2, 1 ]/1
     atlas>

Again the pairing between these sets is the usual dot product::


      atlas> set alpha=posroots(rd)[0]
      Identifier alpha: vec
      atlas> alpha
      Value: [ 1, -1 ]
      atlas> set alpha_check=poscoroots(rd)[0]
      Identifier alpha_check: vec
      atlas> alpha_check
      Value: [ 1, -1 ]
      atlas> alpha_check
      Value: [ 1, -1 ]
      atlas> alpha*alpha_check
      Value: 2

This is the natural way of pairing roots with coroots. Pairing roots with roots is not too meaningful in the theory. 


Now let us try  G=GL(3,R)::

    atlas> set G=GL(3,R)
    Identifier G: RealForm (hiding previous one of type RealForm)
    atlas> set rd=root_datum(G)
    Identifier rd: RootDatum (hiding previous one of type RootDatum)
    atlas> rd
    Value: simply connected adjoint root datum of Lie type 'A2.T1'
    atlas> simple_roots(rd)
    Value:
    | 1, 0 |
    | -1, 1 |
    | 0, -1 |
    atlas> simple_coroots(rd)
    Value:
    | 1, 0 |
    | -1, 1 |
    | 0, -1 |
    atlas>

Here, the semisimple rank is 2, the full rank is 3 and the roots and coroots are expressed again in the usual coordinates. However look what happens for SL(3,R)::

    atlas> set G=SL(3,R)
    Identifier G: RealForm (hiding previous one of type RealForm)
    atlas> set rd=root_datum(G)
    Identifier rd: RootDatum (hiding previous one of type RootDatum)
    atlas> rd
    Value: simply connected root datum of Lie type 'A2'
    atlas> simple_roots(rd)
    Value:
    | 1, 1 |
    | -1, 2 |
    atlas> simple_coroots(rd)
    Value:
    | 1, 0 |
    | -1, 1 |
    atlas> ^simple_roots(G)*simple_coroots(G)
    Value:
    | 2, -1 |
    | -1, 2 |
    atlas>

Unfortunately these are not the usual coordinates for this group. Nevertheless the Cartan matrix is the usual one.

There is also a function called Cartan_matrix. The possible arguments and outputs are given below::

      atlas> whattype Cartan_matrix ?
      Overloaded instances of 'Cartan_matrix'
      LieType->mat
      RootDatum->mat
      (int,int)->mat
      <example/>atlas> Cartan_matrix(rd)
      Value:
      | 2, -1 |
      | -1, 2 | 


Now let's try a larger group::

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


These are also not the usual coordinates for ``C4``. But again we get
the usual Cartan matrix. And in this case it is equal to the matrix of
the simple roots. So these are good coordinates; the fundamental
weight coordinates. In these corrdinates ``rho`` is::

      atlas> rho(rd)
      Value: [ 1, 1, 1, 1 ]/1
      atlas>

So, in fundamental weight coordinates, the coordinates of ``rho`` are all ``1``.

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

These are isomorphic root data. They are equal up to a change of coordinates. It just takes getting used to understanding which coordinates ``atlas`` is using.

