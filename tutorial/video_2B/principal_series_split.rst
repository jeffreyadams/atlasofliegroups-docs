Principal Series of Split Groups
=================================

So far the focus has been on Cartan subgroups, whose information is
encoded on the element ``x`` as the Cartan involution of the complex
abstract group $H$, which determines the real group :math:`H(\mathbb
R)`. Now ``x`` is really a :math:`K`-orbit on :math:`G/B`. So, it is
the support of the corresponding D-module. In order to explain this in
detail we will look at some easy cases. In particular we will be
talking about the principal series of split groups.

So, we start with a group G and a parameter ``p=(x, lambda, nu)``
where x encodes the above information and :math:`\lambda \in X^*
/(1-\theta )X^*` and :math:`\nu \in {X^* \otimes \mathbb Q
}^{-\theta}`. With these data we obtain a character of H(R) with
differential (1+theta lambda /2 + nu.

From this character we get a representation of the group G. 

Minimal Principal Series for split groups
------------------------------------------

If :math:`H` is the split Cartan of :math:`G`. Let :math:`B` be a borel
including this Cartan. We can construct the induced representation
:math:`Ind_B ^G (\chi)` where :math:`\chi` is a character of
:math:`H(\mathbb R)`.

For example, if :math:`G=SL(2, /mathbb R )` we can look again at the
list of parameters with infinitesimal character :math:`\rho`.  

Recall the ``command all_parameters_gamma` takes a real form and an
ifinitesimal character, which is a rational vector, and gives you a
list of parameters for the representations of the real form with that
infinitesimal character::

    atlas> whattype all_parameters_gamma ?
    Overloaded instances of 'all_parameters_gamma'
      (RealForm,ratvec)->[Param]
    atlas> rho(G)
    Value: [ 1 ]/1
    atlas> 
    atlas> G:=SL(2,R)
    Value: connected split real group with Lie algebra 'sl(2,R)'
    atlas> set parameters=all_parameters_gamma (G,[1])
    Identifier parameters: [Param]
    atlas> #parameters
    Value: 4
    atlas> void: for p in parameters do prints(p) od
    final parameter (x=0,lambda=[1]/1,nu=[0]/1)
    final parameter (x=1,lambda=[1]/1,nu=[0]/1)
    final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    final parameter (x=2,lambda=[2]/1,nu=[1]/1)
    atlas>


Here the ``x`` is giving us Cartan involutions of the Cartans::

     atlas> involution(KGB(G,0))
     Value: 
     | 1 |
     
     atlas> involution(KGB(G,1))
     Value: 
     | 1 |
     
     atlas> involution(KGB(G,2))
     Value: 
     | -1 |

We can find out more about the Cartan for each parameter ``p`` as follows::

  atlas> set p= parameters[3]
  Identifier p: Param (hiding previous one of type Param)
  atlas> p
  Value: final parameter (x=2,lambda=[2]/1,nu=[1]/1)
  atlas>
  atlas> x:=x(p)
  Value: KGB element #2
  atlas> set H=Cartan_class(x)
  Identifier H: CartanClass (hiding previous one of type RealForm)
  atlas> print_Cartan_info(H)
  compact: 0, complex: 0, split: 1
  canonical twisted involution: 1
  twisted involution orbit size: 1; fiber size: 1; strong inv: 1
  imaginary root system: empty
  real root system: A1
  complex factor: empty
  atlas>

So, this is the split Cartan for this group, with one real factor and
no compact or complex factor. We can ignore the rest of the
information for the moment.  The last two in the list of parameters
for ``G`` are the ones associated to this split Cartan subgroup;
namely the two principal series with parameter ``nu=1``::

    atlas> parameters[2]
    Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    atlas> parameters[3]
    Value: final parameter (x=2,lambda=[2]/1,nu=[1]/1)
    atlas>

The difference between these two are the ``lambda``. The trivial representation of :math:`G` is::

    atlas> trivial(G)
    Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    atlas>

This is the spherical principal series. There is a rho shift for the
``lambda`` so that the spherical pricipal series has ``lambda=1`` instead of ``0`` as you might expect. The other principal series is the non spherical irreducible::

   atlas> set ps2=parameters[3]
   Identifier ps2: Param
   atlas> ps2
   Value: final parameter (x=2,lambda=[2]/1,nu=[1]/1)
   atlas>
   atlas> set std=I(ps2)
   Identifier I: (Param,string)
   atlas> std
   Value: (final parameter (x=2,lambda=[2]/1,nu=[1]/1),"std") 
   atlas>
   atlas> show(composition_series (std))
   1*J(x=2,lambda=[2/1],nu=[1/1])
   atlas>

Here ``J`` stands for an irreducible representation and the single
line above says that there is only one composition factor in this
representation. Namely, the irreducible itself.

On the other hand, the composition factor of the spherical principal
series is::

    atlas> set ps1=parameters[2] 
    Identifier ps1: Param (hiding previous one of type Param) 
    atlas>
    atlas> show(composition_series (I(ps1)))
    1*J(x=0,lambda=[1/1],nu=[0/1])
    1*J(x=1,lambda=[1/1],nu=[0/1])
    1*J(x=2,lambda=[1/1],nu=[1/1])
    atlas>

This one has three composition factors, all irreducible. So I(ps1) is the sum in the Grothendieck group of three irreducible composition factors.

Similarly, if we take parameters of a spherical representation with non integral infinitesimal character we get irreducibility::

    atlas> x
    Value: KGB element #2
    atlas> set q=parameter (x, [1], [3/2])
    Identifier q: Param (hiding previous one of type Param)
    atlas> infinitesimal_character (q)
    Value: [ 3 ]/2
    atlas> show(composition_series (I(q)))
    1*J(x=2,lambda=[1/1],nu=[3/2])
    atlas>
    atlas> set q=parameter (x, [0], [3/2])
    Identifier q: Param (hiding previous one of type Param)
    atlas> show(composition_series (I(q)))
    1*J(x=2,lambda=[2/1],nu=[3/2])
    atlas>

Cuspidal Data
--------------
