# atlas Documentation Project
This is the sphinx source directory which stores the reStructuredText files. 

The documentation website url is: https://jeffreyadams.github.io/atlasofliegroups-docs

## Sphinx

Sphinx is a tool that makes it easy to create beautiful documentation. For more information see http://www.sphinx-doc.org/en/stable/index.html

It automatically generates webpages using .rst source files. Sphinx also supports inline math or display math.

**Install Sphinx**

Sphinx supports all three major operating systems. For details of how to install Sphinx on your machine, see http://www.sphinx-doc.org/en/stable/install.html

**Mac installation**

This assumes you use MacPorts. If you have
```
pip
```
installed already, then there are simple instructions at http://www.sphinx-doc.org/en/stable/install.html

As for any MacPorts installation, type"
```
sudo port install py27-sphinx
```
There are likely to be many dependencies involved (for example, mysql) so this may take a long time (even an hour or longer?). You don't need to do anything, so overnight is a good possibility. After the installation is complete, type
```
sudo port select --set python python27
sudo port select --set sphinx py27-sphinx
sudo port install py-sphinx_rtd_theme
```
You can test this in a NEW terminal window (the one you've been using doesn't know about the commands you just installed) by typing
```
which sphinx-quickstart
```

## How to use this repository

### Download and preview website

Under desired directory on your machine, do 
```
git clone https://github.com/jeffreyadams/atlasofliegroups-docs.git
```	
Go to the atlasofliegroups-docs directory 
```
cd atlasofliegroups-docs
```
Use the the following command to generate html files from the rst files: 
```
make html
```
Sidenote: Sphinx also supports many other output format including LaTex and plain text.

Go to the parant folder and you'll see a new folder was generated: 
```
cd ../atlasofliegroups-docs-gh-pages
```
You'll find all the automatically generated html files here. Open the index.html file with your browser, you can have a preview of the documentation website.

### To contribute

All the source files are the .rst files under atlasofliegroups-docs directory. You can edit them to add or modify content.

See http://www.sphinx-doc.org/en/stable/rest.html for a short introduction to reStructuredText syntax.

After you finished editing the .rst files, next step is to generate the html files. Under the source directory do: 
```
make html
```
All the newly generated html files will be stored in atlasofliegroups-docs-gh-pages. Open index.html to preview the website. 

You can now push the source files (namely the .rst files) to the master branch
```
cd atlasofliegroups-docs
git add $FILE
git commit $SOMETEXT
git push origin master
```
and all the html files to the gh-pages branch
```
cd atlasofliegroups-docs-gh-pages
git add --all
git commit -m $SOMETEXT
git push origin gh-pages
```



-------------------------------------------------------------------
12/20/2021

Instructions on editing the documentation site

edit rst pages in this directory
run sphinx-build, something like this is recommended (to update a single or small number of pages):

sphinx-build  -b html -d ../atlasofliegroups-docs-gh-pages/doctrees   . ../atlasofliegroups-docs-gh-pages linux_installation.rst

cd to ../atlasofliegroups-docs-gh-pages

git add (changes files)
git commit
git push origin gh-pages

to push the html pages to github

You can view these changes in a browser by goingi to the local file ../atlasofliegroups-docs-gh-pages/index.html

then on the atlas server, in

/var/www/html/software/documentation/atlasofliegroups-docs#

do git pull gh-pages
