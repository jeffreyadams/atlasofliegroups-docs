Matrices
=========

A matrix is represented in atlas using the data type ``mat``. As with
vectors, we define a matrix using ``=:`` and listing the entries as sets of n-tuples
in order by columns. Note, as for vectors, the ``:`` distinguishes the matrix
from an array of integers. For example::

  atlas> set A=mat:[[1,2],[3,4]]
  Identifier A: mat 
  atlas> A
  Value: 
  | 1, 3 |
  | 2, 4 |
  
  atlas> set B=[[1,2],[3,4]]
  Identifier B: [[int]]
  atlas> 
  atlas> B
  Value: [[1,2],[3,4]]
  atlas>


Note what happens if we add ``A`` and ``B``::


	 atlas> A+B
	 Internal error: forced value is no vector
	 Evaluation aborted.
	 atlas>

Operations on Matrices
-----------------------

Multiplication on the left, resp. on the right of ``A`` by a vector automatically converts the product into the product of ``A`` by column or row vector respectively.   The transpose of A is obtained using ``^A``::

	       atlas> A*[1,1]
	       Value: [ 4, 6 ]
	       atlas> [1,1]*A
	       Value: [ 3, 7 ]
	       atlas> ^A
	       Value: 
	       | 1, 2 |
	       | 3, 4 |
	       
	       atlas> 


``atlas`` has two commands related to the inverse: The first one, ``invert(A)`` gives
a pair ``(B,d)`` Where ``B`` is an integral multiple, ``d`` of the inverse of
``A``. If ``A`` is invertible over the integers then ``B`` is the
inverse of ``A`` and ``d=1``::


	  atlas> set (B,d)=invert(A)
	  Identifiers B: mat (hiding previous one of type [[int]]), d: int
	  atlas> B
	  Value: 
	  | -4,  3 |
	  |  2, -1 |
	  
	  atlas> d
	  Value: 2
	  atlas> A*B
	  Value: 
	  | 2, 0 |
	  | 0, 2 |
	  
	  atlas>


	  atlas> set C=mat:[[1,0],[1,1]]
	  Identifier C: mat
	  atlas> C
	  Value: 
	  | 1, 1 |
	  | 0, 1 |
	  atlas> invert(C)
	  Value: (
	  | 1, -1 |
	  | 0,  1 |
	  ,1)
	  atlas> 


The second command ``inverse(A) `` is not in the initial software commands. It is defined in the supplementary file ``basic.at``.


Recall that to tell ``atlas`` where to find the ``.at`` files, you need to launch your software using the command ``./atlas --path=atlas-scripts``. If you have not done this yet, you can quit the software and launch it again with this command. 

You can then input the file ``basic.at`` and continue.

