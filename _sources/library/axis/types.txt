Types
========

Introduction
--------------

The axis language is `strongly`_ and `statically`_ typed: the interpreter first
analyses the expressions and definitions given by the user to verify that
types can be attributed to all subexpressions, and all operations are defined
for the types they are applied to; only if the expression passes this test
does the system attempt to evaluate the expression. Thus many computations
that would produce problems on execution are signaled. For instance, after
loading "groups.at" which defined ``GL: (int->RootDatum)``, **atlas** will complain
about::

    atlas> block_sizes (GL(5))
    Type error:
      Subexpression GL(5) at <standard input>:...
      has wrong type: found RootDatum while InnerClass was needed.
    Type check failed

because the built-in function ``block_sizes`` requires an ``InnerClass`` value but
``GL`` produces a value of type ``RootDatum``. In the following example::

    atlas> Lie_type(Cartan_matrix(GL(5)))
    Error in expression Lie_type(Cartan_matrix(GL(5))) at...
      Failed to match 'Lie_type' with argument type mat
    Type check failed

the message is somewhat different, because the name ``Lie_type`` corresponds to
several functions, and **atlas** can only report that none of them applies for
the given expression. To find out which instances are known, one can enter::

    atlas> whattype Lie_type ?
    Overloaded instances of Lie_type
    string->LieType
    RootDatum->LieType
    (int,int)->LieType

(note the question mark, which here means treat ``Lie_type`` as possibly
overloaded function name rather than as a variable) showing that either a
``string`` or a ``RootDatum`` value would have worked instead of a (Cartan) ``matrix``.
For instance::

    atlas> Lie_type(GL(5))
    Value: Lie type 'A4.T1'
    atlas> Lie_type("E6.T1.D4")
    Value: Lie type 'E6.T1.D4'

All built-in operators and functions, and normally also all user defined ones,
are defined as "overloaded" symbols (even if only one meaning is built-in, as
is the case for ``block_sizes``). This allows the user to add new definitions of
those symbols without overriding those built in. On the other hand, the values
of all identifiers that are not functions are stored in a different table,
allowing only one such value at a time to be associated to a given identifier.

.. _statically: https://en.wikipedia.org/wiki/Type_system#Static_type_checking
.. _strongly: https://en.wikipedia.org/wiki/Strong_and_weak_typing

Primitive Types
-------------------

The interpreter knows about several "primitive" types, which it distinguishes
but for which (in contrast to "composite" types discussed below) it usually
does not provide specific language constructions (although it does know for
instance that a Boolean value can be tested in a conditional expression).
These basic types are:

.. list-table::
   :widths: 12 18 20
   :header-rows: 1

   * - Primitive Type
     - Represent
     - Example
   * - bool
     - truth values
     - ``true`` or ``false``
   * - :ref:`int <int_rat_vec>`
     - machine integers (32 or 64 bits) 
     - ``8``
   * - :ref:`rat <int_rat_vec>`
     - rational numbers (quotient of two machine integers)
     - ``2/3``
   * - :ref:`string <string>`
     - string of characters
     - ``"atlas"``
   * - :ref:`vec <int_rat_vec>`
     - vector of machine integers
     - ``vec:[1,2,3]``
   * - mat
     - matrix of machine integers
     - ``id_mat(3)``, ``mat:[[1,2],[3,4]]``
   * - ratvec
     - rational vector (vector numerator with common denominator)
     - ``[1,2]/3``, ``[1/2,2/3]``
   * - LieType
     - Lie type
     - ``D4.A2.T1.E8``
   * - :ref:`RootDatum`
     - root datum, specifying a connected complex reductive group
     - ``simply_connected(LieType:"A1.T1")``
   * - InnerClass
     - inner class of real forms (based root datum with involution)
     - ``inner_class (split_form(E8))``
   * - RealForm
     - real form within an inner class
     - ``SL(3,R)``
   * - CartanClass
     - class of Cartan subgroups within an inner class
     - 
   * - KGBElt
     - element of the set K\G/B associated to some RealForm value
     - 
   * - Block
     - block for a pair of RealForm values (at dual inner classes)
     - 
   * - Split
     - "split integer" a + b.s where s is "split unit" with s^2=1 
     - 
   * - Param
     - value representing a standard module or its irreducible quotient
     - 
   * - ParamPol
     - virtual module with signature (Param values with Split coefs)
     - 


