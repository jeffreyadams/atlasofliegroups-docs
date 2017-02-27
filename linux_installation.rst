.. _linux:

######
Linux
######

*********************
Download the software
*********************
* :ref:`direct`
* :ref:`using_git`
* :ref:`executable`

.. _direct:

Download source code in a single  file
======================================

This is the latest stable version.

+--------------------------+------------------------------+---------------------------------------+
| Version 1.0              |   `atlas_1.0.tgz`_           | source code for Fokko and atlas       |
|                          |                              | including messages and atlas-scripts  |
+--------------------------+------------------------------+---------------------------------------+

.. _atlas_1.0.tgz: http://www.liegroups.org/software/source/1.0/atlas_1.0.tgz


.. _using_git:

Get the source code using git
=============================

For users who are not familiar with git, see :ref:`help_git`.

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, then type::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git
    
This creates a subdirectory "atlasofliegroups" and stores the files there.


************************
Installation from Source
************************

After you have the source code, cd to the atlasofliegroups directory.

Type::

    make

You may need to edit the Makefile to change the line ``CXX = g++ -std=c++0x`` to something 
different, depending on your system. This is specifyingi the C++ compiler.

You can choose turn on the verbose option by typing::

    make verbose=true

This will show you the details of the commands your compiler is using to compile and link the codes.
Some other compiler options are (you can set multiple options separated by spaces)::

    optimize=false    
    debug=true
    readline=false

Optimize is true by default. ``debug=true`` enables more debugging
output, and allows the software to abort if certain tests
fail. ``readline=false`` should only be used if you are getting error
messages related to readline. See :ref:`installation_troubleshooting`.

Ideally, this should compile the code, and produce both ``Fokko`` and
``atlas``. If you encounter any error see see :ref:`installation_troubleshooting`.

We recommend running::

      make install

to put make ``atlas`` accessible from anywhere, and guarantee it has
access to the atlas-scripts directory.  By default this will put a
shell script in ~/bin and points to the atlas-scripts directory.  Make
sure thath ~/bin is in your path. Then the commands ``atlas`` and
``Fokko`` will run the software, (and make the atlas-scripts (for
atlas) and messages (for Fokko) directories available.

To install the excecutable elsewhere run::

   make install BINDIR=path-to-bin-directory

See the Makefile for further options.

Alternatively, in the directory in which you built the software you
can execute 

./atlas --path=atlas-scripts all

The path argument tells atlas where to find the scripts, and ``all``
says to load most of the scripts (possibly excluding a few which are under
development). You can also run

./Fokko

.. _executable:

Download and Install an executable
==================================

The best method is to compile from source. As a backup option you can 
download install an executable file. 

Download a copy of the executable, and the atlas-scripts directory here:

+-----------------------------------+------------------------------+-------------------------------------+
| linux 64 compiled                 | `atlas_linux_pre_1.0.tgz`_   |  executable, and messages           |
|                                   |                              |  atlas-scripts directories          |
+-----------------------------------+------------------------------+-------------------------------------+

.. _atlas_linux_pre_1.0.tgz: http://www.liegroups.org/software/source/1.0/atlas_linux_pre_1.0.tgz

Extract the file:

     tar xvfz atlas_linux_pre_1.0.tgz

cd to the directory:

     cd atlasofliegroups

Make the file executable:

    chmod u+x atlas

Run the software with the command::

     ./atlas  --path=atlas-scripts all

The path argument tells atlas where to find the scripts, and ``all`` says to load
most of the scripts (not including a few which are under development). 

Unfortunately with the precompiled software readline (command line
tools) does not work. For this reason we recommend installing from source.




