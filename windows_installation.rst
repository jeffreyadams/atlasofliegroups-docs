.. _windows:

#######
Windows
#######

The two options, in order of preference, are:

* :ref:`docker`
* :ref:`compiling_from_source`

.. _docker:

************
Using Docker
************

This installs a *container*, which is a self-contained linux
environment (similar to a virtual machine) on your machine which is
called the *host*. The atlas software runs entirely in the container,
so is less dependent on the details of your system. This is a good
option of you have trouble compiling the software yourself.

This 
requires adminsitrative privileges, so is mainly used for personal
machines, and not institutional machines under the control of a system
administrator. Also since the software is running in a container
a little more effort is required for :ref:`file input and output<file_io_in_docker>`.

Install docker (community version) for your system from `<https://www.docker.com/community-edition>`_

Give the command::

      sudo docker run -it jeffreyadams/atlasofliegroups:version1.1

to download the software and run it (it launches atlas and reads in
the file all.at). docker needs to be run as roots, so all docker
commands are preceded by ``sudo``.  The first time you do this it
takes up to a few minutes.  Subsequent times it is much faster.

To get the latest update, give the command::

    sudo docker pull jeffreyadams/atlasofliegroups:version1.1

.. _file_io_in_docker:


File Input and Output in Docker
===============================

Since docker runs in a container, some extra effort is required to make
files read/write from the host system. On Windows this is compounded by
differences between the linux and windows filesystems. For now we don't
have explicit instructions to address this issue.

.. _other_docker

Other Docker Commands
=====================

Here are a few other frequently used docker commands::

   sudo docker images
   sudo docker image ls

to list the images docker knows about. Similarly::

    sudo docker container ls

to list the running containers (each container has a container
id). Occasionally you will need the container id, as in::

    sudo docker container kill container_id

to kill a container that is running. This command::

    sudo docker container prune

gets rid of containers that are no longer running.

.. _compiling_from_source:

*********************************
Compiling the Sofware from Source
*********************************

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

Once you installed the bash shell, open a bash window.

Now you may need to install some necessary software. After the first
call of sudo apt-get install you need to type your
password. (Depending on how you installed the bash shell you might not
need to use sudo.)::

  sudo apt-get install git
  sudo apt-get install make
  sudo apt-get install g++
  sudo apt-get install bison
  sudo apt-get install libreadline-dev
  sudo apt-get install emacs (or your favorite text editor)

.. _download:

Download the source code using git
==================================

For users who are not familiar with git, see :ref:`help_git`. git is a software management
tool, and is included by default on most linux distributions. 

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, then type::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git

This creates a subdirectory ``atlasofliegroups`` and stores the files there.

.. _compile:

Compile 
========

After you have the source code, cd to the atlasofliegroups directory.

Type::

    make

If all goes well you will have an executable file ``atlas``. Give the command::

    atlas

You should see something like::

    This is 'atlas' (version 1.1, axis language version 1.0),
    the Atlas of Lie Groups and Representations interpreter,
    compiled on Dec 30 2021 at 16:01:25.   http://www.liegroups.org/


Congratulations! Go on to :ref:`post_compile` for the next steps.

You may need to edit the Makefile to change the line ``CXX = g++ -std=c++0x`` to something 
different, depending on your system (this is specifying the C++ compiler). 

To find out your default compiler give the command::

    g++ --version

The software has been well tested with g++ versions 4.8 and above.

The most likely reason for an error has to do with
the readline library. The software will run without it. To
see if this is the problem give command::

    make readline=false

If this succeeds, you have a functioning version of the software, but without the
readline functions. See :ref:`installation_troubleshooting` for information
on compiling with readline and other issues.

.. _post_compile:

After compiling
===============

We recommend running::

      make install

(from the atlasofliegroups directory) to  make ``atlas`` accessible
from anywhere. By default this will put a shell script in ~/bin and
points to the atlas-scripts directory.  Make sure thath ~/bin is in
your path. Then the command ``atlas`` will run the software.


The software relies on a large set of auxiliary files in the directory
atlasofliegroups/atlas-scripts, with the suffix .at (or
.ax). Generally you want to load all of these, by loading the single
file ``all.at``. This happens automatically if you use ``make install``.

See the Makefile for other options.

.. _other_launches

Other ways of launching atlas
=============================

Alternatively you can launch atlas and tell it where to find the scripts.
Here are few examples.


We recommend creating a directory ``atlasofliegroups/my_files``, and always starting
atlas from there. Assuming you've run ``make install`, you can do::

    cd atlasofliegroups
    mkdir my_files
    cd my_files
    atlas

This will read the necessary files from the directory atlasofliegroups/atlas-scripts, and any files
you write to will be in atlasofliegroups/my_files.
Another possibility (which doesn't require ``make install`` is::

    cd atlasofliegroups
    mkdir my_files
    cd my_files
    ../atlas --path=../atlas-scripts all.at

Alternatively go to thedirectory in which you built the software and run atlas from there::

  cd atlasofliegroups
  ./atlas --path=atlas-scripts all.at

The path argument tells atlas where to find the scripts, and ``all.at``
says to load most of the scripts (possibly excluding a few which are under
development).

Another option is to run atlas from the atlas-scripts directory, in which
case it doesn't need the path::

    cd atlasofliegroups/atlas-scripts
    ../atlas all.at
  

The compiler also produces an executable file ``Fokko'' which has the core software
but not the scripting language. 

.. _file_io:

File Input and Output
=====================

When you read files from within atlas it looks in the working directory (from which you launched atlas)
and the atlas-scripts directory, or whatever directory (or directories) you speficy with ``--path``. 

When the atlas software writes output to a file, it is always in the working directory.

Assuming you ran ``make install`` as above you don't need to do anything else. Files will be
read from the working directory (from which you launched atlas) and the atlas-scripts directory. Output will go to
files in the working directory.

.. _other_compile_options

Other Compile Options
+++++++++++++++++++++

When you compile the software by running ``make``, there are some other options available.
Among these::

     make optimize=true

is recommended: the compilation is slower, but the code runs substantially faster.

See the Makefile for more options.
