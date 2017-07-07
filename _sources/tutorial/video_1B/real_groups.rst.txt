Real Groups
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

These is a real Lie group , so the data type is a Real Form. Again the
underlying root datum of :math:`G` is the one for the simply connected
group of type ``A1``::

      atlas> set rd=root_datum (G)
      Identifier rd: RootDatum (hiding previous one of type RootDatum)
      atlas> rd
      Value: simply connected root datum of Lie type 'A1'

Note that :math:`SL(2,\mathbb R)` is NOT simply connected. However, it is the
Lie group whose complexified Lie algebra is type ``A1`` and its root
datum corresponds to the the roots of the simply connected complex
group :math:`SL(2,\mathbb C)`.


Now let's take the non-semisimple Lie group :math:`GL(2,\mathbb R)` ::

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

These are the roots in the basis {e_1, e_2} of the torus :math:`T`. 

Now for :math:`PSL(2,\mathbb R)` we have::

    atlas> set G=PSL(2,R)
    Identifier G: RealForm (hiding previous one of type RealForm)
    atlas> simple_roots(G)
    Value:
    | 1 |
    atlas> simple_coroots(G)
    Value:
    | 2 |
    atlas>

On the other hand if we type ::

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


Which makes sense since :math:`SL(2,\mathbb C)` is the real Lie group with complexified Lie algebra of type ``A1 x A1``,


In general, if we use the standard real form notation for the
groups, ``atlas`` normally gives the usual coordinates. For
example, we can do things like this::


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

These are the usual simple roots for :math:`Sp(4,\mathbb R)`. Using these
pre-defined groups to define our real forms gives us, in most cases, the
familiar coordinates to work with. We can look at all the positive
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

Once again, the pairing between these sets is the usual dot product::


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


Now let us try  :math:`G=GL(3,\mathbb R)`::

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

Here, the semisimple rank is 2, the full rank is 3 and the roots and coroots are expressed again in the usual coordinates. However look what happens for :math:`SL(3,\mathbb R)`::

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

There is also a function called ``Cartan_matrix``. The possible arguments and outputs are given below::

      atlas> whattype Cartan_matrix ?
      Overloaded instances of 'Cartan_matrix'
      LieType->mat
      RootDatum->mat
      (int,int)->mat
      atlas> Cartan_matrix(rd)
      Value:
      | 2, -1 |
      | -1, 2 | 

We will see more about ``atlas`` coordinates in the next section.



