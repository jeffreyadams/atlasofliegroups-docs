Lowest :math:`K`-types of a Representation
===========================================

We can also look at the lowest :math:`K` types of a
representation. For this we need the command ``highest_weights``::


  atlas> whattype highest_weights ?
  Overloaded instances of 'highest_weights'
    (KGBElt,ratvec)->[(KGBElt,vec)]
    ((KGBElt,ratvec),KGBElt)->[(KGBElt,vec)]
    Param->[(KGBElt,vec)]
    (Param,KGBElt)->[(KGBElt,vec)]
  atlas>


We will use the first instance of the usage of this function in this
case.

A good reference on how to obtain the highest weights of the lowest
:math:`K`-types of a representation is Anthony Knapp's paper, "Minimal
:math:`K`-type formula". Noncommutative harmonic analysis and Lie
groups (Marseille, 1982), 107-118.

To learn about the reverse process of attaching a series of
representations to a given :math:`K`-type see David Vogan's book,
"Representations of real reductive Lie groups". Birkhäusser, 1981

Let's find the lowest :math:`K`-types of each
minimal principal series of :math:`Sp(4,\mathbb R )`. We proceed as
follows ::

   atlas> void: for p in ps do prints(p, " ", highest_weights (p, KGB(G,2))) od 
   final parameter (x=10,lambda=[2,1]/1,nu=[2,1]/1) [(KGB element #2,[ 0, 0 ])] 
   final parameter (x=10,lambda=[3,1]/1,nu=[2,1]/1) [(KGB element #2,[ 1, 0 ]),(KGB element #2,[ 0, -1 ])] 
   final parameter (x=10,lambda=[2,2]/1,nu=[2,1]/1) [(KGB element #2,[ 1, 0 ]),(KGB element #2\ ,[ 0, -1 ])
   final parameter (x=10,lambda=[3,2]/1,nu=[2,1]/1) [(KGB element #2,[ 1, 1 ]),(KGB element #2\ ,[ -1, -1 ])]
   atlas>

The first representation, the trivial one, has lowest :math:`K`-type
[0,0]. The next two have lowest :math:`K`-types [1,0] and [0,-1] and the las
one has :math:`K`-types [1,1] and [-1,-1].

COMMENT: The choice of ``2`` in the input ``KGB(G,2)`` is so that the output of the :math:`K` -types is given in the more familiar coordinates. We will see more about this when we discuss ``KGB`` elements in more detail.