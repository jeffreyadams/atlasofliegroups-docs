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

If you choose to use git, you can get the most up-to-date version of the software. 

Choose a directory on your machine to store the source code. Use your terminal to navigate into that directory, type::

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

If you have downloaded the source code, either using git or the provided links, here is what you do: under the source code directory type::

    make

Ideally, this should get the source code compiled. If you encounter any error, see :ref:`trouble_shooting`


.. _macs:

Mac
---

.. _windows:

Windows
-------