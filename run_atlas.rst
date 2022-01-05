.. _run_atlas:

Run atlas
=========

This document will tell you how to start running atlas after you have done :ref:`download_and_install`.

This video on `running the atlas software <https://www.youtube.com/watch?v=SU4fql8rOQg&feature=youtu.be>`_ covers some of the same
material in this section.

Get atlas running
--------------------

Let's say you've compiled the software in a directory
atlasofliegroups.  Use your terminal to navigate into that
directory. It should contain the executable file atlas.
To see this do::

    file atlas

and you should see something like (of course details will differ)::

      atlas: ELF 64-bit LSB shared object, x86-64, version 1 (GNU/Linux), dynamically linked,
      interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=db51b2603a2949cfa75646963f81c18343dfb993,
      for GNU/Linux 3.2.0, not stripped

The minimal way to test that atlas is has been installed correctly
is to give the command::

    ./atlas

(depending on your environment the ``./`` might not be necessary).     

You should see see something like this::

    This is 'atlas' (version 1.1, axis language version 1.0),
    the Atlas of Lie Groups and Representations interpreter,
    compiled on Dec 30 2021 at 16:01:25.   http://www.liegroups.org/
    atlas>

Assuming this works go to the next section to load scripts.

Load scripts
------------

The software relies on a large set of auxiliary files in the directory
atlasofliegroups/atlas-scripts, with the suffix .at (or
.ax). Generally you want to load all of these, by loading the single
file ``all.at``.

Assuming you've run ``make install`` (see :ref:`post_compile`)
then the command ``atlas`` will run the software, and
load ``all.at``, and therefore load all of the scripts.

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

To test if the scripts are loaded do::

  atlas> set G=SL(2,R)

and you should see::
  
  Variable G: RealForm
  atlas> G
  Value: connected split real group with Lie algebra 'sl(2,R)'

You can also load scripts from within atlas, for example::

    ./atlas --path=atlas-scripts
    <basic.at


The symbol "<" means read a file.

To check if readline (command completion, recalling previous commands, etc.) is working, hit **TAB** on your keyboard twice. You should see something like::

    atlas> 
    Display all 902 possibilities? (y or n)
    
This indicates that command completion is working. Now do a few simple commands::

    atlas> 1+1
    Value: 2
    atlas> set G=SL(2,R)
    Identifier G: RealForm
    atlas> print_block(trivial (G))
    Parameter defines element 2 of the following block:
    0:  0  [i1]  1   (2,*)  *(x=0,lam=rho+  [0], nu=  [0]/1)  e
    1:  0  [i1]  0   (2,*)  *(x=1,lam=rho+  [0], nu=  [0]/1)  e
    2:  1  [r1]  2   (0,1)  *(x=2,lam=rho+  [0], nu=  [1]/1)  1^e

Congratulations! Now you have atlas working on your machine! Proceed to :ref:`tutorial_with_examples` for some examples of what you can do with atlas.

Quit atlas
----------

Just type ``quit`` :)

