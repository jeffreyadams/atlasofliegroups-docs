Blocks
=======

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
principal series at infinitesimal character ``0`` and lambda is
essentially ``rho``. But this is only telling you what the character
is on the :math:`{\math Z}_2` factors. On the other hand the first two
are the limits of discrete series. 

Now let us see where these representations fit in. A very useful thing
is to find the block of a representation ::

   atlas> set t=trivial(G)
   Variable t: Param (overriding previous instance, which had type Param)
   atlas> print_block(t)
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

This is the block of the trivial representation, which as it says
above, it is parameter number 10 in this block, whith real roots
labeled ``r2`` and ``r1``in the ``tau`` invariant. This block has two
principal series in it. Namely the two with ``x=10``. This block has
12 representations and we have seen that there are 18 representations
with infinitesimal character ``rho``. it turns out they are divided
into blocks. The other principal series are in other blocks. Let us find them ::

   set params=all_parameters_gamma(G,rho(G))
   Variable params: [Param]
   atlas> print_block(params[17])
   Parameter defines element 10 of the following block:
    0:  0  [i1,i1]   1   2   ( 4, *)  ( 5, *)  *(x= 0,lam_rho=  [0,0], nu=  [0,0]/1)  e
    1:  0  [i1,i1]   0   3   ( 4, *)  ( 6, *)  *(x= 1,lam_rho=  [0,0], nu=  [0,0]/1)  e
    2:  0  [ic,i1]   2   0   ( *, *)  ( 5, *)  *(x= 2,lam_rho=  [0,0], nu=  [0,0]/1)  e
    3:  0  [ic,i1]   3   1   ( *, *)  ( 6, *)  *(x= 3,lam_rho=  [0,0], nu=  [0,0]/1)  e
    4:  1  [r1,C+]   4   9   ( 0, 1)  ( *, *)  *(x= 4,lam_rho=  [0,0], nu= [1,-1]/2)  1^e
    5:  1  [C+,r1]   7   5   ( *, *)  ( 0, 2)  *(x= 5,lam_rho=  [0,0], nu=  [0,1]/1)  2^e
    6:  1  [C+,r1]   8   6   ( *, *)  ( 1, 3)  *(x= 6,lam_rho=  [0,0], nu=  [0,1]/1)  2^e
    7:  2  [C-,i1]   5   8   ( *, *)  (11, *)  *(x= 7,lam_rho=  [0,0], nu=  [2,0]/1)  1x2^e
    8:  2  [C-,i1]   6   7   ( *, *)  (11, *)  *(x= 8,lam_rho=  [0,0], nu=  [2,0]/1)  1x2^e
    9:  2  [i2,C-]   9   4   (10,11)  ( *, *)  *(x= 9,lam_rho=  [0,0], nu=  [3,3]/2)  2x1^e
   10:  3  [r2,rn]  11  10   ( 9, *)  ( *, *)  *(x=10,lam_rho=  [1,1], nu=  [2,1]/1)  1^2x1^e
   11:  3  [r2,r1]  10  11   ( 9, *)  ( 7, 8)  *(x=10,lam_rho=  [0,0], nu=  [2,1]/1)  1^2x1^e
   atlas> 

This is again the block of the trivial ::

  atlas> print_block(params[16])
  Parameter defines element 0 of the following block:
  0:  0  [rn,rn]  0  0   (*,*)  (*,*)  *(x=10,lam_rho=  [0,1], nu=  [2,1]/1)  1^2x1^e
  atlas>
  atlas> params[16]
  Value: final parameter (x=10,lambda=[2,2]/1,nu=[2,1]/1)
  atlas>

This is another principal series, all by itself in another block
because it is an irreducible principal series. Let us find the other one.

   atlas> print_block(params[15])
   Parameter defines element 4 of the following block:
   0:  0  [C+,rn]  2  0   (*,*)  (*,*)  *(x= 5,lam_rho=  [0,1], nu=  [0,1]/1)  2^e
   1:  0  [C+,rn]  3  1   (*,*)  (*,*)  *(x= 6,lam_rho=  [0,1], nu=  [0,1]/1)  2^e
   2:  1  [C-,i1]  0  3   (*,*)  (4,*)  *(x= 7,lam_rho=  [1,0], nu=  [2,0]/1)  1x2^e
   3:  1  [C-,i1]  1  2   (*,*)  (4,*)  *(x= 8,lam_rho=  [1,0], nu=  [2,0]/1)  1x2^e
   4:  2  [rn,r1]  4  4   (*,*)  (2,3)  *(x=10,lam_rho=  [1,0], nu=  [2,1]/1)  1^2x1^e
   atlas> params[15]
   Value: final parameter (x=10,lambda=[3,1]/1,nu=[2,1]/1)
   atlas>

This is a smaller block but it has the last 5 of the representations with infinitesimal character ``rho``.

So, the blocks are three of sizes are 1, 5, 12 for this group. In fact we can get block sizes information doing the following L::

   atlas> block_sizes (Sp(4,R))
   Value: 
   | 0, 0,  1 |
   | 0, 0,  4 |
   | 1, 5, 12 |

This matrix gives information about the block sizes of all the real forms of Sp(4,R). The last row gives the block sizes for the split group. 

Recall that blocks is where the Kazshdan-Lusztig polynomials live. Also a block is a singleton if and only if the representation is irreducible.

Now do something similar for the real forms of ``E8`` ::

   atlas> void: for H in real_forms(G) do prints(H) od
   compact connected real group with Lie algebra 'e8'
   connected real group with Lie algebra 'e8(e7.su(2))'
   connected split real group with Lie algebra 'e8(R)'
   atlas> 

We have three real forms, the compact one, an intermediate one and the split one ::

   atlas> block_sizes(split_form(E8))
   Value: 
   | 0,     0,      1 |
   | 0,  3150,  73410 |
   | 1, 73410, 453060 |
   
   atlas>

Again the last row gives the block sizes of the blocks of the split real form of ``E8``. There is only one irreducible principal series and 255 reducible ones. 120 are in the second block and 135 in the other block.

As an exercise it is interesting to print each one of thos blocks. 