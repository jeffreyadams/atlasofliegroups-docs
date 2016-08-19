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
   :widths: 12 30
   :header-rows: 1

   * - Primitive Type
     - Represent
   * - :ref:`bool`
     - truth values
   * - :ref:`int <int_rat_vec>`
     - machine integers (32 or 64 bits)
   * - :ref:`rat <int_rat_vec>`
     - rational numbers (quotient of two machine integers)
   * - :ref:`string <string>`
     - string of characters
   * - :ref:`vec <int_rat_vec>`
     - vector of machine integers
   * - :ref:`mat <mat>`
     - matrix of machine integers
   * - :ref:`ratvec`
     - rational vector (vector numerator with common denominator)
   * - :ref:`LieType`
     - Lie type
   * - :ref:`RootDatum`
     - root datum, specifying a connected complex reductive group
   * - :ref:`InnerClass`
     - inner class of real forms (based root datum with involution)
   * - :ref:`RealForm`
     - real form within an inner class
   * - :ref:`CartanClass`
     - class of Cartan subgroups within an inner class
   * - :ref:`KGBElt`
     - element of the set K\\G/B associated to some RealForm value
   * - :ref:`Block`
     - block for a pair of RealForm values (at dual inner classes)
   * - :ref:`Split`
     - "split integer" a + b.s where s is "split unit" with s^2=1 
   * - :ref:`Param`
     - value representing a standard module or its irreducible quotient
   * - :ref:`ParamPol`
     - virtual module with signature (Param values with Split coefs)


.. note:: If you want to check the data type of something, for example ``id_mat(3)``. You can do ``whattype id_mat(3)`` in **atlas** and it will output ``type: mat``.

.. _bool:

bool
+++++

``bool`` represents truth values. Values of bool are ``true``, ``false``::

    atlas> whattype true
    type: bool
    atlas> whattype false
    type: bool


.. _string:

string
++++++++

``string`` represents string of characters. String values can be entered using a double quote::

    atlas> set s = "atlas"
    Variable s: string
    
    

Strings denotations contain newline characters (but a constant
'new_line' is provided, containing a string with a single newline character).
Values of other basic types can only be obtained by using appropriate
operators and functions (for instance 22/7 has type 'rat' and GL(5) has type
'RootDatum'), or sometimes via :ref:`implicit conversions <implicit_conversion>`.

.. _int_rat_vec:

int, rat, & vec
++++++++++++++++

* ``int`` represents machine integers (32 or 64 bits); 
* ``rat`` represents rational numbers (quotient of two machine integers); 
* ``vec`` represents vector of machine integers.

As you might expect, the sum of a ``int`` type and ``rat`` type is a ``rat`` type::
    
    atlas> set a = 2
    Variable a: int
    atlas> set b = 1/2
    Variable b: rat
    atlas> whattype a+b
    type: rat
    

Similarly, if you add a ``vec`` type and an array of ``int``, whenever possible, the result is of type ``vec``::

    atlas> set v = vec:[1,2,3]
    Variable v: vec
    atlas> set w = [3,4,5]
    Variable w: [int]
    atlas> whattype v+w
    type: vec
    
.. _mat:

mat
++++

``mat`` represents matrix of machine integers.

If you directly enter ``[[1,2],[3,4]]``, the type would be set to ``[[int]]``. You need to specifically declare the type ``mat`` if you want ``[[1,2],[3,4]]`` to be a matrix::
    
    atlas> set m = mat : [[1,2],[3,4]]
    Variable m: mat
    
Identity matrix of dimension n is a build-in expression. Suppose :math:`n=3`::

    atlas> id_mat(3)
    Value: 
    | 1, 0, 0 |
    | 0, 1, 0 |
    | 0, 0, 1 |
    
.. _ratvec:

ratvec
+++++++

``ratvec`` represents rational vector (vector numerator with common denominator).

There are two basic ways to declare a rational vector::

    atlas> set v = [1,2,3]/5
    Variable v: ratvec
    atlas> set w = ratvec:[1/2,3/5]
    Variable w: ratvec
    
You can also make array of rational numbers ``[rat]``::
    
    atlas> set w = [1/2,3/5]
    Variable w: [rat]
    
Similar to ``int``, if you add a ``ratvec`` to ``[rat]``, the result is ``ratvec``::

    atlas> set v = [1,2,3]/5
    Variable v: ratvec
    atlas> set w = [1/2,3/5]
    Variable w: [rat]
    atlas> whattype v+w
    type: ratvec
    
