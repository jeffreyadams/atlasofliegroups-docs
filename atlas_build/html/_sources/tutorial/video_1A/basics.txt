Getting started using the software
==================================


This document will tell you about how to get started using ``atlas``. To learn about how to launch :code:`atlas` see :ref:`run_atlas`.

To quit ``atlas`` just type ``quit`` 

(Or type ``^Z`` to quit it momentarily and put it in the background. Then type ``fg`` to get it back in the foreground)

The ``atlas`` software will do basic arithmetic operations on integers, vectors, and matrices with integral or rational coefficients. These are the basic types of data that``atlas`` uses to store and give information on Lie groups structure and representations.


You can ask the software to compute basic operations on the different data types.

To set up a variable, for example ``x=1``, type::

   atlas> set x=1
   Identifier x: int
   atlas>

The second line is ``atlas`` telling us that it recognizes ``x`` as an integer. ``atlas`` assigns a memory location in the computer for future operations involving the value assigned to that variable. We can verify we assigned the correct value to the variable by typing just ``x``::

    atlas> x
    Value: 1


Sometimes we want to ask ``atlas`` to repeat the previous value or to use it to perform an operation on it. We use ``$`` for this::

    atlas> $
    Value: 1
    atlas> $+2
    Value: 3
    atlas>

A useful way to change the value assigned to a variable is using the
command ``:=``. However this works as long as the new value is of the
same data type as the old one. You may also  notice in the example below
that, if we don't use this way of assigning a new value to the variable, we get a
message "hiding previous one of type ...." ::

	atlas> set x=2 
	Identifier x: int (hiding previous one of type int) 
	atlas> x 
	Value: 2 
	atlas> x:=5 
	Value: 5 
	atlas> x:=2/3
        Error during analysis of expression at <standard input>:33:0-6
        Type error: 
  	  Subexpression /(2,3) at <standard input>:33:3-6
	  has wrong type: found rat while int was needed.  
	Type check failed 
	atlas>


The software will often accept a simpler data type (like an integer) in a place where a more complicated one (like a rational number) is required, as long as this can be done without ambiguity::


   atlas> y:=3
   Identifier y: int
   atlas> set z=3/2
   Identifier z: rat
   atlas> y+z
   Value: 9/2
   atlas> whattype(y+z)
   type: rat
   atlas>


This works in most cases. However, there are some exceptions when the software does not switch to the appropriate data type.


Another useful command is whattype::
	
	atlas> whattype x
        type: int
        atlas>

This tells us the data type (int) of the variable x. For more information on data types go to :ref:`basic_commands`` 

The ``basic.at`` file
----------------------

When you launch ``atlas`` with the standard built-in commands only,
you sometimes may need another command that is not included there
and you get an error telling you the command is undefined. The reason
is because the command may be defined in a supplementary file that
needs to be loaded. The ``basic.at`` contains most of the commands you will need to get familiar with the software.

We need to introduce two other commands.

``<`` is the input command that will help you load the ``.at`` files that you want.

``>`` is the output command. More on this later.

There are a few supplementary files that you may want to load right
away as you launch the software. If you haven't done so or you don't
remember, you can type ``<basic.at`` for example. If you get an error
saying it failed to input the file, you need to quit ``atlas`` for a moment to learn how to do that.

The supplementary files are in the directory ``atlas-scripts``. But
``atlas`` needs to know where they are. So you need to launch it again
providing the path it needs to take. Go to :ref:`run_atlas` for
information about this. (Make sure you are in the directory
where you downloaded ``atlas`` and type ``ls`` to verify that the ``atlas-scripts`` directory is there).

You can also ``cd`` into that directory to see all the supplementary files available. These are all the ``.at`` files listed there. 

After you launched the file with the path information, you can load the file ``basic.at``::

      atlas> <basic.at 
      Starting to read from file 'atlas-scripts/basic.at'.


After this the software will list all the scripts included in the ``basic.at``
file that are now added to the built-in commands. You can see what you have now by scrolling back on your screen. As we cover more features of the subject we will need to load other ``.at`` files.

For more detail on the commands included in any ``.at`` file you can go to the file itself using ``more`` or ``emacs``.

