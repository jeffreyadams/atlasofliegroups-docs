.. _windows:

#######
Windows
#######

Ways to download and install the s oftware
=========================================

The options, in order of preference, are:


* :ref:`docker_windows`
* :ref:`compile_windows`
.. _docker_windows:

Using Docker
============

The simplest method is using Docker.

This installs a *container*, which is a self-contained linux
environment (similar to a virtual machine) and runs the software in
the container. This is less dependent on the details of your system,
and is a good option of you have trouble compiling the software
yourself. It requires adminsitrative privileges, so is mainly used for
personal machines, and not instutional machines under the control of a
system administrator.
The Docker web site is `docker.com <https://www.docker.com>`_


Install docker (community version) for your system from `<https://www.docker.com/community-edition>`_
Double click on the file to install it. This requires typing your password.

Open a command window and give the command

      docker run -it jeffreyadams/atlasofliegroups

to download the software and run it (it launches atlas and read in the
fill all.at). The first time you do this it takes up
to a few minutes.  Subsequent times it is much faster.

To get the latest update, give the command

    docker pull jeffreyadams/atlasofliegroups



.. _compile_windows:

Compiling
=========

The best compilation option is available on Windows 10 and 11. This is the
`bash shell
<https://msdn.microsoft.com/en-us/commandline/wsl/about>`_, which is
available in Windows 10 and 11. It provides a
linux command line environment. This was produced by Canonical, the
makers of Ubuntu, so it is very close to an Ubuntu linux environment. 

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

The remainder of the process follows the standard linux process. See :ref:`linux` for details. 

