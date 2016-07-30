Basic atlas Syntax
==================


This document will tell you about :code:`atlas`'s syntax. To learn about how to launch code:`atlas` see :ref:`run_atlas`.

Basic Operations
------------------

For more examples on the following discussion go to

http://www.liegroups.org/software/download/online_training_videos_IA.html#

``atlas`` is a general purpose programing language written by Marc van Leuwen. It the usual features like loops, conditionals and  expressions as in any programing language. And it has features especially designed for Lie Groups. 
The :code:`atlas` software will do basic arithmetic operations on integers, vectors, and matrices with integral or rational coefficients. These are the basic types of data that :code:`atlas` uses to store and give information on Lie groups structure and representations.

You can ask the software to compute basic operations on the different data types.

To set up a variable, for example ``x=1``, type::

   atlas> set x=1
   Identifier x: int
   atlas>

The second line is :code:`atlas` telling us that it recognizes x as an integer. We can verify we typed the correct variable by typing just x::

    atlas> x
    Value: 1
    atlas>


Another useful command is whattype::
   atlas> wahttype x
   type: int
   atlas>
This tells us the data type (int) of the variable x.

To know more about the different data types you can quit ``atlas`` for a moment and go to the directory atlas-scripts and look for the helpfile atlas.help. This file gives an introduction of the software and how to install it. If you go to #3. Design principles of ``axis`` language, and current limitations, scrolling down you will find information about the details covered in the present document including the list of data types used by the software. Some of them are ``bool`` for boolean, ``int`` for integer, ``rat`` for tational, etc.; and some are related to Lie groups, like LieType, RootDAtum, etc. that we will see later in this notes.

Another useful help file is atlas.functions.help. This has listed all the functions defined on ``atlas``. It describes their domain and range (data types); starting from the basic symbol-operators ``+``, ``_``, ``*``, to booleans, to word-operators like ``null`` that takes an integer ``n`` to the null n-vector, to ``invert`` and ``diagonalize``, which act on matrices, etc.
Finally the file scripts.help which lists most of the supplementary scripts found in this directory and a short description of what they do. The most basic one is ``basic.at`` which includes many useful scripts. We will see how to load them and look at them directly to see what they do.


Useful ``unix`` commands
-------------------------


Another thing you can do in ``atlas`` is hitting the ``TAB`` key twice. Hitting it once does command completion which helps you finish a command if you do not quite remember it. Hitting it twice does command completion on the empty string and it will tell you all possible completions::
   atlas> 
   Display all 204 possibilities? (y or n)
Now, when you type ``y`` it will display all the 204 commands in the software using more, so you can scroll through them when needed. You can also use it to find more than one possible command completions. For example, typing ``nu`` and then ``TAB`` completes to null. Typing ``TAB`` again gives::
   atlas> nu
   {TAB}
   atlas> null
   {TAB}
   null         null_module  
   atlas> null   
which can be very useful if you do not remember a command completely. 
Here the brackets mean a comment. In this case it means that you hit the key in question instead of typing the word. 

Note, if you try this on your version of `atlas` and it does not work it may be because the readline is not working, since it is by the readline library that command completion is implemented. It is reccommended that you get that fixed.
Another useful unix command is ``ctrl-p`` which helps you find the previous command you typed. For example::
   atlas> set y=2
   Identifier y: int
   atlas> {ctrl-p}
   atlas> set y=3
So, you can easily scroll back to the previous commands that you have typed by repeating this step. This is also useful for editing the commands without having to type them all again, as we did in the above example by changing ``y=2`` to ``y=3`` after recalling our previous command. 

A simpler way to do this is to hit the arrow keys. This also lets you scroll forward as well as backward.

Back to Basic Operations
------------------------


