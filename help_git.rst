.. _help_git:

Help with git
=============

`git <https://git-scm.com/>`_ is a distributed version control system. It helps developers handle their projects. Git is easy to learn. It is also free and open source. One advantage of using ``git`` is that the latest version of the software is always there 


This page is organized into the following sections:

* :ref:`primary_commands`
* :ref:`branch`
* :ref:`other_commands`
* :ref:`unstuck`
* :ref:`more_git`
* :ref:`tagging_and_branches`
* :ref:`other_refs`


.. _primary_commands:

Primary commands
----------------

To download the software, do::

    git clone https://github.com/jeffreyadams/atlasofliegroups.git
    

Once you have done git clone, most other commands operate locally. Everything is done from within the atlasofliegroups directory, using meta-information in the .git subdirectory. 

To update the software, do::

    git pull origin
    
will update your local copy of the software with the any latest changes.


.. _branch:

Branches
--------

There are several branches (versions) of the atlas code. The main branch is named master. Most users never need any other branch. After you have done ``git clone`` you can cd into the newly downloaded directory and do::

    git branch
    
This will show you which branch you are on (the default is master). To generate a list of all remote branches, do::

    git branch -r
    
The primary branches are master, unitary, and latest. The The master branch is probably what most users would want. If you choose to download a specific branch, say the branch with name "unitary", you can do::

    git clone -b unitary --single-branch https://github.com/jeffreyadams/atlasofliegroups.git

To switch into other branches from the current branch, do::

    git checkout latest
    
This will switch you into the branch named "latest".


.. _other_commands:

Other helpful commands
-----------------------

Again, after you have done `git clone`, most of these commands operate locally. Use you terminal to navigate into "atlasofliegroups" directory.

To show the status of your local repository, compared to the remote one, do::

    git status
    
To show a lot of information about the repository, including recent activities, do::


    git log
    git log --oneline
    
The ``--oneline`` option gives you a more succinct output.

To launch a graphical git browser, do::

    gitk
    
However, you need to have `gitk <https://git-scm.com/docs/gitk>`_ installed.

Many commands of git have help options::

    git # This gives short git help.  git --help # This gives longer git help. 
    git tag --help # This gives help on tagging.  
    git pull origin # This downloads objects from the origin repository (stored
on GitHub )and integrates witn another repository or local branch.
    git pull origin master # This downloads the latest version from the master branch where the software is.
    
Some commands have dry-run versions::

    git pull origin --dry-run

says what the command will do, but doesn't do anything. 



.. _unstuck:

Getting unstuck
-----------------

If all you ever do is pull code, from a single branch, hopefully you won't run in to trouble.
Suppose this happens::

    git pull origin master
    file test.rx not up to date, cannot merge

and the update from google will not execute (at all). Do this::

    git stash
    git pull origin master

to stash your local changes, and execute the update from google. The do::

    git stash pop

to bring back your modified files. There are other variants of git stash, see the references.

If you are not making changes to the code, but have a problem, it is always easy to start from scratch. Delete your current directory (don't forget to delete the invisible .git directory), or start a new directory, and start over with a fresh git clone.


.. _more_git:

More on git objects
--------------------

This is a quick overview. See The `Git Objects <https://git-scm.com/book/en/v2/Git-Internals-Git-Objects>`_ for more detail. The main git object is a commit.

A commit contains a tree, which is a snapshot of a directory, together with some meta-information. 
Here are some commands for working with git objects::

    git log 
    git log --oneline    # This shows list of commits
    
The output is something like::

    4826100 ...
    94a5663 ...
    268f5d4 ...
    
You can refer to each commit by the first few letters of the hex name. For example::

    git show 94a5   # This will show you details about the second commit



.. _tagging_and_branches:

Tagging and branches
--------------------

Tags are (mainly) a way to give user-friendly names to commits::

    git tag    # Print list of tags 
    git tag -n    # Print list of tags with more information

Here is how I created the version_0_4_6 tag::

    git log --oneline
    b1c0fdd Updated version to 0.4.6 in version.h
    bbca5d3 deleted README-git
    bb64257 edited README-git
    ...
    git tag version_0_4_6 b1c0f 
    git push --tags    # To make the changes on the server



.. _other_refs:

Git references
---------------

* `The main git site <https://git-scm.com/documentation>`_
* `Git reference <http://gitref.org/creating/>`_
* `Some handy git tips <http://mislav.net/2010/07/git-tips/>`_
* `Git and Google code <http://google-opensource.blogspot.com/2008/05/develop-with-git-on-google-code-project.html>`_

The O'Reilly book `Version Control with Git <http://www.foo.be/cours/dess-20122013/b/OReilly%20Version%20Control%20with%20GIT.pdf>`_, by John Loeliger is quite useful.

There is a lot of browsing you can do at the `Atlas page at github <https://github.com/jeffreyadams/atlasofliegroups>`_, including looking at different branches and tags.





















