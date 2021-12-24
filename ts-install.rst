.. _installation_troubleshooting:

Installation -- Trouble Shooting
=================================

During the compile process, errors may occur. This page will help you fix errors regarding:

* :ref:`readline`
* :ref:`ctanglex`
* :ref:`compiler`


.. _readline:

The readline package
--------------------

If you see an error about readline, you probably need to install the readline package.
The readline package to provide very useful command line tools, including CTRL-p for previous line, tab completion, etc.

To compile atlas with readline you need the development version of readline. To install this under **Linux** Debian-based systems (including Ubuntu), do::

    sudo apt-get install libreadline-dev
    
On **redhat**-like systems do::

    sudo yum install libreadline-dev
    
This line in the makefile tells the software where to find the readline library::

    rlincludes = -lreadline -lcurses
    
On some systems it is necessary to replace ``-lcurses`` with ``-lncurses``.

.. note:: If all else fails, you can compile the software without readline ``make readline = false``.

.. _ctanglex:

ctanglex error
--------------

If you see::

    ctanglex: Command not found
    
this means you need to install `CWEBx <http://wwwmathlabo.univ-poitiers.fr/~maavl/CWEBx/>`_. It is included in our distribution of atlas. You can find the subdirectory "cwebx". Running ``make`` under that directory should compile cwebx and generate cwebx/ctanglex and cwebx/cweavex. 

.. note:: The file sources/interpreter/Makefile tells the compiler to look for these executables. If you move the cwebx directory, or want to use different versions you must edit this Makefile.


.. _compiler:

Compiler error
--------------

Your g++ version should be newer than version 9.3. To check your g++ version, do::

    g++ --version

If you are using a C++ compiler that's not g++, you need to edit Makefile. Find the line::

    C++ = g++
    
replace g++ with your C++ compiler.













