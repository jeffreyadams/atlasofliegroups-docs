Functions and Loops
===================

To define a function we specify the argument, variable and the operation(s) performed on the argument using the following format "set f(<data type> <variable name>)=operation".The software then tells us what type of output the function gives. We can also ask the software what type of input and output has been specified for the function  ``f``.  For example::
   atlas> set f(int x)=x^2
   Defined f: (int->int)
   atlas> whattype f?
   Overloaded instances of 'f'
     int->int
   atlas> f(2)
   Value: 4
   atlas>

We can also specify what the output will be by including it in the definition of the function::

   atlas> set f(int x)=int:x^2
   Redefined f: (int->int)
   atlas>

   atlas> set f(int x, int y)=rat:x/y
   Added definition [2] of f: (int,int->rat)
   atlas> f(3,2)
   Value: 3/2
   atlas>

More functions are defined in the ``.at`` files and we can copy and paste more complicated functions from there.

Loops
-----

We can define some functions using loops. For example, one basic loop lists the column vectors of a matrix as follows::

   atlas> A:=[[1,2],[3,4]]
   Value:
   | 1, 3 |
   | 2, 4 |
   atlas>
   atlas> for v in A do v od
   Value: [[ 1, 2 ],[ 3, 4 ]]
   atlas> 

This is an example of a ``for loop``. Which tells the software that for each v in A you return something. Here od tells ``atlas`` to end the loop once all the vectors of A were listed.

Another example is::

	atlas> v:=[1,2,3,4]
	Value: [1,2,3,4]
	atlas> for a in v do a^2 od
	atlas>
	Value: [1,4,9,16]
	atlas> whattype $
	type: [int]
	atlas> 

Which takes the elements of v, squares them and lists them as an
array of integers.

Now using this type of  simple ``for loop`` we can, for example, define  the `flattening' function which takes the columns of a matrix and writes them concatenated into a single row::

   atlas> set f(mat A)=vec: let rv=vec:[] in for v in A do rv#:=v od;rv
   Added definition [3] of f: (mat->vec)
   
   atlas> A:=[[1,2],[3,4]]
   Value: 
   | 1, 3 |
   | 2, 4 |
   
   atlas> f(A)
   Value: [ 1, 2, 3, 4 ]
   atlas> 

Note that the command above that does this is a loop. The first part
says that the function takes a matrix and outputs a vector.  The
second part defines an empty vector rv. The third part is the loop that
says that for each vector v in the matrix A, append it to what you
have in rv. The last part says, do it for all the vectors in A and print the final result.

There are several kinds of loops which are explained in the ``atlas.help`` file. However, sometimes it is easier to look at some of the scripts in the ``.at`` files and see how the loops are used to define functions. IN particular the ``basic.at`` file can be useful. 