.. _LieType:

LieType
++++++++

``LieType`` represents Lie types.

An example of a valid Lie type is "A1.T1"::

    atlas> set l = LieType : "A1.T1"
    Variable l: LieType
    

.. _RootDatum:

RootDatum
+++++++++++

``RootDatum`` represents root datum, specifying a connected complex reductive group.

In **atlas**, a root datum is a pair of :math:`m\times n` (integral) matrices :math:`(A,B)` such that :math:`A^T*B` is a Cartan matrix. The number m is rank (number of rows) and n is the semi-simple rank (number of columns). One way to define a ``RootDatum`` is to use ``LieType``::

    atlas> set rd =  simply_connected(LieType:"A1.T1")
    Variable rd: RootDatum

.. _InnerClass:

InnerClass
++++++++++++++

``InnerClass`` represents inner class of real forms (based root datum with involution).

One can think of an inner class as a set of real forms (of a certain complex Lie group) that share some properties. One can define an inner class in **atlas** as::

    atlas> inner_class(SL(2,R))
    Value: Complex reductive group of type A1, with involution defining
    inner class of type 'c', with 2 real forms and 2 dual real forms
    atlas> whattype inner_class(SL(2,R))
    type: InnerClass
    
.. _RealForm:

RealForm
++++++++++

``RealForm`` represents real form within an inner class.

A simple way of specifying a real form is::
    
    atlas> set G = Sp(4,R)
    Variable G: RealForm

This is enabled by the various user-defined scripts in "atlas-scripts" folder.

If furthermore you want to see all real forms that are in the same inner class as :math:`Sp(4,R)`, do::

    atlas> real_forms(G)
    Value: [compact connected real group with Lie algebra 'sp(2)',connected real group with Lie algebra 'sp(1,1)',connected split real group with Lie algebra 'sp(4,R)']
    
.. _CartanClass:

CartanClass
++++++++++++

``CartanClass`` represents class of Cartan subgroups within an inner class.

For a specific real group :math:`G = Sp(4,R)`, one can ask **atlas** what are the Cartan classes that are in the same inner class::

    atlas> set G = Sp(4,R)
    Variable G: RealForm
    atlas>
    atlas> Cartan_classes(G)
    Value: [Cartan class #0, occurring for 3 real forms and for 1 dual real form,Cartan class #1, occurring for 2 real forms and for 1 dual real form,Cartan class #2, occurring for 1 real form and for 2 dual real forms,Cartan class #3, occurring for 1 real form and for 3 dual real forms]
    atlas>
    atlas> whattype Cartan_classes(G)[1]
    type: CartanClass
    
.. _KGBElt:

KGBElt
+++++++

``KGBElt`` represents element of the set K\G/B associated to some RealForm value.

Given a group :math:`G`, for example :math:`G = SL(2,R)`. One can ask **atlas** to print out the KGB elements associated to different Cartan involutions::

    atlas> set G = SL(2,R)
    Variable G: RealForm (overriding previous instance, which had type RealForm)
    atlas> KGB(G)
    Value: [KGB element #0,KGB element #1,KGB element #2]
    atlas> KGB(G,0)
    Value: KGB element #0

.. _Block:

Block
++++++

``Block`` represents block for a pair of RealForm values (at dual inner classes).

::

    atlas> set G = SL(2,R)
    Variable G: RealForm (overriding previous instance, which had type RealForm)
    atlas> blocks(G)
    Value: [Block of 1 elements,Block of 1 elements,Block of 3 elements]
    atlas> whattype blocks(G)[0]
    type: Block


.. _Split:

Split
++++++

``Split`` represents “split integer” :math:`a + b.s` where s is “split unit” with :math:`s^2=1`.


.. _Param:

Param
++++++

``Param`` represents value representing a standard module or its irreducible quotient.


.. _ParamPol:

ParamPol
+++++++++

``ParamPol`` represents virtual module with signature (Param values with Split coefs).



Composite Types
-----------------

Composite types are either **array (list) types**, **tuple types** or **function types**.
Array and tuple types both construct aggregates by combining a sequence of
component values. The difference is: 

* for array types all components must have the *same* type and there could be any number of them (including none at all);

* for tuple types the type explicitly enumerates the (may-be-*different*) types of the components, so in particular the number of components is determined by the type. 

A function type specifies zero or more argument and result types; for either, unless exactly
one such type is specified, the argument or result type is actually a tuple
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


