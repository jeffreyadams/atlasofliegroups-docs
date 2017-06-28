Vectors
=======

Another data type is ``vec``. vectors and other data types like arrays
and matrices are defined using brackets. So in order to specify the
data type you want, you use ``:``. For example, to define, respectively, a vector, an
array of integers and a matrix, we do::

     atlas> set v=vec:[4,6,7]
     Identifier v: vec
     atlas> v
     Value: [ 4, 6, 7 ]
     
     atlas> set w=[4,6,7]
     Identifier w: [int]
     atlas> w
     Value: [4,6,7]
     
     atlas> set A=mat:[[2,4],[1,3]]
     Identifier A: mat
     atlas> A
     Value: 
     | 2, 1 |
     | 4, 3 |
     
     atlas> 


We will see more about matrices and arrays later. Most of the time it
does not matter if you define a vector as an array. For example,
``atlas`` can add ``v+w`` above::


	  atlas> whattype v
	  type: vec
	  atlas> whattype w
	  type: [int]
	  atlas> v+w
	  Value: [  8, 12, 14 ]
	  atlas> whattype(v+w)
	  type: vec
	  atlas>


There are some cases where you need to specify the data type.


Operations and coordinates
--------------------------

The commands for standard operations like length, dot product, coordinates of v, adition and scalar multiplication  are self explanatory::

    atlas> #v
    Value: 3
    atlas> v*v
    Value: 101
    atlas> v[0]
    Value: 4
    atlas> v[1]
    Value: 6
    atlas> v[2]
    Value: 7
    atlas> v[3]
    Runtime error:
      index 3 out of range (0<= . <3) in subscription v[3]
      Evaluation aborted.
    atlas>

    atlas> v+w
    Value: [ 8, 12, 14 ]
    atlas> v/2
    Value: [ 4, 6, 7 ]/2
    atlas> whattype $
    type: ratvec
    atlas>

Note how ``atlas`` converted v/2 to a ratvec. This is a new data type.
Here, we again used ``$`` to call the ``Value`` on the previous line.

