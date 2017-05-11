Representations with Zero Infinitesimal Character
==================================================

Let :math:`G=Sp(4, \mathbb R)`. Let us compute all the representations with
infinitesimal character zero ::

    atlas> G:Sp(4,R)
    Variable G: RealForm (overriding previous instance, which had type RealForm)
    atlas> set parameters=all_parameters_gamma(G,[0,0])
    Variable parameters: [Param] (overriding previous instance, which had type [Param])
    atlas> #parameters
    Value: 5
    atlas> void: for p in parameters do prints(p) od
    final parameter (x=0,lambda=[0,0]/1,nu=[0,0]/1)
    final parameter (x=1,lambda=[0,0]/1,nu=[0,0]/1)
    final parameter (x=5,lambda=[0,1]/1,nu=[0,0]/1)
    final parameter (x=6,lambda=[0,1]/1,nu=[0,0]/1)
    final parameter (x=10,lambda=[2,1]/1,nu=[0,0]/1)
    atlas>

Note that ``nu`` is always ``0``. The last row is the spherical
principal series at infinitesimal character ``0`` and ``lambda`` is
essentially ``rho``. But this is only telling you what the character
is on the :math:`{\mathbb Z}_2` factors. On the other end the first two
are the limits of discrete series and we have two intermediate ones.
So we only have one principal series at zero infinitesimal character.