Matrices
=========

A matrix is represented in atlas using the data type ``mat``. As with
vectors, we define a matrix using ``:`` as illustrated below, and listing the entries as sets of n-tuples
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

Multiplication by a vector on the left, (resp. on the right) of ``A``,
automatically converts the product into the product of ``A`` by column
(resp. row) vector.  The transpose of A is obtained using
``^A``::

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


	atlas> invert(A)
	Value: (
	| -4,  3 |
	|  2, -1 |
	,2)
	atlas> 
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


The second command ``inverse(A)`` is not in the initial software
commands. It is defined in the supplementary file ``basic.at``. This
command calculates the inverse of a matrix over the integers.


Recall that to tell ``atlas`` where to find the ``.at`` files, you need to launch your software using the command ``./atlas --path=atlas-scripts``. If you have not done this yet, you can quit the software and launch it again with this command. 

You can then input the file ``basic.at`` and continue.


Now we can see if we can calculate the inverse of these matrices over the integers ::


    atlas> A
    Value: 
    | 1, 3 |
    | 2, 4 |
    
    atlas> inverse(A)
    Runtime error:
      Matrix not invertible over the integers
      (in call of error, built-in)
      (in call of inverse@mat, defined at atlas-scripts/basic.at:254:4--256:74)
      Evaluation aborted.
    atlas> det(A)
    Value: -2

    atlas> C
    Value: 
    | 1, 1 |
    | 0, 1 |
    
    atlas> inverse(C)
    Value: 
    | 1, -1 |
    | 0,  1 |
    
    atlas> C*inverse(C)
    Value: 
    | 1, 0 |
    | 0, 1 |
    atlas>

Basic Linear Algebra operations
-------------------------------


Now lets use a new matrix and try to solve a linear equation. We use
the function ``solve``, that has as input, a matrix and a vector; and as output,
and array of vectors::

    atlas>  A:=[[1,0,0],[0,2,0],[1,1,0]]
    Value: 
    | 1, 0, 1 |
    | 0, 2, 1 |
    | 0, 0, 0 |
    
    atlas>solve(A,[3,4,0])
    Value: [[ -1,  0,  4 ]]
    atlas> whattype $
    type: [vec]
    atlas> 


Recall that we use ``$`` to refer to the previous value. The type of
the output is not a ``vec``, but rather an array of ``vecs``. In this
case, only one ``vec``. 

Note that the general solution of this matrix equation is a one
dimensional vector space. ``atlas`` just chooses a single integer
solution of the equation. To find all the solutions you need to find the kernel.

If we try to solve an equation with no solutions we would get the empty array::


   atlas> solve(A,[0,0,1])
   Value: []
   atlas>

Now we can check our answer. We can do that by identifying the 0th
entry of our array as the vector solution of the linear equation. We
call this vector ``v``::


       atlas> set answer=solve(A,[3,4,0])
       Identifier answer: [vec]
       atlas> answer
       Value: [[ -1,  0,  4 ]]
       atlas> set v=answer[0]
       Identifier v: vec
       atlas> A*v
       Value: [ 3, 4, 0 ]
       atlas>


Now let's calculate the kernel of our singular matrix. We use the function ``kernel`` with input a matrix and output another matrix whose columns are a basis of the kernel::

    atlas> kernel (A)
    Value: 
    |  2 |
    |  1 |
    | -2 |
    

Note this is a matrix. We can multiply it by A and get 0. However, ``atlas`` will not think of it as a vector solution to the matrix equation. In fact, if we call this matrix w, look what happens when we try to multiply ``v+w`` by A::

    atlas> set w= kernel (A) 
    Identifier w: mat 
    atlas> A*(v+w) 
    Error in expression +(v,w) at <standard input>:36:3-6 
      Failed to match '+' with argument type (vec,mat) 
    Type check failed 
    
We need to rename the column vector of ``w``::

    atlas> set u=w[0] 
    Identifier u: vec 
    atlas> u 
    Value: [ 2, 1, -2 ] 
    atlas>
    
    atlas> A*(v+u)
    Value: [ 3, 4, 0 ]
    atlas> 
    
    atlas> A*(v+3*u)
    Value: [ 3, 4, 0 ]
    atlas> 

They are all solutions of our matrix equation as was expected.

Let's try another matrix::

      atlas>  A:=[[1,0,0],[0,0,0],[0,0,0]]
      Value: 
      | 1, 0, 0 |
      | 0, 0, 0 |
      | 0, 0, 0 |
      
      atlas> kernel (A)
      Value: 
      | 0, 0 |
      | 0, 1 |
      | 1, 0 |



 