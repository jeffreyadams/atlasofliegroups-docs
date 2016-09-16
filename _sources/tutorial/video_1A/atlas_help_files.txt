Help files
===========


``atlas.help``
--------------


To know more about the different data types you can quit ``atlas`` and go to the directory atlas-scripts and look for the help file atlas.help. This file gives an introduction of the software and how to install it. If you go to "#3. Design principles of ``axis`` language, and current limitations," scrolling down you will find information about the details covered in the present document including the list of data types used by the software. Some of them are ``bool`` for boolean, ``int`` for integer, ``rat`` for rational, etc.; and some are related to Lie groups, like LieType, RootDatum, etc. that we will see later in these notes.


``atlas.functions.help``
------------------------


This is another useful help file that lists all the functions defined on ``atlas``. It describes their domain and range (data types); starting from the basic symbol operators ``+``, ``_``, ``*``, to booleans, to word operators like ``null`` that takes an integer ``n`` to the zero n-vector, to ``invert`` and ``diagonalize``, which act on matrices, etc.


``scripts.help``
-----------------


Finally, this help file lists most of the supplementary scripts found in this directory and a short description of what they do. The most basic one is ``basic.at`` which includes many useful functions. We will see how to load them and look at them directly to see what they do.
