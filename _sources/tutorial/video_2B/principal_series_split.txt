Principal Series of Split Groups
=================================

So far the focus has been on Cartan subgroups, whose information is
encoded on the element ``x`` as the Cartan involution of the complex
abstract group :math:`H`, which determines the real group :math:`H(\mathbb
R)`. Now ``x`` is really a :math:`K`-orbit on :math:`G/B`. So, it is
the support of the corresponding :math:`D`-module. In order to explain this in
detail we will look at some easy cases. In particular we will be
talking about the principal series of split groups.

So, we start with a group :math:`G` and a parameter ``p=(x, lambda, nu)``
where x encodes the above information and :math:`\lambda \in X^*
/(1-\theta )X^*` and :math:`\nu \in {X^* \otimes \mathbb Q
}^{-\theta}`. With these data we obtain a character of :math:`H(\mathbb R)` with
differential :math:`{(1+\theta )\over 2}\lambda + nu`.

From this character we get a representation of the group G. 

Minimal Principal Series for split groups
------------------------------------------

If :math:`H` is the split Cartan of :math:`G`. Let :math:`B` be a borel
including this Cartan. We can construct the induced representation
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

So, the first two parameters in the list are associated to the compact
Cartan; the last two to the split one.

We can find out more about the Cartan for each parameter ``p`` as
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

So, this is the split Cartan for this group, with one real factor and
no compact or complex factor. We can ignore the rest of the
information for the moment.  

 As we said above, the last two in the list of parameters for
:math:`G` are the ones associated to this split Cartan subgroup;
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

So there are two large families of irreducible principal series, one
with parameters of the form ``(x, [1], nu)``, and the other with
parameters ``x, [0], nu ), where ``nu`` is non-integral::


Cuspidal Data
--------------

Another thing you can do is get also information about cuspidal data used to construct this representation::

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

So P is a parabolic whith Levifactor GL(1) and q is acharacter of GL(1). So we can extract the character of the Cartan by finding the Cuspidal data for the representation with parameter ``p``::

   atlas> 
   atlas> real_form(q)
   Value: disconnected split real group with Lie algebra 'gl(1,R)'
   atlas> Levi(P)
   Value: disconnected split real group with Lie algebra 'gl(1,R)'
   atlas>

   atlas> induce_irreducible (q,P,G)
   Value: 
   1*final parameter (x=2,lambda=[2]/1,nu=[3]/2)


Aside
-------

NOTE: WHAT FOLLOWS IN THE NEXT LINES IS NOT COMPLETED. I NEED TO WORK A BIT MORE ON WHAT ALL THESE COMMANDS DO. THIS WAS NOT DISCUSSED IN THE VIDEOS AT THIS POINT. BUT I THINK IT WOULD BE GOOD TO HAVE A DISCUSSION HERE ABOUT THESE COMMANDS
Other possible commands arE:: 

   theta_induce_irreducible
   theta_induce_irreducible_as_sum_of_standards
   theta_induce_standard
   theta_stable_data
   theta_stable_parabolic
   theta_stable_parabolics
   theta_stable_parabolics_type

For example::

   atlas> theta_stable_data (p)
   Value: (([0],KGB element #2),final parameter (x=2,lambda=[2]/1,nu=[3]/2))
   atlas> 

In this case the Levi is all of :math:`G`. So this says that the representation is induced from :math:`G` to :math:`G`.

To go back use ``theta_induced_standard``



Another example :math:`G=PSL(2,R)`
-----------------------------------

Another group we can look at is::

   atlas> G:PSL(2,R)
   Variable G: RealForm (overriding previous instance, which had type RealForm)
   atlas> G
   Value: disconnected split real group with Lie algebra 'sl(2,R)'
   atlas>

Here the complex Lie group is :math:`G(\matbbC )=PSL(2,\mathbb C
)=SL(2,\mathbb C)/{\pm 1}`. Its real points are disconnected, and they
are the group :math:`PSL(2, \mathbb R ) \cong SO(2,1)`::

  atlas> rho(G)
  Value: [ 1 ]/2
  atlas> set parameters=all_parameters_gamma (G,rho(G))
  Variable parameters: [Param] (overriding previous instance, which had type [Param])
  atlas>

Note we can use ``rho(G)`` instead of the vector value for :math:`rho`.
The parameters for this group are almost like those  for SL(2,), except that the Weyl group of the compact Cartan has changed and the number of parameters is now just three::

    atlas> #parameters
    Value: 3
    atlas> void: for p in parameters do prints(p) od 
    final parameter (x=0,lambda=[1]/2,nu=[0]/1)
    final parameter (x=1,lambda=[1]/2,nu=[1]/2)
    final parameter (x=1,lambda=[3]/2,nu=[1]/2)
    atlas>

We still have two principal series with infinitesimal character
rho. But we now only have one discrete series representation
associated to the compact Cartan, namely the sum of the two discrete
series for SL(2,R) are now a single irreducible representation of
:math:`PSL(2, R )`.

Now let us look at the trivial representation ::

   atlas> p:trivial(G)
   Variable p: Param
   atlas> p
   atlas> dimension (p)
   Value: 1
   atlas> 

One thing to have in mind is that the trivial representation is always given by the maximal number and lamda and nu =rho

This parameter has composition series::

   Value: final parameter (x=1,lambda=[1]/2,nu=[1]/2)
   atlas> composition_series(I(p))
   Value: (
   1*final parameter (x=0,lambda=[1]/2,nu=[0]/1)
   1*final parameter (x=1,lambda=[1]/2,nu=[1]/2),"irr")
   atlas>

Actually it is best to use the command ``show(composition_series(I(p))))`` ::

   atlas> show(composition_series(I(p)))
   1*J(x=0,lambda=[1/2],nu=[0/1])
   1*J(x=1,lambda=[1/2],nu=[1/2])
   atlas> 


So, this induced representation for :math:`PSL(2,\mathbb R )` has two
factors: the trivial representation (with ``x=1`` and
``lambda=nu=rho``) and a discrete series (with ``x=0``).

What is the other principal series attached to the split Cartan?  For
SL(2, R ) the other representation attached to the split Cartan was an
infinite demensional irreducible principal series. However here we have::

   atlas> q:parameters[2]
   Variable q: Param
   atlas> q
   Value: final parameter (x=1,lambda=[3]/2,nu=[1]/2)
   atlas> is_finite_dimensional (q)
   Value: true
   atlas> p=q
   Value: false
   atlas>
   atlas> p
   Value: final parameter (x=1,lambda=[1]/2,nu=[1]/2)
   atlas> q
   Value: final parameter (x=1,lambda=[3]/2,nu=[1]/2)
   atlas>

This is another one dimensional representation of G not equivalent to
the trivial representation. Recall that :math:`PSL (2,\mathbb R )` is
disconnected, so ``q`` is the parameter for the sign
representation. In other words the standard module attached to this
parameter is a principal series which has as its unique irreducible
quotient the sign representation of :math:`PSL (2,\mathbb R )`.

