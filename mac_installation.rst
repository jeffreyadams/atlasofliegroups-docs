.. _macs:

###
Mac
###

The two options, in order of preference, are:

* :ref:`compiling_from_source`
* :ref:`docker`
  
.. _compiling_from_source:

*********************************
Compiling the Sofware from Source
*********************************
  
.. _download:

There are a few extra steps required on a Mac versus linux.
First you need to install the XCode command line tools if you don't have these already.
Open a terminal, and type::

    xcode-select --install

Next, install the base Macports system: go to `<https://www.macports.org/install.php>`_
and follow the instructions there. Probably you just need step 3 (and possibly 2)
of the Quickstart.

Now install the readline library: in a terminal window type::

    sudo port install readline

You also need to install the software management tool git if you don't already have it.
If you are not familiar with gitt see 
:ref:`help_git`.

Open a terminal open a terminal and give the command ``git``.
If you get an error it is not installed. If not type::

    sudo port install git

Download the source code using git
==================================

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, then type::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git

This creates a subdirectory ``atlasofliegroups`` and stores the files there.

.. _compile:

Compile 
========

Next, you need to tell the compiler where to find read readline
libraries by setting the shell variable rl_libs.  The simplest method
is to edit the appropriate *dot* file in your *home directory*.
Your home directory is probably ``/Users/username``. You can also find 
it out by giving the command ``printenv`` and looking for the line ``HOME=``.

The name of this dot file varies, but usually is either .profile,
.zprofile, .zshrc or .cshrc. Do ``ls -a`` to see all of your files, and
look for one beginning with ``.``. In any event the command ``cd ~``
will take you there.

Add this line to the file::

    export rl_libs="-lreadline -lcurses -L/opt/local/lib"

If the file is .cshrc add this instead::

    setenv rl_libs "-lreadline -lcurses -L/opt/local/lib”

Then do ``source .profile`` (or whichever file you edited) to define the environment
variable rl_libs. You can check this with the command *printenv*, you should
see rl_libs in the output.

On a Mac there is an issue with the compiler finding the correct versions of the
readline files. To remedy this you need to have administrative privileges. Do::

    sudo cd /usr/local/include
    [type your password]
    sudo mkdir readline
    sudo chmod 755 readline
    sudo cp /opt/local/include/readline/* readline

If you don't already have a directory ``/usr/local/include`` you need an extra step::

    sudo cd /usr/local
    [type your password]
    sudo mkdir include
    sudo chmod 755 include
    sudo cd include
    sudo mkdir readline
    sudo chmod 755 readline
    sudo cp /opt/local/include/readline/* readline

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

The software has been well tested with g++/gcc versions 4.8 and above.

The most likely reason for an error has to do with
the readline library. The software will run without it. To
see if this is the problem give command::

    make readline=false

If this succeeds, you have a functioning version of the software, but without the
readline functions. 

.. _post_compile:

After compiling
===============

We recommend running::

      make install

(from the atlasofliegroups directory) to  make ``atlas`` accessible
from anywhere. By default this will put a shell script in ~/bin and
points to the atlas-scripts directory.  Make sure thath ~/bin is in
your path. To do this do::

echo $PATH

and look for something like ``Users/username/bin``. If it isn't there,
one solution is to add a line like this::

    set path = ( $PATH /Users/username/bin)

to the appropriate dot file in your home directory, usually
either .profile, .zprofile or .zshrc. Then quite the terminal
program and launch it again (or do ``source .profile`` (possibly with .profile replaced
by the file you edited); ~/bin should now be in your path.

Now the command ``atlas`` will run the software.


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
Also, if you encounter errors compiling you can try::

     make optimize=true  atlas

to compile atlas only (and not Fokko). 

See the Makefile for more options.

.. _updates:

Updating the atlas software
+++++++++++++++++++++++++++

At any time you can update the atlas software using git.
In the atlasofliegroups directory give the command::

     git pull origin master

Assuming you have not edited any of the files in the distribution this
will update the source code to the latest version. Typically you will
not need to run ``make`` again. This is the case if the only files that
changes (git reports this) are ``*.at`` files. If any files such as
``*.cpp`` files where changed, you should run ``make`` again.

If you get any errors due to conflicts you can try to resolve
them. This can sometimes be tricky. A fallback option is to reinstall
the software from scratch again.

.. _docker:

************
Using Docker
************

The preferred method is to :ref:`compile the software from source <compiling_from_source>`.
The next choice is using the Docker container system.

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

      docker run -it jeffreyadams/atlasofliegroups:version1.1

to download the software and run it (it launches atlas and reads in
the file all.at). The first time you do this it takes up to a few
minutes.  Subsequent times it is much faster.

Note: on the Mac (unlike linux) it should not be necessary to run docker as root
using sudo. If this is required, replace each occurence of ``docker`` with
``sudo docker``.

To get the latest update, give the command::

    docker pull jeffreyadams/atlasofliegroups:version1.1

.. _file_io_in_docker:

*******************************
File Input and Output in Docker
*******************************

Since docker runs in a container, some extra effort is required to make
files read/write from the host system. Here is an example,
assuming your username is ``joe_user``,  your home directory is ``/home/joe_user``,
and you want to work in a subdirectory ``my_files`` of your home directory::

 docker run -it --mount type=bind,source=/home/joe_user/my_files,\
 target=/atlasofliegroups/my_files jeffreyadams/atlasofliegroups:version1.1

(Note: the ``\`` indicates a new line, and no space is allowed after the comma.
On the mac you may need to enter this as a single line.) 

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
=====================

Here are a few other frequently used docker commands::

   docker images
   docker image ls

to list the images docker knows about. Similarly::

    docker container ls

to list the running containers (each container has a container
id). Occasionally you will need the container id, as in::

    docker container kill container_id

to kill a container that is running. This command::

    docker container prune

gets rid of containers that are no longer running
