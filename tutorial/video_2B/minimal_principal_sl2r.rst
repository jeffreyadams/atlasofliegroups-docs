Example :math:`G=SL(2,\mathbb R)`.
==================================

If :math:`H` is the split Cartan subgroup of :math:`G`. Let :math:`B` be a borel
including this Cartan subgroup. We can construct the induced representation
:math:`Ind_B ^G (\chi)` where :math:`\chi` is a character of
:math:`H(\mathbb R)`.

For example, if :math:`G=SL(2, \mathbb R )` we can look again at the
list of parameters with infinitesimal character :math:`\rho`.  

Recall the command ``all_parameters_gamma`` takes a real form and an
ifinitesimal character, which is a rational vector, and gives you a
list of parameters for the representations of the real form with that
infinitesimal character::

    atlas> whattype all_parameters_gamma ?
    Overloaded instances of 'all_parameters_gamma'
      (RealForm,ratvec)->[Param]
    atlas> set G=SL(2,R)
    Variable G: RealForm
    atlas> G
    Value: connected split real group with Lie algebra 'sl(2,R)'
    atlas> rho(G)
    Value: [ 1 ]/1
    atlas> set parameters=all_parameters_gamma (G,[1])
    Variable parameters: [Param]
    atlas> #parameters
    Value: 4
    atlas> void: for p in parameters do prints(p) od
    final parameter (x=0,lambda=[1]/1,nu=[0]/1)
    final parameter (x=1,lambda=[1]/1,nu=[0]/1)
    final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    final parameter (x=2,lambda=[2]/1,nu=[1]/1)
    atlas>

Here the ``x`` is giving us Cartan involutions of the Cartan subgroups::

     atlas> involution(KGB(G,0))
     Value: 
     | 1 |
     
     atlas> involution(KGB(G,1))
     Value: 
     | 1 |
     
     atlas> involution(KGB(G,2))
     Value: 
     | -1 |

So, the first two parameters in the list are associated to the compact
Cartan subgroup; the last two to the split one.

We can find out more about the Cartan subgroup for each parameter ``p`` as
follows::

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

So, this is the split Cartan subgroup for this group, with one real factor and
no compact or complex factor. We can ignore the rest of the
information for the moment.  

As we said above, the last two in the list of parameters for :math:`G`
are the ones associated to this split Cartan subgroup; namely the two
principal series with parameter ``nu=1``::

    atlas> parameters[2]
    Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    atlas> parameters[3]
    Value: final parameter (x=2,lambda=[2]/1,nu=[1]/1)
    atlas>

The difference between these two are the ``lambda``. The trivial representation of :math:`G` is::

    atlas> trivial(G)
    Value: final parameter (x=2,lambda=[1]/1,nu=[1]/1)
    atlas>

So, the parameter is the induced representation that has the trivial
as its irreducible quotient. This is the spherical principal
series. There is a rho shift for the ``lambda`` so that the spherical
pricipal series has ``lambda=1`` instead of ``0`` as you might
expect. The other principal series is the non spherical irreducible::

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
representation. Namely, the irreducible principal series itself.

On the other hand, the composition factors of the spherical principal
series are::

    atlas> set ps1=parameters[2] 
    Identifier ps1: Param (hiding previous one of type Param) 
    atlas>
    atlas> show(composition_series (I(ps1)))
    1*J(x=0,lambda=[1/1],nu=[0/1])
    1*J(x=1,lambda=[1/1],nu=[0/1])
    1*J(x=2,lambda=[1/1],nu=[1/1])
    atlas>

This standard module defined by the above parameter has three
composition factors, all irreducible. So ``I(ps1)`` is the sum in the
Grothendieck group of three irreducible composition factors.

Similarly, if we take parameters of a spherical representation with
non-integral infinitesimal character we get irreducibility::

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

So there are two large families of irreducible principal series; one
with parameters of the form ``(x, [1], nu)``, and the other with
parameters ``(x, [0], nu )``, where ``nu`` is non-integral::



Another thing you can do is get also information about cuspidal data used to construct this representation. This is discussed in a separate section.

