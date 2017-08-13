General Parameters :math:`Sp(4,\mathbb R )`
============================================

Let us look at all the representations of :math:`Sp(4,\mathbb R )`
with infinitesimal character ``rho`` ::

   atlas> G:=Sp(4,R)
   Value: connected split real group with Lie algebra 'sp(4,R)'
   atlas> set B=block_of (trivial(G))
   Variable B: [Param]
   atlas> print_block(trivial(G))
   Parameter defines element 10 of the following block:
    0:  0  [i1,i1]   1   2   ( 4, *)  ( 5, *)  *(x= 0,lam_rho=  [0,0], nu=  [0,0]/1)  e
    1:  0  [i1,i1]   0   3   ( 4, *)  ( 6, *)  *(x= 1,lam_rho=  [0,0], nu=  [0,0]/1)  e
    2:  0  [ic,i1]   2   0   ( *, *)  ( 5, *)  *(x= 2,lam_rho=  [0,0], nu=  [0,0]/1)  e
    3:  0  [ic,i1]   3   1   ( *, *)  ( 6, *)  *(x= 3,lam_rho=  [0,0], nu=  [0,0]/1)  e
    4:  1  [r1,C+]   4   9   ( 0, 1)  ( *, *)  *(x= 4,lam_rho=  [0,0], nu= [1,-1]/2)  1^e
    5:  1  [C+,r1]   7   5   ( *, *)  ( 0, 2)  *(x= 5,lam_rho=  [0,0], nu=  [0,1]/1)  2^e
    6:  1  [C+,r1]   8   6   ( *, *)  ( 1, 3)  *(x= 6,lam_rho=  [0,0], nu=  [0,1]/1)  2^e
    7:  2  [C-,i1]   5   8   ( *, *)  (10, *)  *(x= 7,lam_rho=  [0,0], nu=  [2,0]/1)  1x2^e
    8:  2  [C-,i1]   6   7   ( *, *)  (10, *)  *(x= 8,lam_rho=  [0,0], nu=  [2,0]/1)  1x2^e
    9:  2  [i2,C-]   9   4   (10,11)  ( *, *)  *(x= 9,lam_rho=  [0,0], nu=  [3,3]/2)  2x1^e
   10:  3  [r2,r1]  11  10   ( 9, *)  ( 7, 8)  *(x=10,lam_rho=  [0,0], nu=  [2,1]/1)  1^2x1^e
   11:  3  [r2,rn]  10  11   ( 9, *)  ( *, *)  *(x=10,lam_rho=  [1,1], nu=  [2,1]/1)  1^2x1^e
   atlas>

There are 12 representations in the block of the trivial of
:math:`Sp(4,\mathbb R)`. The first four and the last two are the ones
we already know. Namely, the four discrete series and the two minimal
principal series of :math:`G`. We know the first four are discrete
series because the roots involved (third column of the above table) are all
imaginary. Also, the second column tells us that their lengts are all
zero. On the other hand the last two correspond to the ``KGB`` element
``x=10`` and all the roots are real. So, this tells us we are in the
split Cartan subgroup and these are minimal principal series.

Now we want to look at the representations numbered 4 to 9. For example::

   atlas> p:=B[5]
   Value: final parameter(x=5,lambda=[2,1]/1,nu=[0,1]/1)
   atlas>
   atlas> infinitesimal_character (p)
   Value: [ 2, 1 ]/1
   atlas>   
   atlas> set x=x(p)
   Variable x: KGBElt
   atlas> x
   Value: KGB element #5
   atlas> infinitesimal_character (p)
   Value: [ 2, 1 ]/1
   atlas> involution(x)
   Value: 
   | 1,  0 |
   | 0, -1 |
   
   atlas> 

This is the Cartan involution for one of the intermediate Cartan
subgroups. Namely the ":math:`SL(2)`- Cartan" or the "long root"
Cartan. The Levi factor is :math:`SL(2,\mathbb R )\times GL(1,\mathbb R )`. More about this later. Let us look at the Cartan involution for this Cartan subgroup ::

   atlas> set theta=involution(x)
   Variable theta: mat 
   atlas> theta
   Value: 
   | 1,  0 |
   | 0, -1 |

   atlas>

Note that the :math:`(-1)`-eigenspace of this involution is the span
of the second coordinate, which is where the``nu`` parameter lives::

   atlas> nu(p)
   Value: [ 0, 1 ]/1
   atlas> 

And ``lambda`` has to do with the restriction to the compact part of the Cartan subgroup of the infinitesimal character. 

Cuspidal Data
---------------

To get more information about the above representation we use a new command ::

   atlas> whattype cuspidal_data ?
   Overloaded instances of 'cuspidal_data'
     Param->(([int],KGBElt),Param)
   atlas>
   atlas> set (P,sigma)=cuspidal_data (p)
   Variable P: ([int],KGBElt)
   Variable sigma: Param
   atlas>
   atlas> P
   Value: ([1],KGB element #7)
   atlas> sigma
   Value: final parameter(x=0,lambda=[1,2]/1,nu=[1,0]/1)
   atlas> 

This is the cuspidal data of the representation with parameter
``p``. That is, :math:`P` is a real parabolic subgroup, ``sigma`` is a
discrete series representation of the Levi factor :math:`M` of
:math:`P` and the standard representation

.. math:: I(p)=Ind_P ^G (\sigma \otimes \nu)

Note that :math:`P` is a pair of a string of integers and a ``KGB``
element. This is a generalization of a Borel and the string of
integers lists the roots on the Levi factor. In this case it is just
root number ``1``.  The `KGB` element information has to do with
:math:`K` orbits on :math:`G/P`, which is a quotient of :math:`K`
orbits on :math:`G/B`. There is more information about this in the
papers section of `Atlas of Lie Groups <http://www.liegroups.org>`_ 

`The main git site <https://git-scm.com/documentation>`_