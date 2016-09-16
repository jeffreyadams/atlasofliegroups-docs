Root Data and Lie Types
========================

To start let's talk a bit about Lie types. A Lie type is a product of Complex Lie Algebras of different types. By choosing a Lie type we specify a complex reductive Lie Algebra which is a product of simple and abelian factors. Then we choose a root datum for that Lie type as follows.::

    atlas> set g=LieType:"A1T1"
    Identifier g: LieType
    atlas> g
    Value: Lie type 'A1.T1'
    atlas> set rd=simply_connected (g)
    Identifier rd: RootDatum
    atlas> rd
    Value: simply connected root datum of Lie type 'A1.T1'
    atlas>
    atlas> whattype simply_connected ?
    Overloaded instances of 'simply_connected'
    LieType->RootDatum
    atlas> rd
    Value: simply connected root datum of Lie type 'A1.T1'


This is what ``atlas`` understands as a root datum. The command `simply_connected' applied to a Lie type gives you a root datum. This is a set of simple roots and simple coroots.

Recall that a root datum consists of two lattices,``X^*``,  ``X_*``, with a perfect pairing: ``X^* x X_*->Z  (which  in these coordinates corresponds to the dot product ) and  subsets of simple roots and simple coroots. In the above example we have::

       atlas> simple_roots (rd)
       Value: 
       | 2 |
       | 0 |
       
       atlas> simple_coroots (rd)
       Value: 
       | 1 |
       | 0 |
       
       atlas> 

In atlas, a root datum is a pair of m×n integral matrices (A,B) such that ^{T}AB is the Cartan matrix for the Lie algebra g of the given Lie Type, m= rank of g, and n= semisimple rank of g. In the above example the rank is 2 and the semisimple rank is 1. And we have::

    atlas> set A=simple_roots (rd)
    Identifier A: mat (hiding previous one of type mat)
    atlas> A
    Value:
    | 2 |
    | 0 |
    atlas> set B=simple_coroots (rd)
    Identifier B: mat (hiding previous one of type mat)
    atlas> B
    Value:
    | 1 |
    | 0 |
    atlas> set A=simple_roots (rd)
    Identifier A: mat (hiding previous one of type mat)
    atlas> A
    Value:
    | 2 |
    | 0 |
    atlas> set B=simple_coroots (rd)
    Identifier B: mat (hiding previous one of type mat)
    atlas> B
    Value:
    | 1 |
    | 0 |


These are not necessarily the usual coordinates of this group.
Another example is the Lie Type ``A1``::

	atlas> g:="A1"
	Value: Lie type 'A1'
	atlas> g
	Value: Lie type 'A1'
	atlas> set rd=simply_connected (g)
	Identifier rd: RootDatum (hiding previous one of type RootDatum)
	atlas> rd
	Value: simply connected root datum of Lie type 'A1'
	atlas> simple_roots (rd)
	Value: 
	| 2 |
	
	atlas> simple_coroots (rd)
	Value: 
	| 1 |
	

	atlas> simple_roots (rd)*simple_coroots (rd)
	Value: 
	| 2 |

In this case we have the usual coordinates and the cartan matrix for
``A1`` On the other hand, if we work with the adjoint group, we have
the following situation::

    atlas> rd:=adjoint (g)
    Value: adjoint root datum of Lie type 'A1'
    atlas> simple_roots (rd)
    Value: 
    | 1 |
    
    atlas> simple_coroots (rd)
    Value: 
    | 2 |
    
    atlas> simple_roots (rd)*simple_coroots (rd)
    Value: 
    | 2 |

Here the coordinates of the simple roots and coroots are exchanged. In
these coordinates, in the simply connected case, this means that ``X^* =Z`` and the simple root is ``alpha=[2]``, so ``alpha/2=[1]`` is in X^*`` 

On the other hand, for the adjoint group, we have that ``X^*`` is still ``Z``, the root ``alpha=[1]``  and ``[1]/2`` is NOT in ``X^*``

In general X^* and X_* by definition are Z^n. Where the roots and coroots lie in them has to do with isogenies of the group.


Another useful .at filethat lets you put in Lie types without the quotation marks is the file "lietypes.at". It is also included in the all.at file. This file just defines the Lie types as striings::

	atlas> A1
	Value: "A1"
	atlas>whattype A1
	type: string
	
And now we can type::

    atlas> set g=LieType :A1
    Identifier g: LieType (hiding previous one of type string)
    atlas> g
    Value: Lie type 'A1'
    atlas> whattype A1
    type: string
    
Or we can say::

   atlas> set rd=simply_connected (A1)
   Identifier rd: RootDatum (hiding previous one of type RootDatum)
   atlas> rd
   Value: simply connected root datum of Lie type 'A1'
   atlas>

