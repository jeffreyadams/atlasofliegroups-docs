Local Variables
================

There is some syntax for the software which is convenient when
performing operations on variables that we need for just a temporary
operation. For example, to calculate ``2^3``, we may proceed as
we have been doing::

    atlas> set x=2
    Variable x: int
    atlas> x^3
    Value: 8
    atlas> set y=x^3
    Variable y: int
    atlas>

Another way is to do::

    atlas> let a=2 in a^3
    Value: 8
    atlas>

So ``a`` here is a local variable that goes away after the operation is performed::

   atlas> a
   Error during analysis of expression at <standard input>:16:0-1
     Undefined identifier 'a'
   Expression analysis failed
   atlas>

Here are other examples where the expressions can be more complicated
or more than one local variable is used::

   atlas> let a=2 in 3*a^2+4*a+1
   Value: 21
   atlas>
   atlas> let a=2 in let b=3 in a^b
   Value: 8
   atlas> let a=2 in let b=3 in let c=4 in a*b*c
   Value: 24
   atlas>
   atlas> let a=2 then b=3 then c=4 in a*b*c
   Value: 24
   atlas>
   atlas> let a=2,  b=3, c=4 in a*b*c
   Value: 24
   atlas>
   atlas> set d=let a=2 then b=3 then c=4 in a*b*c
   Variable d: int
   atlas> d
   Value: 24
   atlas>

Note the last four examples involve the same expression, except we use
different syntax that makes the operation more readable and more
natural and, in the last case, we assign the value of the whole
expression to a new variable ``d``. So this is something we can do in case we need to use d in the future. You can check that the other variables are gone and only ``d`` remains in the ``atlas`` memory

We just need to make sure that the strings of ``let <variable> = something``
are terminated with ``in <expression>''. There are times when the
nested expressions you want can get complicated and it is hard to keep
track. So the software keeps track and reminds you that more
information is needed to finish the expression::

   atlas> let a=2
   L > in let b=3
   L > in a*b
   Value: 6
   atlas>

Another thing to notice, for example, if we use ``y`` in
the expression above, this will not interfere with the process even
though ``y`` was assigned a different value before::

   atlas> let a=2, y=3 in a*y
   Value: 6
   atlas> a
   Error during analysis of expression at <standard input>:71:0-1
     Undefined identifier 'a'
   Expression analysis failed
   atlas> y
   Value: 8
   atlas>

So, ``a`` did go away since it was a local variable. However, the
local value of ``y`` inside the ``let`` syntax dissapeared after the
operation was performed and did not interfered with anything outside. Moreover, its first assigned (non-local) value was retained.

The ``;`` syntax::
-------------------
Another useful syntax symbol is ``;``. It is used between
expressions to ask ``atlas`` to just perform the last operation::

   atlas> let x=2 in let y=3 in x^y; x+y
   Value: 5
   atlas>

A more useful application of this is, for example, with the ``prints``
statements. We may ask atlas to print some output. But if we want
``atlas`` to perform an operation with te output and print both the
intitial output and the result, we may run into the following types of
problems::

   atlas> let x=2 in let y=3 in prints("x=" ,x,"y=",y)
   x=2y=3
   set t=prints("x=" ,x,"y=",y)
   x=2y=8
   Variable t: void
   atlas> t
   atlas>

There are two problems happenning here. When we ask on the first line
to print the values of the local variables ``atlas`` lists them as
part of the string. However, ``atlas`` did not keep in memory the
values of the local variables ``x`` and ``y``. So when we assign a
value to the new variable ``t``, it looked elsewhere for the values of
``x`` and ``y``. Since we had set ``y=2^3``, this was not done as a local variable and  ``atlas`` gives that value for ``y``. 

The second problem is that regardles of whether the variables were
local or not, the ``prints`` command returns type ``void`` and
typing ``t`` again does not give us back what we had asked ``atlas``
to print.

This second problem does not get fixed by redefining ``x`` and ``y``::

   atlas> x:=2
   Value: 2
   atlas> y:=3
   Value: 3
   atlas> t:=prints("x=" ,x,"y=",y)
   x=2y=3
   atlas> t
   atlas> 

So, as before, typing ``t`` again does not recall the values of ``x``
and ``y``.

If we want to perform an operation on ``x`` and ``y`` and have ``atlas`` provide the values we had for those variables. Here is how we
can do this::

   atlas> let x=2 in let y=3 in prints("x=" ,x,"y=",y);x^y
   x=2y=3
   Value: 8
   atlas>

Or, if we want to use the most natural syntax, ::

   atlas> let x=2, y=3 in prints("x=" ,x,"y=",y);x^y
   x=2y=3
   Value: 8
   atlas>

And to make the first output look nicer we can split the ``prints`` command in two::

   atlas> let x=2, y=3 in prints("x=" ,x);prints("y=",y);x^y
   x=2
   y=3
   Value: 8
   atlas>

Use of ``;`` and local variables in ``for`` statements
--------------------------------------------------------

Recall some examples of ``for`` loops::

   atlas> for i:4 do i od
   Value: [0,1,2,3]
   atlas> for i:4 do 2*i od
   Value: [0,2,4,6]
   atlas>
   
   atlas> for i:4 do v#:=2*i od
   Value: [[0],[0,2],[0,2,4],[0,2,4,6]]
   atlas> v
   Value: [0,2,4,6]
   atlas>

The last ``for`` loop uses ``#`` which means append the ith expression
to the previous one. Now if we only care about the last value of
``v``, we can use ``;`` as follows::

   atlas> v:=[]
   Value: []
   atlas> for i:4 do v#:=2*i od;v
   Value: [0,2,4,6]
   atlas>

We can repeat the proces to tack on the same string to the previous one::

   atlas> set w=for i:4 do v#:=2*i od;v
   Variable w: [int]
   atlas> w
   Value: [0,2,4,6,0,2,4,6]
   atlas> set w=for i:4 do v#:=2*i od;v
   Variable w: [int] (overriding previous instance, which had type [int])
   atlas> w
   Value: [0,2,4,6,0,2,4,6,0,2,4,6]
   atlas>

Another way of getting the same output ``v`` is using local variables ::

   atlas> v:=[]
   Value: []
   atlas> v
   Value: []
   atlas> let a=for i:4 do v#:=2*i od in v
   Value: [0,2,4,6]
   atlas>


