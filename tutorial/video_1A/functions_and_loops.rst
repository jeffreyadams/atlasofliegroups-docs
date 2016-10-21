Functions and Loops
===================

To define a function we specify the argument, variable and the
operation(s) performed on the argument. The software then tells us
what type of output the function gives. We can also ask the software
what type of input and output has been specified for the function
``f``.  For example::

   atlas> set f(int x)=x^2
   Defined f: (int->int)
   atlas> whattype f?
   Overloaded instances of 'f'
     int->int
   atlas> f(2)
   Value: 4
   atlas>

We can also specify what the output will be by including it in the definition of the function rather than expecting the software to decide what it would be::

   atlas> set f(int x)=int:x^2
   Redefined f: (int->int)
   atlas>

   atlas> set f(int x, int y)=rat:x/y
   Added definition [2] of f: (int,int->rat)
   atlas> f(3,2)
   Value: 3/2
   atlas>

More functions are defined in the ``.at`` files and we can copy and paste more complicated functions from there.

Arguments and Outputs
---------------------

To find out about the usage of a function you type ``whattype <function name> ?``. ``atlas`` will list all the instances where that function is used with the type of input and output for each case. For example,::

   atlas> whattype inverse ?
   Overloaded instances of 'inverse'
   mat->mat
   atlas>

Gives you the argument and output for the function 'inverse'. It says that the function 'inverse' takes a matrix and produces another matrix.
    
Note: Remember that the command `whattype' without the question mark gives a data type. To get atlas to give you and argument you need to add ``?``::

      atlas> whattype invert ?
      Overloaded instances of 'invert'
      mat->(mat,int)
      atlas>

This says that the function 'invert' takes a matrix and gives back a pair of a matrix and an integer (See the section on Matrices for more information).

To find all usages of the function ``+`` we do::

   atlas> whattype + ?
   Overloaded instances of '+'
   (int,int)->int
   (rat,int)->rat
   (rat,rat)->rat
   (vec,vec)->vec
   (ratvec,ratvec)->ratvec
   (mat,int)->mat
   (int,mat)->mat
   (mat,mat)->mat
   (Split,Split)->Split
   (ParamPol,Param)->ParamPol
   (ParamPol,(Split,Param))->ParamPol
   (ParamPol,[(Split,Param)])->ParamPol
   (ParamPol,ParamPol)->ParamPol
   (string,string)->string
   (string,int)->string
   (int,string)->string
   (string,(int,int))->string
   Split->int
   ([[vec]],[[vec]])->[[vec]]
   ([[vec]],vec)->[[vec]]
   ((Param,string),(Param,string))->(ParamPol,string)
   ((ParamPol,string),(Param,string))->(ParamPol,string)
   ((ParamPol,string),(ParamPol,string))->(ParamPol,string)
   atlas>

Another command that tells us more about function usage for a given input is the command ``@``, which we use in the following format. suppose we want to know what the function inverse does to a matrix. Then we type::

	atlas> inverse@mat
	Value: Function defined at atlas-scripts/basic.at:254:4--256:74
	(M): let (inv,d)=invert@mat(M) in if =@(int,int)(d,1) then inv else error("Matrix not invertible over the integers") fi
	atlas>

Note that it also tells you in which .at file you can find the script of the function::

     atlas> +@(string,string)
     Value: Function defined at atlas-scripts/basic.at:108:0-70
     (s,t): #@(string,string)(s,t)
     atlas>

This is defined in basic, takes a pair of strings and concatenates them

However, if you want to know what '+' does to a matrix and an integer you get::

    atlas>
    atlas> +@(mat,int)
    Value: {+@(mat,int)}
    atlas>

This means this is a built-in function that you can find in the ``atlas-functions.help`` file for information. But, in this case we can also try it to see what it does::

     atlas> set A =id_mat(3)
     Identifier A: mat
     atlas> A
     Value:
     | 1, 0, 0 |
     | 0, 1, 0 |
     | 0, 0, 1 |
     atlas> {A quick way to write the nxn id. matrix}
     atlas>
     atlas> +(A,1)
     Value:
     | 2, 0, 0 |
     | 0, 2, 0 |
     | 0, 0, 2 |
     atlas>

So, it adds a 1 to the diagonal of a matrix.

Loops
-----

Some of the simplest examples of loops are the ``for loops``. For example::

     atlas> for i:3 do i od
     Value: [0,1,2]
     atlas> 

     atlas> set v=for i:3 do i od
     Variable v: [int]
     atlas> v
     Value: [0,1,2]

If we do not want ``atlas `` to print the result we can use either ``void:`` before the loop or ``;()`` at the end of the loop::

   atlas> void:for i:3 do i od
   atlas>

   atlas> for i:3 do i od;()
   atlas>   

A loop can also be used to ask atlas to print from a list. For example::

   atlas> for i:3 do prints(i) od
   0
   1
   2
   Value: [(),(),()]
   atlas>

You can ignore the last line or use the commands above to prevent it from appearing::
 
   atlas> void:for i:3 do prints(i) od
   0
   1
   2
   atlas> for i:3 do prints(i) od;()
   0
   1
   2

Functions defined using loops
------------------------------

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

Another examples are::

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

Now using this type of simple ``for loop`` we can, for example, define
the "flattening" function which takes the columns of a matrix and
writes them concatenated into a single row::

   atlas> set f(mat A)=vec: let rv=vec:[] in for v in A do rv#:=v od;rv
   Added definition [3] of f: (mat->vec)
   atlas> A:=[[1,2],[3,4]]
   Value: 
   | 1, 3 |
   | 2, 4 |
   
   atlas> f(A)
   Value: [ 1, 2, 3, 4 ]
   atlas> 

Again the command above that does this is a loop. The first part
says that the function takes a matrix and outputs a vector.  The
second part defines an empty vector ``rv``. The third part is the loop that
says that for each vector v in the matrix A, append it to what you
have in ``rv``. The last part says, do it for all the vectors in A and print the final result. 

Note the use of the operation ``#`` here means append each ``v`` in ``A`` to the previous iteration.

You can find out more about this operation by typing ``whattype # ?`` and by looking at the ``atlas-functions.help`` file::

    atlas> whattype # ?
    Overloaded instances of '#'
      (string,string)->string
      string->int
      vec->int
      mat->(int,int)
      (vec,int)->vec
      (int,vec)->vec
      (vec,vec)->vec
      (int,[vec])->mat
      LieType->int
      Block->int
      ParamPol->int 

Here is a simple example of what you can do with it::

    atlas> set v=vec:[1,2]
    Identifier v: vec
    atlas> set x=3
    Identifier x: int
    atlas> v#x
    Value: [ 1, 2, 3 ]
    atlas>


There are several kinds of loops which are explained in the
``atlas.help`` file. However, sometimes it is easier to look at some
of the scripts in the ``.at`` files and see how the loops are used to
define functions. In particular the ``basic.at`` file can be useful.

