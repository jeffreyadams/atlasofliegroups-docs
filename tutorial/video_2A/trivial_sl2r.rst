Trivial Representation of ``SL(2,R)``
======================================

Let us consider again the case of ``SL(2,R)`` and the trivial representation.::

   atlas> set G=SL(2,R)
   Identifier G: RealForm
   atlas> G
   Value: connected split real group with Lie algebra 'sl(2,R)'
   atlas> p:=trivial(G)
   Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
   atlas> set x=x(p)
   Identifier x: KGBElt (hiding previous one of type KGBElt)
   atlas> x:=x(p)
   Value: KGB element #2
   atlas> theta:=involution(x)
   Value: 
   | -1 |
   
   atlas>

So the parameter for the trivial representation contains the
information of the Cartan subgroup and its cartan involution, $\theta$
given by x. In this case ``theta=-1``. This means it is the split
Cartan, which is isomorphic to ${\mathbb R }^x$ We also have
information about he character which, as we saw in the section on
characters of real tori, is given by ``lambda=1`` and ``nu=1``. Where
``nu`` is the differential of the Character and ``lambda`` gives the
character on the component group ${\mathbb Z}/(1-\theta){\mathbb Z}=\mathbb Z/2{\mathbb Z}$, of the torus. 

