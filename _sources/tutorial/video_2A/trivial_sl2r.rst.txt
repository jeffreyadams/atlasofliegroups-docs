Trivial Representation of :math:`SL(2,R)`
======================================

Let us consider again the case of :math:`SL(2,R)` and the trivial representation.::

   atlas> set G=SL(2,R)
   Identifier G: RealForm
   atlas> G
   Value: connected split real group with Lie algebra 'sl(2,R)'
   atlas> p:=trivial(G)
   Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
   atlas> x:=x(p)
   Value: KGB element #2
   atlas> theta:=involution(x)
   Value: 
   | -1 |
   
   atlas>

So the parameter for the trivial representation contains information
of the Cartan subgroup and its cartan involution, :math:`\theta`,
encoded in the :math:`K\backslash G/B` element ``x``. In this case
:math:`\theta=-1`. This means it is the split Cartan subgroup, which
is isomorphic to :math:`{\mathbb R }^x`

We also have encoded information about the character which, as we saw in the
section on characters of real tori, is given by ``lambda`` and
``nu``. Here ``nu=1`` is the differential of the character, and
``lambda=1`` gives the character on the component group :math:`{\mathbb
Z}/(1-\theta){\mathbb Z}=\mathbb Z/2{\mathbb Z}`, of the torus::

   atlas> (1+theta)*lambda(p)/2 
   Value: [ 0 ]/1
   atlas> (1-theta)*nu(p)/2 
   Value: [ 1 ]/1
   atlas> 


