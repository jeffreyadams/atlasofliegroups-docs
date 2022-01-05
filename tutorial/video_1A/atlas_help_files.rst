Help files
===========


``atlas.help``
--------------


To know more about the different commands and data types of the
software you can quit ``atlas``, go to the directory atlas-scripts
and look for the help file atlas.help. This file has more general information about how the software works, how to use it and how it compares with the Fokko program. It gives an introduction of the software and how to install it. If you go to "#3. Design principles of the ``axis`` language, and current limitations," scrolling down you will find information about the details covered in the present document including the list of data types used by the software. Some of them are ``bool`` for boolean, ``int`` for integer, ``rat`` for rational, etc.; and some are related to Lie groups, like ``LieType``,``RootDatum``, etc. that we will see later in these notes.


``atlas-functions.help``
------------------------

This is the most useful help file that lists all the operations and functions defined in ``atlas``. It describes their domain and range (data types); starting from the basic symbol operators ``+``, ``_``, ``*``, to booleans, to word operators like ``null`` that takes an integer ``n`` to the zero n-vector, to ``invert`` and ``diagonalize``, which act on matrices, etc.

