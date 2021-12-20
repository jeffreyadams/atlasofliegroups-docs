.. _macs:

###
Mac
###

Ways to download and install the software
*****************************************

The options, in order of preference, are:

* :ref:`docker`
* :ref:`compile_mac`

.. _docker:

Using Docker
============

Docker is the preferred installation method on a Mac.

Docker installs the software in a *container*, which is a self-contained linux
environment (similar to a virtual machine) and runs the software in
the container. This is less dependent on the details of your system,
and is a good option of you have trouble compiling the software
yourself. It requires adminsitrative privileges, so is mainly used for
personal machines, and not instutional machines under the control of a
system administrator.


Install docker (community version) for your system from `<https://www.docker.com/community-edition>`_
Double click on the dmg file to install it. This requires typing your password.

Open a terminal window and give the command

      docker run -it jeffreyadams/atlasofliegroups

to download the software and run it (it launches atlas and read in the
fill all.at). The first time you do this it takes up
to a few minutes.  Subsequent times it is much faster.

To get the latest update, give the command

    docker pull jeffreyadams/atlasofliegroups


.. _compile_mac:

Download and compile the source code
================================================

First you need to install the XCode command line tools if you don't have these already.
Open a terminal, and type::

    xcode-select --install

Next, install the base Macports system: go to `https://www.macports.org/install.php`_

Now install the readline library: in a terminal window type::

    sudo port install readline

Finally you need to tell the compiler where to find read readline libraries by setting
the shell variable rl_libs.

The simplest method is to edit your .cshrc file, and add the line::

    setenv rl_libs "-lreadline.8 -lcurses  -L/opt/local/lib"

.. _using_git_Mac:

Download the source code using git
++++++++++++++++++++++++++++++++++

For users who are not familiar with git, see :ref:`help_git`.

If you choose to use git, you can get the most up-to-date version of
the software. Open a terminal window (in the Finder click
Macintosh/Applications/Utilities/Terminal).

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, then type::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git
    
This creates a subdirectory "atlasofliegroups" and stores the files there.


Compiling from source
************************

Follow the instructions at :ref:`compile` to compile and run the atlas software.


