.. _run_atlas:

Run atlas
=========

This document will tell you how to start running atlas after you have done :ref:`download_and_install`. These instruction works the best for the latest version.

Get atlas running
--------------------

Let's say you compiled the software in a directory atlasofliegroup, or perhaps you put a pre-compiled binary there. Use your terminal to navigate into that directory. You should end up in a directory that contains the excecutable files Fokko and atlas, and subdirectories messages (help files for Fokko) and atlas-scripts (auxiliary and help files for atlas).

Once you are there, depending on your setting, do either::

    ./atlas --path=atlas-scripts

or::

    atlas --path=atlas-scripts

You should then see something like this::

    This is 'atlas' (version 0.6, axis language version 0.9),
    the Atlas of Lie Groups and Representations interpreter,
    compiled on Jan 19 2016 at 02:21:55.   http://www.liegroups.org/
    atlas> 
    
Alternatively, you can cd into the atlas-scripts folder, then do::

    ../atlas
    
Load scripts
------------

Assuming you are in the atlas environment (when you see ``atlas>`` in your terminal), you should now load some scripts. For example, to load the file "basic.at" do::

    atlas> <basic
    
You will see atlas output::

    Starting to read from file 'atlas-scripts//basic.at'.
    Added definition [12] of #: (int->[int])
    Added definition [13] of #: (bool->int)
    ...
    
The symbol "<" means read a file. If this doesn't work, please see :ref:`trouble_shooting`. Also, there is a `video <https://www.youtube.com/watch?v=SU4fql8rOQg&feature=youtu.be>`_ explaining how to launch atlas so that it finds the necessary .at files.

Once this is working, you can and should load other files. Load all.at to get a recommended set of files::

    atlas> <all
    [... some atlas output ...]
    atlas>
    
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

Congratulations! Now you have atlas working on your machine! Proceed to :ref:`simple_commands` for some examples of what you can do with atlas.

Quit atlas
----------

Just type ``quit`` :)

