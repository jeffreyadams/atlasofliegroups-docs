.. _windows:

Windows
-------

You have three options:

* :ref:`compiling` : recommended method.
* :ref:`precompiled`

.. _compiling:

Compiling
+++++++++

The best option is available on Windows 10. This is the 

`bash shell
<https://msdn.microsoft.com/en-us/commandline/wsl/about>`_, which is
available (currently in beta version) in Windows 10. It provides a
linux command line environment. This was produced by Canonical, the
makers of Ubuntu, so it is very close to an Ubuntu linux environment. 

On older Windows machines linux software can be run using 
`Cygwin <https://www.cygwin.com/>_`. Unless you have already installed Cygwin and 
are familiar with it this is not recommended. 

Step-by-Step installation using the bash shell
~~~~~~~~~~~~

If you haven't done so already, install the bash shell 
following the instructions from the Microsoft `bash shell <https://msdn.microsoft.com/en-us/commandline/wsl/about>`_ page.
We also recommend 
these instructions from `How-To Geek <http://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10>`_.

Open a bash window.

Install some necessary software:::

  apt-get install git
  apt-get install make
  apt-get install g++
  apt-get install bison
  apt-get install libreadline-dev
  apt-get install emacs (or your favorite text editor)

The remainder of the process follows the standard linux process. See :ref:`linux` for details.

Get a copy of the software using git:::

  git clone http://github.com/jeffreyadams/atlasofliegroups.git
  
Go into the proper directory and type make:::
   
   cd atlasofliegroups
   make

.. _precompiled:

Pre-compiled
+++++++++

etc


~~~~~~~~~~~~

Unzip the file you just downloaded, open atlas_windows/bin, double click on atlas.exe or Fokko.exe to run.

If for some reason, you choose to download the source files and would like to compile atlas, see `this page <http://www.liegroups.org/software/download/windows.html>`_ for instructions.
