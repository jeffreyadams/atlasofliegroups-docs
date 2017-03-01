.. _macs:

###
Mac
###

*********************
Download the software
*********************
* :ref:`direct`
* :ref:`using_git_Mac`
* :ref:`executable_mac`

.. _direct:

Download source code in a single file
=====================================

This is the latest stable version.

+--------------------------+------------------------------+---------------------------------------+
| Version 1.0              |   `atlas_1.0.tgz`_           | source code for Fokko and atlas       |
|                          |                              | including messages and atlas-scripts  |
+--------------------------+------------------------------+---------------------------------------+

.. _atlas_1.0.tgz: http://www.liegroups.org/software/source/1.0/atlas_1.0.tgz

.. _using_git_Mac:

Using git
=========

For users who are not familiar with git, see :ref:`help_git` to get started with git.

If you choose to use git, you can get the most up-to-date version of
the software. Open a terminal window (in the Finder click
Macintosh/Applications/Utilities/Terminal). Make sure your git client
is relatively new. Version 1.7.0.4 and above should work.

To check your git version, on the command line, do::

    git --version

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, then type::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git
    
This creates a subdirectory "atlasofliegroups" and stores the files there.


************************
Installation from Source
************************

After you have the source code, cd to the atlasofliegroups directory.

Compiling atlas for the Mac using Homebrew
===========================================

To compile atlas on a Mac you need to install a C++ compiler (the
default Mac compiler is not up to the task). Homebrew is a package
manager for the Mac, which is an alternative to the more standard MacPorts. 
Homebrew is the preferred method. Alternatively see 
:ref:`macports`.

Install Homebrew
++++++++++++++++

Go to `Homebrew <https://brew.sh>`_  and follow the instructions there to install Homebrew.

(This  is a single command /usr/bin/ruby... executed in a terminal window)

Install the C++ compiler
++++++++++++++++++++++++

Open a terminal window and give the command

     brew install gcc49

Edit two Makefiles
++++++++++++++++++

cd to the directory where you downloaded the source code. Edit the file Makefile 
to replace CXX = g++ -std=c++0x with:

      CXX = /usr/local/Cellar/gcc@4.9/4.9.3_1/bin/g++-4.9  -std=c++0x

The correct path for you might be slightly different from this. cd to /usr/local/Cellar and 
find a file .../bin/g++... and use this.

Make the same change to the file ./sources/interpreter/Makefile

Enable readline
++++++++++++++++++

Give the command 

    brew link --force readline

to install some symbolic links necessary for readline

Compile
+++++++

Give the command

     make atlas

To compile atlas. 

Note: This compiles atlas, with readline. It does *not* compile Fokko. 
To compile Fokko use the command

     make Fokko readline=false

Other Compilation options: 
~~~~~~~~~~~~~~~~~~~~~~~~~~~

We recommend compiling with::

   make atlas verbose=true optimize=true

The option "verbose" makes atlas print a little more information about
what it is doing, like printing a counter during a long
Kazhdan-Lusztig computation. The option "optimize" tells the compiler
to work hard to make the code as fast as possible; this takes slightly
longer to compile, then runs maybe 10% faster.

Other possibilities are::

   debug=true
   readline=false.

The option "debug" makes the software report bad things (for example, negative coefficient in a KL polynomial) that aren't supposed to happen, to detect code problems early. 

(7) Installing Fokko and atlas
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To install the executables in [installation directory] and put symlinks in [binary directory], type::

   make install INSTALLDIR=[installation directory] BINDIR=[binary directory]

The default BINDIR is ``INSTALLDIR/../bin``

Example: 
~~~~~~~~~~~~~
To install the executables in ``/usr/local/atlas``, and symlinks in ``/usr/local/bin``, type::

   sudo make install INSTALLDIR=/usr/local/atlas

(This example only works up to OS 10.10, and you need root access).

Example: 
~~~~~~~~~~
To install the executables in /home/[userid]/software/atlas, and symlinks in /home/userid/bin, type::

   make install INSTALLDIR=/home/[userid]/software BINDIR=/home/[userid]/bin

Example: 
~~~~~~~~~~~

Say you unpacked the software in /home/[userid]/atlas_0.7. To leave the software there, and create symlinks in /home/[userid]/bin, type::

   make install

Next: see :ref:`Running Atlas <run_atlas>` 


.. _installing_cwebx:

Installing cwebx
+++++++++++++++++

The software cwebx is needed to compile atlas. If you downloaded a tgz file from the downloads page, you should not need to install cwebx. If you downloaded the software from github using git, then cwebx is included in the directory cwebx, or available from www-math.univ-poitiers.fr/~maavl/CWEBx.

Running make in the directory cwebx should compile cwebx, and produce the executables cweb/ctanglex and cweb/cweavex. The file sources/interpreter/Makefile tells the compiler to look for these executables. If you move the cwebx directory, or want to use different versions, you must edit this Makefile.

You need to have a working copy of tex in your PATH to run cweavex.

.. _executable_mac:

***********************************
Download and Install an executable
***********************************

The best method is to compile from source. As a backup option you can 
download install an executable file. 

Download a copy of the executable, and the atlas-scripts directory here:

+-------------------------------+------------------------------+-------------------------------------+
| Mac  compiled                 | `atlas_mac_pre_1.0.tgz`_     |  executable, and messages           |
|                               |                              |  atlas-scripts directories          |
+-------------------------------+------------------------------+-------------------------------------+

.. _atlas_mac_pre_1.0.tgz: http://www.liegroups.org/software/source/1.0/atlas_mac_pre_1.0.tgz

Double-click on the file to extract it. 

Open a terminal window, and cd to the directory where the files were downloaded.

Make the file executable:

    chmod u+x atlas

Run the software with the command::

     ./atlas  --path=atlas-scripts all

The path argument tells atlas where to find the scripts, and ``all`` says to load
most of the scripts (not including a few which are under development). (Double-clicking
on the file will launch the application, but will not make the atlas-scripts available.) 
