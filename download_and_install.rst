.. _download_and_install:

Download and Install
====================

This document will show you how to download and install atlas and Fokko on your machine.

Choose your operating system:

* :ref:`linux`
* :ref:`macs`
* :ref:`windows`


.. _linux:

Linux
-----

Download the software
~~~~~~~~~~~~~~~~~~~~~~

You have two options:

* :ref:`using_git` : recommended method if you are comfortable with git
* :ref:`using_link`

.. _using_git:

Using git
+++++++++

If you choose to use git, you can get the most up-to-date version of the software. Make sure your git client is relatively new. Version 1.7.0.4 and above should work. To check your git version, do::

    git --version

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, then type::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git
    
This creates a subdirectory "atlasofliegroups" and stores the files there.

.. _using_link:

Using provided links
++++++++++++++++++++

We recommend you to download the latest version.

+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| Latest atlas-scripts directory | `atlas-scripts.0.6.3.tgz`_           | supplementary files for atlas                                                                                                         |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| Latest complete version: 0.6   | `atlas_0.6.tgz`_                     | source code, Fokko and atlas                                                                                                          |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
|                                | `atlas_0.6_executables.tgz`_         | pre-compiled 64-bit binaries                                                                                                          |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| Verstion 0.5.9                 | `atlas_0.5.9.tgz`_                   | source code, atlas and realex                                                                                                         |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
|                                | `atlas_0.5.9_64bit_executables.tgz`_ | precompiled 64 bit binaries, atlas and realex, including messages and rx-scripts                                                      |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
|                                | `messages_and_rx-scripts0.5.9.tgz`_  | freestanding messages directory (help files for atlas)                                                                                |
|                                |                                      | and rx-scripts directory (scripts for realex, and also some realex help files).                                                       |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| Version 0.5.8                  | `atlas_0.5.8.tgz`_                   | source code, atlas and realex                                                                                                         |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
|                                | `atlas_0.5.8_32bit.executables.tgz`_ | precompiled 32 bit binaries, atlas and realex, including messages and rx-scripts                                                      |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
|                                | `messages_and_rx-scripts0.5.8.tgz`_  | freestanding messages directory (help files for atlas)and rx-scripts directory (scripts for realex, and also some realex help files). |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| Version 0.5.7                  | `atlas_0.5.7.tgz`_                   | source code, atlas and realex                                                                                                         |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
|                                | `atlas_0.5.7_32bit.executables.tgz`_ | precompiled 32 bit binaries, atlas and realex, including messages and rx-scripts                                                      |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
|                                | `atlas_0.5.7_64bit.executables.tgz`_ | precompiled 64 bit binaries, atlas and realex, including messages and rx-scripts                                                      |
+--------------------------------+--------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+

.. _atlas_0.6.tgz: http://www.liegroups.org/software/atlas_0.6/atlas_0.6.tgz
.. _atlas_0.6_executables.tgz: http://www.liegroups.org/software/atlas_0.6/atlas_0.6_executables.tgz
.. _atlas-scripts.0.6.3.tgz: http://www.liegroups.org/software/atlas_0.6/atlas_0.6.tgz
.. _atlas_0.5.9.tgz: http://www.liegroups.org/software/atlas_0.5.9.tgz
.. _atlas_0.5.9_64bit_executables.tgz: http://www.liegroups.org/software/atlas_0.5.9_64bit_executables.tgz
.. _messages_and_rx-scripts0.5.9.tgz: http://www.liegroups.org/software/atlas_0.5.9_messages_and_rx-scripts.tgz
.. _atlas_0.5.8.tgz: http://www.liegroups.org/software/atlas_0.5.8.tgz
.. _atlas_0.5.8_32bit.executables.tgz: http://www.liegroups.org/software/atlas_0.5.8_32bit.executables.tgz
.. _messages_and_rx-scripts0.5.8.tgz: http://www.liegroups.org/software/messages_and_rx-scripts.tgz
.. _atlas_0.5.7.tgz: http://www.liegroups.org/software/atlas_0.5.7.tgz
.. _atlas_0.5.7_32bit.executables.tgz: http://www.liegroups.org/software/atlas_0.5.7_32bit.executables.tgz
.. _atlas_0.5.7_64bit.executables.tgz: http://www.liegroups.org/software/atlas_0.5.7_64bit.executables.tgz

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



.. _macs:

Mac
---

This section is currently under construction. For instruction on how to download and install on a Mac machine, see `compiling atlas for Mac using MacPorts <http://www.liegroups.org/software/download/mac.html>`_.

.. _windows:

Windows
-------

Download
~~~~~~~~

We recommend you to download the latest version.

+--------------------------------+----------------------------+--------------------------------------------------------------------------------+
| Latest atlas-scripts directory | `atlas-scripts.0.6.3.tgz`_ | supplementary files for atlas                                                  |
+--------------------------------+----------------------------+--------------------------------------------------------------------------------+
| Latest complete version: 0.6   | `atlas_0.6_windows.tgz`_   | executables for Windows, Fokko and atlas, including messages and atlas-scripts |
+--------------------------------+----------------------------+--------------------------------------------------------------------------------+
| Verstion 0.5.9                 | `atlas_0.5.9.windows.zip`_ | executables for Windows, atlas and realex, including messages and rx-scripts   |
+--------------------------------+----------------------------+--------------------------------------------------------------------------------+

.. _atlas_0.6_windows.tgz: http://www.liegroups.org/software/atlas_0.6/atlas_0.6_windows.tgz
.. _atlas_0.5.9.windows.zip: http://www.liegroups.org/software/atlas_0.5.9.windows.zip

Installation
~~~~~~~~~~~~

Unzip the file you just downloaded, open atlas_windows/bin, double click on atlas.exe or Fokko.exe to run.

If for some reason, you choose to download the source files and would like to compile atlas, see `this page <http://www.liegroups.org/software/download/windows.html>`_ for instructions.
