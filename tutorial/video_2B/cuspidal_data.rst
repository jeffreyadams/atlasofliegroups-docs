Cuspidal Data
==============

Another thing you can do is get also information about cuspidal data
used to co\ nstruct this representation::

   set p=parameter(x,[2],[3/2])
   Identifier p: Param (hiding previous one of type Param)
   atlas> set (P,q)=cuspidal_data(q)
   Identifiers P: ([int],KGBElt), q: Param (hiding previous one of type Param)
   atlas> Levi(P)
   Value: disconnected split real group with Lie algebra 'gl(1,R)'
   atlas> q
   Value: final parameter (x=0,lambda=[1]/1,nu=[1]/1)
   atlas> p
   Value: final parameter (x=2,lambda=[2]/1,nu=[1]/1)


So :math:`P` is a parabolic whith Levi factor :math:`GL(1,\mathbb R)`
 and ``q``is acharacter of :math:`GL(1,\mathbb R)`. So we can
 extract the character of the Cartan by finding the Cuspidal data
 for the representation with parameter ``p``::

   atlas>
   atlas> real_form(q)
   Value: disconnected split real group with Lie algebra 'gl(1,R)'
   atlas> Levi(P)
   Value: disconnected split real group with Lie algebra 'gl(1,R)'
   atlas>

   atlas> induce_irreducible (q,P,G)
   Value:
   1*final parameter (x=2,lambda=[2]/1,nu=[3]/2)

