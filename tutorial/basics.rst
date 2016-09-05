Getting started
================


This document will tell you about how to get started using ``atlas``. To learn about how to launch :code:`atlas` see :ref:`run_atlas`.


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
	
	atlas> whattype x
        type: int
        atlas>

This tells us the data type (int) of the variable x.


To quit ``atlas`` just type ``quit``

