.. _macports:

Compiling atlas for the Mac using MacPorts
==========================================

Regardless of how you download the source code you will need to
compile it.  Here is the preferred method.

You are going to install the gcc C compiler (provided by MacPorts),
which is preferred for installing Fokko and atlas. To do so you must
first install the XCode C Compiler.

(1) Install MacPorts. 
======================

(If MacPorts is installed on your system go to
step (2)). Visit `macports.org <https://www.macports.org>`, go to
`Installing MacPorts <https://www.macports.org/install.php>`, and
download the dmg file for your version of MAC OSX (for example
10.7.*=Lion). Double click on the dmg file to install MacPorts. You
need to be an administrative user, and will need to enter your
password.

(2) Install the XCode C compiler. 
==================================

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

Or, if you are using El Capitan(OS X 10.11) or later::

   Configured with: --prefix=/Library/Developer/CommandLineTools/usr
   --with-gxx-include-dir=/usr/include/c++/4.2.1

(3) Install the MacPorts (gcc) C Compiler
=========================================

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
=====================

Do::

   sudo port install readline

to install the readline package.

(5) Edit the Makefiles
=======================

You will need to edit two files to tell your computer which compiler to use.

(A) In the atlasofliegroups directory, edit the Makefile as follows:

First search for CXX and find the following text::

  # the compiler to use, including language switch 
  #some C++11 supportneeded (rvalue references, shared_ptr) but g++-4.4 suffices
  CXX = g++- -std=c++0x

Then edit the last line to read::
 
  CXX = g++-mp-4.9 -std=c++0x

(Remember to change 4.9 to the version of compiler that you have
downloaded).  

Also edit the line::

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

   CXX := g++-mp-4.9 -std=c++0x 

(again remember to change 4.9 to the correct compiler version).

(6) Compile Fokko and atlas
===========================

The simplest way to compile is with the command::

    make

(issued while you are in the atlasofliegroups directory where the
Makefile is). This should compile both Fokko and atlas.

If you get an error related to readline see
`installing the readline package: <http://www.liegroups.org/software/download/readline.html>`_

If you get an error::

   ctanglex: Command not found

see :ref:`installing_cwebx`.  If you get an error like the following::

   <assert.h> not found

then XCode may not be installed in exactly the right way. Try installing the command-line
utilities specifically as follows::

   xcode-select --install

Other Compilation options: 
~~~~~~~~~~~~~~~~~~~~~~~~~~~

For more complete compilation, we recommend compiling with::

   make verbose=true optimize=true

The option "verbose" makes Fokko print a little more information about what it is  doing, like printing a counter during a long Kazhdan-Lusztig computation. The option "optimize" tells the compiler to work hard to make the code as fast as possible; this takes slightly longer to compile, then runs maybe 10% faster. 

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
