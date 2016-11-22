.. _macs:

Mac
---

Download the software
~~~~~~~~~~~~~~~~~~~~~~

You have two options:

* :ref:`using_git_Mac` : recommended method.
* :ref:`using_link_Mac`

.. _using_git_Mac:

Using git
+++++++++

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

.. _using_link_Mac:

Using provided links
++++++++++++++++++++

We recommend you to download the latest version.

+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| Latest atlas-scripts directory | `atlas-scripts.0.7.0.tgz`_           | supplementary files for atlas                                                                                                         |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| Latest complete version: 0.7   | `atlas_0.7.tgz`_                     | source code, Fokko and atlas                                                                                                          |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+

.. _atlas_0.7.tgz: http://www.liegroups.org/software/atlas_0.7/atlas_0.7.tgz
.. _atlas-scripts.0.7.0.tgz: http://www.liegroups.org/software/atlas_0.7/atlas_0.7.0.tgz


Compiling atlas for the Mac using MacPorts
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Regardless of how you download the atlas software you will need to
compile it.  This is the preferred method. For other Mac options see
:ref: `other methods of installing on the Mac`.

You are going to install the gcc C compiler (provided by MacPorts),
which is preferred for installing Fokko and atlas. To do so you must
first install the XCode C Compiler. See :ref: `C Compilers for the
Mac` for an explantion.

(1) Install MacPorts. 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

(If MacPorts is installed on your system go to
step (2)). Visit `macports.org <https://www.macports.org>`, go to
`Installing MacPorts <https://www.macports.org/install.php>`, and
download the dmg file for your version of MAC OSX (for example
10.7.*=Lion). Double click on the dmg file to install MacPorts. You
need to be an administrative user, and will need to enter your
password.

(2) Install the XCode C compiler. 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you already have XCode installed, go to step (3) (XCode is not installed by default).

The XCode package is huge, and includes a lot of unnecessary tools. We
recommend downloading and installing just the `XCode command line
tools <https://developer.apple.com/downloads/index.action#>`, which
have everything you need. 

Alternatively install the entire `Xcode <https://developer.apple.com/xcode>`
package. In either case you will need a (free) Apple ID.

Once you have the XCode command line tools, you will have a C compiler /usr/bin/gcc. You can test this in a terminal window by typing::

     gcc -v

The response should be, on an earlier OS, something like::

    Configured with: --prefix=/Applications/Xcode.app/Contents/Developer/usr...

Or, if you are using Sierra or El Capitan::

   Configured with: --prefix=/Library/Developer/CommandLineTools/usr
   --with-gxx-include-dir=/usr/include/c++/4.2.1

(3) Install the MacPorts (gcc) C Compiler
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Open a terminal window (Terminal is available in Applications). All further commands are given from within this window. Give the command::

   sudo port install gcc49

to install the Macports version of gcc. 

Be sure to be connected to the internet at this point! (Other Macports
versions of gcc starting with 4.4 should also work; if you have or
download a different version, you'll need to change "4.9"
appropriately below.) If you are using only the command line tools of
Xcode (not the full XCode installation) ignore the warning about not
finding XCode. After a few minutes [or a few hours: some MacPorts
things can take a VERY long time. Safest to do this overnight,
connected to a power source] you should have /opt/local/bin/gcc-mp-4.9
(the MacPorts C compiler) and /opt/local/bin/g++-mp-4.9 (the MacPorts
C++ compiler). You can check these things in a terminal window by
typing::

   ls /opt/local/bin/g*

Also the directory /opt/local/bin has been added to your PATH environment variable.

(4) Install readline
~~~~~~~~~~~~~~~~~~~~~~~~~~

Do::

   sudo port install readline

to install the readline package.

(5) Edit the Makefiles
~~~~~~~~~~~~~~~~~~~~~~~~~~

You will need to edit two files to tell your computer which compiler to use.

(A) In the atlasofliegroups directory, edit the Makefile as follows:

First search for CXX and find the following text::

  # the compiler to use, including language switch 
  #some C++11 supportneeded (rvalue references, shared_ptr) but g++-4.4 suffices
  CXX = g++- -std=c++0x

Then edit the last line to read::
 
  CXX = g++-mp-4.9 -std=c++0x

Or modify for the version of of compiler that you have downloaded. 
and also edit the line::

  rl_libs ?= -lreadline

to read::

   rl_libs ?= -lreadline -lcurses -L/opt/local/lib

(to tell the compiler where to find the readline libraries).

(B) In addition, in the directory
``atlasofliegroups/sources/intepreter``, you need to modify the
Makefile in there. Search again for ``CXX`` and find the following
text::

   # our C++ compiler (call language version c++0x, for backward compatibility)     
   CXX := g++ -std=c++0x

Then edit the last line to read::

   CXX := g++-mp-4.7 -std=c++0x -I/opt/local/include

(6) Compile Fokko and atlas
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The command::

    make

(issued while you are in the atlasofliegroups directory where the Makefile is) should compile both Fokko and atlas.

If you get an error related to readline see `installing the readline
package <http://www.liegroups.org/software/download/readline.html>`.

If you get an error::

   ctanglex: Command not found

see :ref: `installing_cwebx`.

Compilation options: 
~~~~~~~~~~~~~~~~~~~~~~~

We recommend compiling with::

   make verbose=true optimize=true

Other possibilities are::

   debug=true
   readline=false.

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

Note that the messages (help) directory must be in the same directory as the Fokko executable. Alternatively you can run Fokko with the command::

   Fokko MESSAGEDIR

to specify where to find this directory.