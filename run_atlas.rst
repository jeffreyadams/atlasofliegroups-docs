.. _run_atlas:

Run atlas
=========

This document will tell you how to start running atlas after you have done :ref:`download_and_install`. These instructions work best for the latest version.

Get atlas running
--------------------

Let's say you've compiled the software in a directory
atlasofliegroups.  Use your terminal to navigate into that
directory. It should contain the executable files Fokko and atlas, and
subdirectories "messages" (help files for Fokko) and "atlas-scripts"
(auxiliary and help files for atlas).

The minimal way to test that atlas is has been installed correctly
is to give the command::

    ./atlas

(depending on your environment the "./" might not be necessary).     

You should see see something like this:

    This is 'atlas' (version 1.0.9, axis language version 1.0),
    the Atlas of Lie Groups and Representations interpreter,
    compiled on Aug 17 2021 at 18:04:22.   http://www.liegroups.org/
    atlas>

Assuming this works go to the next section to load scripts.
    
Load scripts
------------

The folder atlas-scripts includes scripts, with names ending in ".at", the provide additional functionality.
The file ``all.at`` load all of the scripts and this is the recommended way to start atlas.

To launch atlas, and all scripts, give the command::

    ./atlas --path=atlas-scripts all

To test if the scripts are loaded do::

  atlas> set G=SL(2,R)
  Variable G: RealForm
  atlas> G
  Value: connected split real group with Lie algebra 'sl(2,R)'

You can also load scripts from within atlas::

    ./atlas --path=atlas-scripts
    <basic

loads the script basic.at, or::

    ./atlas --path=atlas-scripts
    <all

is the same as "./atlas--path=atlas-scripts all" (except that it
reports on what it is loading).

The symbol "<" means read a file. If this doesn't work, please see :ref:`trouble_shooting`. Also, there is a `video <https://www.youtube.com/watch?v=SU4fql8rOQg&feature=youtu.be>`_ explaining how to launch atlas so that it finds the necessary .at files.

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

