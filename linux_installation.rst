.. _linux:

Linux
-----

Download the software
~~~~~~~~~~~~~~~~~~~~~~

You have two options:

* :ref:`using_git` : recommended method.
* :ref:`direct`

.. _using_git:

Using git
+++++++++

For users who are not familiar with git, see :ref:`help_git` to get started with git.

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, then type::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git
    
This creates a subdirectory "atlasofliegroups" and stores the files there.

.. _direct:

Download the source code directly
+++++++++++++++++++++++++++++++++

You can download an archive of the source code. These are typically not as up-to-date as
the git version. 

+--------------------------------+------------------------------+-------------------------------------+
| Latest atlas-scripts directory |       `atlas_0.8.tgz`_       | source code, Fokko and atlas        |
+--------------------------------+------------------------------+-------------------------------------+

.. _atlas_0.8.tgz: http://www.liegroups.org/software/atlas_0.8.tgz

Installation
~~~~~~~~~~~~

**Source code**

Assuming you have downloaded the source code, either using git or the provided links, here is what you do: under the source code directory type::

    make

You can choose turn on the verbose option by typing::

    make verbose=true

This will show you the details of the commands your compiler is using to compile and link the codes.

Ideally, this should get the source code compiled. If you encounter any error, see :ref:`installation_troubleshooting`.

**Executables**

Assuming you have downloaded the executables from the provided links, after you unzip the files you are pretty much good to go. Proceed to :ref:`run_atlas`.

If you want to create `symlinks <https://en.wikipedia.org/wiki/Symbolic_link>`_ for atlas, you can do::

    make install INSTALLDIR = [installation directory] BINDIR = [desired symlinks directory]
   
For example, if you want to install the executables in /home/userid/software/atlas, and symlinks in /home/userid/bin, type::

    make install INSTALLDIR=/home/userid/software BINDIR=/home/userid/bin
    
.. note:: If you have downloaded the messages (help) files, it is recommended that you put it in the same directory as the atlas executables.
