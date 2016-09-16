Getting started using the software
==================================


This document will tell you about how to get started using ``atlas``. To learn about how to launch :code:`atlas` see :ref:`run_atlas`.

To quit ``atlas`` just type ``quit`` 

(Or type ``^Z`` to quit it momentarily and put it in the background. Then type ``^fg`` to get it back in the foreground)

The ``atlas`` software will do basic arithmetic operations on integers, vectors, and matrices with integral or rational coefficients. These are the basic types of data that``atlas`` uses to store and give information on Lie groups structure and representations.


You can ask the software to compute basic operations on the different data types.

To set up a variable, for example ``x=1``, type::

   atlas> set x=1
   Identifier x: int
   atlas>

The second line is ``atlas`` telling us that it recognizes x as an integer. We can verify we typed the correct variable by typing just x::

    atlas> x
    Value: 1


Sometimes we want to ask atlas to repeat the previous value. We use ``$`` for that::

    atlas> $
    Value: 1

Another useful command is whattype::
	
	atlas> whattype x
        type: int
        atlas>

This tells us the data type (int) of the variable x. For more information on data types go to :ref:`basic_commands` 

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
file that are now added to the built-in commands. You can see what you have now by scrolling back on your screen. As we cover more features of the subject we will need other ``.at`` files loaded.

For more detail on the commands included in any ``.at`` file you can go to the file itself using ``more`` or ``emacs``.

