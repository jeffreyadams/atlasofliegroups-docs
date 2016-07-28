Basic atlas Syntax
==================


This document will tell you about atlas' syntax. To learn about how to launch atlas see :ref:`run_atlas`.

Basic Operations
------------------

For more examples on the following discussion go to

http://www.liegroups.org/software/download/online_training_videos_IA.html#

Atlas will do basic operations on rationals, integers, vectors and matrices with integral or rational coefficients.. These are the basic types of data that atlas uses to store and give information on Lie groups structure and representations.

You can ask the software to compute basic operations on the different data types

To set up a variable, for example x=1 you type::

   atlas> set x=1
   Identifier x: int
   atlas>

The secnd line is atlas telling us that it recognizes x as an integer. And we c\
an verify we typed the correct variable by typing just x::

    atlas> x
    Value: 1
    atlas>

Another useful command is the command whattype::

        atlas> whattype x
        type: int
        atlas>

Which tells us which data type is the variable x.

