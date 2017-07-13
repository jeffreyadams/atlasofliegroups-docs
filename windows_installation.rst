.. _windows:

#######
Windows
#######

Ways to download and install the software
=========================================

The options, in order of preference, are:

* :ref:`compile_windows`
* :ref:`docker_windows`
* :ref:`executable_windows`

.. _compile_windows:

Compiling
=========

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

The remainder of the process follows the standard linux process. See :ref:`linux` for details. Briefly:

Download the source code:

+--------------------------+------------------------------+---------------------------------------+
| Version 1.0.5            |   `atlas_1.0.5.tgz`_         | source code for Fokko and atlas       |
|                          |                              | including messages and atlas-scripts  |
+--------------------------+------------------------------+---------------------------------------+

.. _atlas_1.0.5.tgz: http://www.liegroups.org/software/source/1.0.5/atlas_1.0.5.tgz

Unpack the file::

   tar xvf atlas_1.0.5.tgz
  
Go into the proper directory and type make::
   
   cd atlasofliegroups
   make

Follow the instructions in :ref:`linux`.

.. _cygwin:

Installing under Cygwin
++++++++++++++++++++++++

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

Next, open a cygwin terminal by double-clicking on the icon. You are now in a linux-like environment.

The remainder of the process follows the standard linux process, similar to the procedure under bash.
See :ref:`linux` for details.

.. _docker_windows:

Using Docker
============

The preferred method is to :ref:`compile the software from source <compile_windows>`.

The next choice is using `the Docker container system <https://www.docker.com>`_.

This installs a *container*, which is a self-contained linux
environment (similar to a virtual machine) and runs the software in
the container. This is less dependent on the details of your system,
and is a good option of you have trouble compiling the software
yourself. It requires adminsitrative privileges, so is mainly used for
personal machines, and not instutional machines under the control of a
system administrator.


Install docker (community version) for your system from `<https://www.docker.com/community-edition>`_
Double click on the file to install it. This requires typing your password.

Open a command window and give the command

      docker run -it jeffreyadams/atlasofliegroups

to download the software and run it (it launches atlas and read in the
fill all.at). The first time you do this it takes up
to a few minutes.  Subsequent times it is much faster.

To get the latest update, give the command

    docker pull jeffreyadams/atlasofliegroups

.. _executable_windows:

Download and Install an executable
==================================

The best method is to compile from source. As a backup option you can 
download and install an executable file. 

Download a copy of the executable, and the atlas-scripts directory here:

+-------------------------------+--------------------------------+-------------------------------------+
| Windows compiled              | `atlas_windows_pre_1.0.tar`_   |  executable, and messages           |
|                               |                                |  atlas-scripts directories          |
+-------------------------------+--------------------------------+-------------------------------------+

.. _atlas_windows_pre_1.0.tar: http://www.liegroups.org/software/source/1.0/atlas_windows_pre_1.0.tar

Double click on the file and extract the software. This will create a folder 
atlas_windows_pre_1.0. Double click on the folder, and then on the atlas icon. Then do


      <all

to load the scripts.

Note: using this option readline (command line tools) will not work. For this reason 
this is the least desirable option.