.. note:: If you want to check the data type of something, for example ``id_mat(3)``. You can type ``whattype id_mat(3)`` in **atlas** and it will output ``type: mat``.

.. _string:

string
++++++++

Strings denotations contain newline characters (but a constant
'new_line' is provided, containing a string with a single newline character).
Values of other basic types can only be obtained by using appropriate
operators and functions (for instance 22/7 has type 'rat' and GL(5) has type
'RootDatum'), or sometimes via :ref:`implicit conversions <implicit_conversion>`.

.. _int_rat_vec:

int, rat, & vec
++++++++++++++++

As you might expect, the sum of a ``int`` type and ``rat`` type is a ``rat`` type. Similarly, if you add a ``vec`` type and an array of ``int``, whenever possible, the result is of type ``vec``::

    atlas> set v = vec:[1,2,3]
    Variable v: vec
    atlas> set w = [3,4,5]
    Variable w: [int]
    atlas> v+w
    Value: [ 4, 6, 8 ]

.. _RootDatum:

RootDatum
+++++++++++

In **atlas**, a root datum is a pair of m by n (integral) matrices (A,B) such that (A^T)*B is a Cartan matrix. The number m is rank (number of rows) and n is the semi-simple rank (number of columns).

Composite Types
-----------------

Composite types are either **array (list) types**, **tuple types** or **function types**.
Array and tuple types both construct aggregates by combining a sequence of
component values; for array types all components must have the same type and
there could be any number of them (including none at all), while for tuple
types the type explicitly enumerates the types of the components, so in
particular the number of components is determined by the type. A function type
specifies zero or more argument and result types; for either, unless exactly
one such type is specified the argument or result type is actually a tuple
type. Thus if t0,t1,t2,t3 are types, one has composite types like:

.. list-table::
   :widths: 12 40
   :header-rows: 1

   * - Composite Types
     - Represents
   * - [t0]
     - array of elements all of which have type t0
   * - [[t0]]
     - array of elements all of which have type [t0] (a list of lists)
   * - ...
     - etc
   * - (t0,t1)
     - 2-tuple formed of components of types t0 and t1 respectively
   * - (t0,t1,t2)
     - 3-tuple, with components of types t0,t1,t2 respectively
   * - (t0,t1,t2,t3)
     - 4-tuple, with components of types t0,t1,t2,t3 respectively
   * - ...
     - etc
   * - void
     - 0-tuple (irrelevant value)
   * - (t0->t1)
     - function with argument of type t0 and result of type t1
   * - (t0,t1->t2)
     - function with argument of type (t0,t1) and result of type t2
   * - (t0->t1,t2)
     - function with argument of type t0 and result of type (t1,t2)
   * - (t0,t1->t2,t3)
     - function with argument of type (t0,t1), result of type (t2,t3)
   * - (t0,t1->)
     - function with argument of type (t0,t1) and no useful result
   * - (->t0)
     - function with 0 arguments with result of type t0
   * - ...
     - etc

Often the user does not have to write any types, and the system will take care
of deriving primitive and composite types as implicitly specified by the
expression. However when writing user defined functions, the types of the
arguments must be specified, so that types can be checked for the function
body; once this check succeeds, a type is attributed to the function, and it
will henceforth be treated just like a built-in function of that type would be
(and one can in fact for instance form an array that contains both built-in
and user-defined functions, provided they all have the same (function) type).


