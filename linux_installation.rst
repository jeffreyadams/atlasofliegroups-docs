.. _linux:

######
Linux
######

*********************
Download the software
*********************
* :ref:`using_git` : recommended method.
* :ref:`direct`

.. _using_git:

Using git
=========

For users who are not familiar with git, see :ref:`help_git`.

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, then type::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git
    
This creates a subdirectory "atlasofliegroups" and stores the files there.

.. _direct:

Download the source code directly
=================================

You can download an archive of the source code. These are typically not as up-to-date as
the git version. 

+--------------------------------+------------------------------+-------------------------------------+
| Complete archive               |       `atlas_0.8.tgz`_       | source code, Fokko and atlas        |
+--------------------------------+------------------------------+-------------------------------------+

.. _atlas_0.8.tgz: http://www.liegroups.org/software/atlas_0.8/atlas_0.8.tgz

************************
Installation from Source
************************

After you have downloaded the source code, cd to the atlasofliegroups directory.

Type::

    make

You may need to edit the Makefile to change the line ``CXX = g++ -std=c++0x`` to something 
different. You can choose turn on the verbose option by typing::

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
says to load most of the scripts (not including a few which are under
development). You can also run

./Fokko

 ************************
Installing an executable
************************

The best method is to compile from source. As a backup option you can 
try installing an executable. Download a copy of the executable, 
and the atlas-scripts directory. 

+-----------------------------------+------------------------------+-------------------------------------+
| atlas executable for linux 64 bit |   `atlas_0.8_linux`_         | binary file                         |
+-----------------------------------+------------------------------+-------------------------------------+
| atlas-scripts directory           |   `atlas-scripts_0.8.tgz`_   | just the atlas scripts (.at files)  |
+-----------------------------------+------------------------------+-------------------------------------+

.. _atlas_0.8_linux: http://www.liegroups.org/software/atlas_0.8/atlas_0.8_linux
.. _atlas-scripts_0.8.tgz: http://www.liegroups.org/software/atlas_0.8/atlas-scripts_0.8.tgz

Make the file executable::

     chmod u+x atlas_*.*_linux

Where *.* is replaced by the appropriate number, for example ``chmod u+x atlas_0.8``.
Extract the atlas-scripts directory::

     tar xvfz atlas-scripts.tgz

Run the software with the command::

     ./atlas_*.*_linux  --path=atlas-scripts all

The path argument tells atlas where to find the scripts, and ``all`` says to load
most of the scripts (not including a few which are under development). 




