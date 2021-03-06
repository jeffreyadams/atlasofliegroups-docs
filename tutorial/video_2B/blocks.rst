Blocks of Representations
==========================

Recall that blocks of a representation are where the Kazshdan-Lusztig
polynomials live. So it is vey useful to find the block of a single
representation.

Let :math:`G=Sp(4, \mathbb R)` and let us find the block of the
trivial representation ::

   atlas> G:Sp(4,R)
   Variable G: RealForm (overriding previous instance, which had type RealForm)
   atlas> 
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
labeled ``r2`` and ``r1`` in the ``tau`` invariant. This block has two
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
because it is an irreducible principal series. Let us find the other one ::

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

So, there are three blocks of sizes 1, 5 and 12 each. In fact we can get block sizes information doing the following ::

   atlas> block_sizes (Sp(4,R))
   Value: 
   | 0, 0,  1 |
   | 0, 0,  4 |
   | 1, 5, 12 |

This matrix gives information about the block sizes of all the real
forms of :math:`Sp(4,\mathbb R)`. The last row gives the block sizes for the split
group.

Recall that a block is a singleton if and only if the representation is irreducible.

Now let us look at the other real forms of Sp(4,R) inner class ::

   atlas> set rf=real_forms(G)
   Variable rf: [RealForm]
   atlas> #rf
   Value: 3
   atlas> void: for H in rf do prints(H) od 
   compact connected real group with Lie algebra 'sp(2)'
   connected real group with Lie algebra 'sp(1,1)'
   connected split real group with Lie algebra 'sp(4,R)'
   atlas>

The ``block_sizes`` matrix is the same ::

   atlas> G:=Sp(2,0)
   Value: compact connected real group with Lie algebra 'sp(2)'
   atlas> block_sizes (G)
   Value: 
   | 0, 0,  1 |
   | 0, 0,  4 |
   | 1, 5, 12 |
   
   atlas> all_parameters_gamma (G, rho(G))
   Value: [final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1)]
   atlas>

And for the last real form ::

   atlas> G:=Sp(1,1)
   Value: connected real group with Lie algebra 'sp(1,1)'
   atlas> block_sizes (G)
   Value: 
   | 0, 0,  1 |
   | 0, 0,  4 |
   | 1, 5, 12 |

   atlas> set params=all_parameters_gamma (G, rho(G))
   Variable params: [Param]
   atlas> #params
   Value: 4
   atlas> void: for p in params do prints(p) od
   final parameter(x=3,lambda=[2,1]/1,nu=[3,3]/2)
   final parameter(x=2,lambda=[2,1]/1,nu=[1,-1]/2)
   final parameter(x=1,lambda=[2,1]/1,nu=[0,0]/1)
   final parameter(x=0,lambda=[2,1]/1,nu=[0,0]/1)
   atlas> 

And we can check that the block of the trivial for this group has the same elements ::

   atlas> print_block (trivial(G))
   Parameter defines element 3 of the following block:
   0:  0  [i1,ic]  1  0   (2,*)  (*,*)  *(x=0,lam_rho=  [0,0], nu=  [0,0]/1)  e
   1:  0  [i1,ic]  0  1   (2,*)  (*,*)  *(x=1,lam_rho=  [0,0], nu=  [0,0]/1)  e
   2:  1  [r1,C+]  2  3   (0,1)  (*,*)  *(x=2,lam_rho=  [0,0], nu= [1,-1]/2)  1^e
   3:  2  [ic,C-]  3  2   (*,*)  (*,*)  *(x=3,lam_rho=  [0,0], nu=  [3,3]/2)  2x1^e
   atlas> 


Warning: It doesn't always happen that the ``block_sizes`` matix accounts for all the represenyations at infinitesimal character ``rho``. For example ::

AN EXAMPLE WILL BE COMMING SOON.


Now do something similar for the real forms of ``E8``. For example for the split form ::

   atlas> G:=split_form(E8)
   Value: connected split real group with Lie algebra 'e8(R)'
   atlas> block_sizes(G)
   Value: 
   | 0,     0,      1 |
   | 0,  3150,  73410 |
   | 1, 73410, 453060 |
   
   atlas> 
   
This matrix tells us there are three real forms for :math:`E8`. Recall
that we can find out as follows ::

   atlas> void: for H in real_forms (G) do prints(H) od
   compact connected real group with Lie algebra 'e8'
   connected real group with Lie algebra 'e8(e7.su(2))'
   connected split real group with Lie algebra 'e8(R)'
   atlas>

We have three real forms, the compact one, an intermediate one and the split one.

Again the last row gives the block sizes of the blocks of the split real form of ``E8``. There is only one irreducible principal series and 255 reducible ones. 120 are in the second block and 135 in the other block.

The first row gives the blocks of the compact real form which is just one block of size one. The second row corresponds to the blocks of the intermediate real form. 

As an exercise it is interesting to print each block. 