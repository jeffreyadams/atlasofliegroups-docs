Rational Matrices
==================

Most operations atlas uses involve integral matrices. However,
rational matrices can be manipulated in ``atlas``. In particular, they
can be inverted directly without having to turn them into integral
matrices. We need a special command because the command ``inverse`` only
inverts matrices which are invertible over the integers. If they are
not, we get an error ::

     atlas> set A=mat:[[2,1],[0,1]]
     Variable A: mat
     atlas> A
     Value: 
     | 2, 0 |
     | 1, 1 |
     atlas> inverse(A)
     Runtime error:
       Matrix not invertible over the integers
     (in call at atlas-scripts/basic.at:295:23-71 of error@string, built-in)
       [inv=
     |  1, 0 |
     | -1, 2 |
     , d=2]
       [M=
     | 2, 0 |
     | 1, 1 |
     ]
     (in call at <standard input>:8:0-10 of inverse@mat, defined at atlas-
     scripts/basic.at:293:4--295:74)
     Evaluation aborted.
     atlas>

Instead we need to use the following::

     atlas> set B=rational_inverse(A)
     Variable B: (mat,string,int)
     atlas> B
     Value: (
     |  1, 0 |
     | -1, 2 |
     ,"/",2)
     atlas>

As you can see a rational matrix is a triple that consists of an
integral matrix, a string consisting of the division sign and an
integer. What this means is that the integral matrix is divided by 2
to give the rational matrix which is the inverse of ``A``

To print the matrix by itself we use the command ``show``::

   atlas> show(B)
   1/2 -1/2 
   0 1 
   atlas> 

We can multiply rational matrices with integral matrices and check in
this case that we do have the inverse of A::

   atlas> B*A
   Value: (
   | 1, 0 |
   | 0, 1 |
   ,"/",1)
   atlas> 

But we can convert a rational matrix which is integral into its integral form::

   atlas> set C=B*A
   Variable C: (mat,string,int) 
   atlas> 
   Value: (
   | 1, 0 |
   | 0, 1 |
   ,"/",1)
   atlas>
   atlas> ratmat_as_mat (C)
   Value: 
   | 1, 0 |
   | 0, 1 |
   atlas>

Rational matrices can also be multiplied with rational vectors and do other operations as with their integral counterparts::

   atlas> B*[3/2, 1/2]
   Value: [  3, -1 ]/4
   atlas>

