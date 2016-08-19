Basic Operators
=================

.. list-table::
   :widths: 6 8 16
   :header-rows: 1
   
   * - Operator
     - Argument(s) -> Result(s)
     - Brief Description
   * - ``+``, ``-``, ``*``
     - ``(int,int->int)``
     - usual integer arithmetic operations
   * - ``-``
     - ``(int->int)``
     - integral unary minus
   * - ``^``
     - ``(int,int->int)``
     - | integer exponentiation 
       | (whenever result integral)
   * - ``\``, ``%``
     - ``(int,int->int)``
     - integer (Euclidian) division and remainder
   * - ``\%``
     - ``(int,int->int,int)``
     - Euclidian division with remainder
   * - ``+``, ``-``, ``\*``, ``/``
     - ``(rat,rat->rat)``
     - usual rational arithmetic operations
   * - ``+``, ``-``, ``\*``, ``/``
     - ``(rat,int->rat)``
     - more efficient in applicable bcases
   * - ``%``
     - ``(rat,int->rat)``
     - | remainder after removing 
       | greatest integer multiple
   * - ``%``
     - ``(rat,rat->rat)``
     - | remainder after removing 
       | greatest integer multiple
   * - ``-``
     - ``(rat->rat)``
     - rational unary minus
   * - ``/``
     - ``(rat->rat)``
     - rational unary divide (in other words: inverse)
   * - ``^``
     - ``(rat,int->rat)``
     - | rational exponentiation 
       | (whenever result defined)
   * - ``%``
     - ``(rat->int,int)``
     - pair of numerator and denominator
   * - ``+``, ``-``
     - ``(vec,vec->vec)``
     - addition/subtraction of vectors of equal size
   * - ``-``
     - ``(vec->vec)``
     - vector unary minus
   * - ``*``
     - ``(vec,int->vec)``
     - scalar multiplication (note the operand order)
   * - ``\``
     - ``(vec,int->vec)``
     - scalar division, rounding down
   * - ``%``
     - ``(vec,int->vec)``
     - remainder in scalar division
   * - ``*``
     - ``(vec,vec->int)``
     - scalar product
   * - ``+``, ``-``
     - ``(mat,mat->mat)``
     - matrix addition and subtraction
   * - ``*``
     - ``(mat,vec->vec)``
     - matrix-vector product
   * - ``*``
     - ``(mat,mat->mat)``
     - matrix-matrix product
   * - ``*``
     - ``(vec,mat->mat)``
     - vector-matrix product (vector is transposed)
   * - ``^``
     - ``(mat->mat)``
     - (unary use of ^) matrix transposition
   * - ``^``
     - ``(vec->mat)``
     - | (unary use of ^) (transposed) vector 
       | as 1-line matrix
   * - ``+``, ``-``
     - ``(mat,int->mat)``
     - | addition/subtraction 
       | of multiple of identity
   * - ``+``, ``-``
     - ``(int,mat->mat)``
     - | addition/subtraction 
       | from multiple of identity
   * - ``/``
     - ``(vec,int->ratvec)``
     - vector division giving rational vector
   * - ``%``
     - ``(ratvec->vec,int)``
     - pair of numerator vector and denominator
   * - ``+``, ``-``
     - ``(ratvec,ratvec->ratvec)``
     - additive rational vector arithmetic
   * - ``*``, ``/``, ``%`` 
     - ``(ratvec,int->ratvec)``
     - scalar rational vector operations
   * - ``*``, ``/``
     - ``(ratvec,rat->ratvec)``
     - scalar rational vector operations
   * - ``-``
     - ``(ratvec->ratvec)``
     - unary minus of rational vectors
   * - ``*``
     - ``(mat,ratvec->ratvec)``
     - left-multiplication my matrix of ratvec
   * - ``*``
     - ``(ratvec,mat->ratvec)``
     - right-multiplication my matrix of ratvec
   * - ``=``, ``!=``
     - ``(int->bool)``
     - test for equality/inequality against 0
   * - ``>=``, ``>``
     - ``(int->bool)``
     - | non-negative, positive 
       | (note op. on wrong side)
   * - ``<=``, ``<``
     - ``(int->bool)`` 
     - | non-positive, negative 
       | (note op. on wrong side)
   * - | ``>``, ``>=``, ``<``, ``<=``, 
       | ``=``, ``!=``
     - ``(int,int->bool)``
     - usual relational operators
   * - ``=``, ``!=``
     - ``(rat->bool)``
     - test for equality/inequality against 0/1
   * - ``>=``, ``>``
     - ``(rat->bool)``
     - | non-negative, positive 
       | (note op. on wrong side)
   * - ``<=``, ``<``
     - ``(rat->bool)``
     - | non-positive, negative 
       | (note op. on wrong side)
   * - | ``>``, ``>=``, ``<``, ``<=``, 
       | ``=``, ``!=``
     - ``(rat,rat->bool)``
     - usual relational operators
   * - ``=``, ``!=``
     - ``(bool,bool->bool)``
     - Boolean equivalence, inequivalence (xor)
   * - ``=``, ``!=``
     - ``(string->bool)``
     - test for being (or not being) the empty string
   * - | ``>``, ``>=``, ``<``, ``<=``, 
       | ``=``, ``!=``
     - ``(string,string->bool)``
     - relational operators
   * - ``=``, ``!=``
     - ``(vec->bool)``
     - test for being (or not being) a zero vector
   * - ``>=``, ``>`` 
     - ``(vec->bool)``
     - | test for all entries being 
       | non-negative/positive
   * - ``=``, ``!=``
     - ``(vec,vec->bool)``
     - vector equality and inequality
   * - ``=``, ``!=``
     - ``(ratvec->bool)``
     - test for being a (or not) zero rational vector
   * - ``>=``, ``>``
     - ``(ratvec->bool)``
     - test for all entries non-negative/positive
   * - ``=``, ``!=``
     - ``(ratvec,ratvec->bool)``
     - rational vector equality, inequality
   * - ``=``, ``!=``
     - ``(mat->bool)``
     - test for being a (or not) zero matrix
   * - ``=``, ``!=``
     - ``(mat,mat->bool)``
     - matrix equality and inequality
   * - ``#``
     - ``(string->int)``
     - length of string
   * - ``#``
     - ``(vec->int)``
     - number of components of vector
   * - ``#``
     - ``(ratvec->int)``
     - number of components of rational vector
   * - ``#``
     - ``(mat->int,int)``
     - dimensions (rows, columns) of a matrix
   * - ``#``
     - ``([T]->int)``
     - number of components of row (T is any type)
   * - ``#``
     - ``(string,string->string)``
     - string concatenation
   * - ``#``
     - ``(vec,vec->vec)``
     - concatenation of vectors
   * - ``#``
     - ``(vec,int->vec)``
     - append element to a vector
   * - ``#``
     - ``(int,vec->vec)``
     - prepend element to a vector
   * - ``#``
     - ``([T],[T]->[T])``
     - concatenation of rows (T is any type)
   * - ``#``
     - ``([T],T->[T])``
     - append element to a row (T is any type)
   * - ``#``
     - ``(T,[T]->[T])``
     - prepend element to a row (T is any type)
   * - ``#``
     - ``(int,[vec]->mat)``
     - | combine columns of given fixed height 
       | into matrix
   * - ``^``
     - ``(int,[vec]->mat)``
     - | combine rows of given fixed length 
       | into matrix
   