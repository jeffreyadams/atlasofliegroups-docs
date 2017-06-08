Cuspidal Data for Representations
==================================

Given a parameter ``(x, lambda, nu)`` we can obtain information about
the cuspidal data used to construct the representation. Let us review the parameters of all the representations of :math:`G=SL(2,\mathbb R)` with infinitesimal character ``rho`` ::

    atlas> set G=SL(2,R)
    Variable G: RealForm
    atlas> G
    Value: connected split real group with Lie algebra 'sl(2,R)'
    atlas> rho(G)
    Value: [ 1 ]/1
    atlas> set parameters=all_parameters_gamma(G,rho(G))
    Variable parameters: [Param]
    atlas> void: for p in parameters do prints(p) od
    final parameter (x=0,lambda=[1]/1,nu=[0]/1)
    final parameter (x=1,lambda=[1]/1,nu=[0]/1)
    final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    final parameter (x=2,lambda=[2]/1,nu=[1]/1)
    atlas>
    atlas> set t=trivial(G)
    Variable t: Param
    atlas> t
    Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    atlas>

Now, let us find the cuspidal data for``t`` ::

    atlas> set (P,q)=cuspidal_data(t)
    Variable P: ([int],KGBElt)
    Variable q: Param
    atlas> q
    Value: final parameter (x=0,lambda=[0]/1,nu=[1]/1)
    atlas> Levi(P)
    Value: disconnected split real group with Lie algebra 'gl(1,R)'
    atlas> real_form(q)
    Value: disconnected split real group with Lie algebra 'gl(1,R)'
    atlas> induce_irreducible (q,P,G)
    Value: 
    1*final parameter (x=0,lambda=[1]/1,nu=[0]/1)
    1*final parameter (x=1,lambda=[1]/1,nu=[0]/1)
    1*final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    atlas> 

Recall that the Cartan subgroup for this parameter is the split Cartan subgroup::

    atlas> set x=x(t)
    Variable x: KGBElt
    atlas> x
    Value: KGB element #2
    atlas> set H=Cartan_class(x)
    Variable H: CartanClass (overriding previous instance, which had type string (constant))
    atlas> H
    Value: Cartan class #1, occurring for 1 real form and for 2 dual real forms
    atlas> print_Cartan_info(H)
    compact: 0, complex: 0, split: 1
    canonical twisted involution: 1
    twisted involution orbit size: 1; fiber size: 1; strong inv: 1
    imaginary root system: empty
    real root system: A1
    complex factor: empty

So, we can extract the character of the Cartan subgroup by finding the Cuspidal
data for the representation with parameter ``t``. 

The standard representation containing the trivial is induced from a
parabolic subgroup P with Levi factor equal to :math:`GL(1,R)` and a
character ``q`` of :math:`GL(1,R)` with ``lambda=0`` and ``nu=1``.
 
Moreover, we can see above that when we induce we obtain the composition series
of the spherical principal series that contains the trivial
representation and the two discrete series::

    atlas> t
    Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    atlas>

Similarly we can do the same for the non-spherical principal series::

    atlas> set p=parameters[3]
    Variable p: Param
    atlas> p
    Value: final parameter (x=2,lambda=[2]/1,nu=[1]/1)
    atlas> set (P,q)=cuspidal_data(p)
    Variable P: ([int],KGBElt) (overriding previous instance, which had type ([int],KGBElt))
    Variable q: Param (overriding previous instance, which had type Param)
    atlas> real_form(q)
    Value: disconnected split real group with Lie algebra 'gl(1,R)'
    atlas> q
    Value: final parameter (x=0,lambda=[1]/1,nu=[1]/1)
    atlas> induce_irreducible (q,P,G)
    Value: 
    1*final parameter (x=2,lambda=[2]/1,nu=[1]/1)
    atlas> 
    atlas> p
    Value: final parameter (x=2,lambda=[2]/1,nu=[1]/1)
    atlas>

So, we get the irreducible, non-spherical principal series by inducing
the character on :math:`GL(1,R)` with ``lambda`` and ``nu`` both equal
to ``1`` and from the same parabolic subgroup as in the previous
case. 


Similarly, just to look at another example with non-integral infinitesimal character::

   atlas> set u=parameter(x, [2], [3/2])
   Variable u: Param
   atlas> u
   Value: final parameter (x=2,lambda=[2]/1,nu=[3]/2)
   atlas>
   atlas> set (P,q)=cuspidal_data(u)
   Variable P: ([int],KGBElt) (overriding previous instance, which had type ([int],KGBElt))
   Variable q: Param (overriding previous instance, which had type Param)
   atlas> q
   Value: final parameter (x=0,lambda=[1]/1,nu=[3]/2)
   atlas> Levi(P)
   Value: disconnected split real group with Lie algebra 'gl(1,R)'
   atlas> induce_irreducible(q,P,G)
   Value: 
   1*final parameter (x=2,lambda=[2]/1,nu=[3]/2)
   atlas> u
   Value: final parameter (x=2,lambda=[2]/1,nu=[3]/2)
   atlas> 

So the induced representation is also irreducible as was expected.



