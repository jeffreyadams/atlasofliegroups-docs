
.. _linux:

#################################################
Downloading and Installing in Linux (and Solaris)
#################################################

These instructions apply to most Linux distributions. They 
apply to Solaris with little or no change.

The two options, in order of preference, are:

* :ref:`compile`
* :ref:`docker`

.. _compile:

*********************************
Compiling the Sofware from Source
*********************************
  
.. _download:

Download the source code using git
==================================

For users who are not familiar with git, see :ref:`help_git`. git is a software management
tool, and is included by default on most linux distributions. 

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, then type::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git

This creates a subdirectory ``atlasofliegroups`` and stores the files there.

.. _compile:

Compiling from source
=====================

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

Ideally, this should compile the code and produce the file 
``atlas``. The most likely reason for an error has to do with
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

(from the atlasofliegroups directory) to put make ``atlas`` accessible
from anywhere. By default this will put a shell script in ~/bin and
points to the atlas-scripts directory.  Make sure thath ~/bin is in
your path. Then the command ``atlas`` will run the software.


The software relies on a large set of auxiliary files in the directory
atlasofliegroups/atlas-scripts, with the suffix .at (or
.ax). Generally you want to load all of these, by loading the single
file ``all.at``. This happens automatically if you use ``make install``.

.. _other_launches

Other ways of launching atlas
=============================

Alternatively you can launch atlas and tell it where to find the scripts.
Here are few examples.


For example we recommend creating a directory ``atlasofliegroups/my_files``, and always starting
atlas from there. Assuming you've run ``make install`, you can do::

    mkdir my_files
    cd my_files
    atlas

This will read the necessary files from the directory atlasofliegroups/atlas-scripts, and any files
you write to will be in atlasofliegroups/my_files.
Another possibility (which doesn't require ``make install`` is::

    mkdir my_files
    cd my_files
    ../atlas --path=../atlas-scripts all.at










Alternatively, in the directory in which you built the software you
can execute::

  ./atlas --path=atlas-scripts all.at

The path argument tells atlas where to find the scripts, and ``all.at``
says to load most of the scripts (possibly excluding a few which are under
development).

The compiler also produces an executable file ``Fokko'' which has the core software
but not the scripting language. 

See the Makefile for other options.

.. _file_io

File Input and Output
+++++++++++++++++++++

When you read files from within atlas it looks in the working directory (from which you launched atlas)
and the atlas-scripts directory (or whatever directory you speficy with ``--path``). 

Whe the atlas software writes output to a file, it is always in the working directory.


Assuming you ran ``make install`` as above you don't need to do anything else. Files will be
read from the working directory (from which you launched atlas) and the atlas-scripts directory. Output will go to
files in the working directory.


.. _docker:

************
Using Docker
************

The preferred method is to :ref:`compile the software from source <compile>`.
The next choice is using the Docker container system.

This installs a *container*, which is a self-contained linux
environment (similar to a virtual machine) and runs the software in
the container. This is less dependent on the details of your system,
and is a good option of you have trouble compiling the software
yourself. It requires adminsitrative privileges, so is mainly used for
personal machines, and not institutional machines under the control of a
system administrator.


Install docker (community version) for your system from `<https://www.docker.com/community-edition>`_

Give the command::

      sudo docker run -it jeffreyadams/atlasofliegroups

to download the software and run it (it launches atlas and reads in
the file all.at). docker needs to be run as roots, so all docker
commands are preceded by ``sudo``.  The first time you do this it
takes up to a few minutes.  Subsequent times it is much faster.

To get the latest update, give the command::

    sudo docker pull jeffreyadams/atlasofliegroups

.. _file_io

File Input and Output in Docker
+++++++++++++++++++++++++++++++

Since docker runs in a container, some extra effort is required to make
files read/write from the host system. Here is an example,
assuming your username is ``joe_user``,  your home directory is ``/home/joe_user``,
and you want to work in a subdirectory ``my_files`` of your home directory::

 sudo docker run --mount type=bind,source=/home/joe_user/my_files,\
 target=/atlasofliegroups/my_files jeffreyadams/atlasofliegroups:master

Now atlas will run as usual. Any files you write using atlas will be visible
from the host system in the ``my_files`` directory. You can add files
to this directory from the host filesystem, and ``atlas`` can read them.

Since docker is running as root, any files that atlas creates (which you
can see in youor my_files directory) are owned by root. They are readable,
but you must be root to write to them. You can copy any file to another
file, in which case the new file will be readable/writable by you,
and visible to atlas.

.. _other_docker

Other Docker Commands
+++++++++++++++++++++++++++++++

Here are a few other frequently used docker commands::

   sudo docker images
   sudo docker image ls

to list the images docker knows about,::

    sudo docker container ls

to list the running containers (each container has a container
id). Normally a container will die when it is not longer being used::

    sudo docker container kill container_id

to kill a container that is running, and::

    sudo docker container prune

to get rid of containers that are no longer running.












