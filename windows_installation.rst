.. _windows:

Windows
---------

* :ref:`compiling` 
* :ref:`precompiled`

.. _compiling:

Compiling
+++++++++++

The best option is available on Windows 10. This is the
`bash shell
<https://msdn.microsoft.com/en-us/commandline/wsl/about>`_, which is
available (currently in beta version) in Windows 10. It provides a
linux command line environment. This was produced by Canonical, the
makers of Ubuntu, so it is very close to an Ubuntu linux environment. 

On older Windows machines linux software can be run using 
:ref:`cygwin`.
Unless you have already installed Cygwin and 
are familiar with it this is not recommended. 

Step-by-Step installation using the bash shell
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you haven't done so already, install the bash shell 
following the instructions from the Microsoft `bash shell <https://msdn.microsoft.com/en-us/commandline/wsl/about>`_ page.
We also recommend 
these instructions from `How-To Geek <http://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10>`_.

Open a bash window.

Install some necessary software. After the first call of sudo apt-get install you 
need to type your password. (Depending on how you installed the bash shell you
might not need to use sudo.)::

  sudo apt-get install git   
  sudo apt-get install make
  sudo apt-get install g++
  sudo apt-get install bison
  sudo apt-get install libreadline-dev
  sudo apt-get install emacs (or your favorite text editor)

The remainder of the process follows the standard linux process. See :ref:`linux` for details. Briefly:y to

Get a copy of the software using git::

  git clone http://github.com/jeffreyadams/atlasofliegroups.git
  
Go into the proper directory and type make::
   
   cd atlasofliegroups
   make

.. _cygwin:

Installing under Cygwin
+++++++++++++++++++++++++++

Download Cygwin. See
`the Cygwin web page <https://www.cygwin.com>`_. 

Install cygwin: Double-click on setup.exe to run it. At the package menu choose at least the following packages:


* gcc/g++ (version 4x)
* make
* bison
* libncurses-devel
* libstdc++6-devel
* readline
* git

Next, open a cygin terminal by double-clicking on the icon. You are now in a linux-like environment.

The remainder of the process follows the standard linux process, similar to the procedure under bash.
See :ref:`linux` for details.

.. _precompiled:

Pre-compiled
++++++++++++++++++





etc
~~~~~~~~~~~~

Unzip the file you just downloaded, open atlas_windows/bin, double click on atlas.exe or Fokko.exe to run.

If for some reason, you choose to download the source files and would like to compile atlas, see `this page <http://www.liegroups.org/software/download/windows.html>`_ for instructions.
