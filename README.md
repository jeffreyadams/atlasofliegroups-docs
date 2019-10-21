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
Go to the atlas_documentation directory 
```
cd atlas_documentation
```
since we are trying to make a website, type: 
```
make html
```
Sphinx also supports many other output format including LaTex and plain text.
```
cd atlas_build/html
```

CORRECTION: cd ../atlasofliegroups-docs-gh-pages

You'll find all the automatically generated html files here. Open the index.html file with your browser, you can have a preview of the documentation website.

### To contribute

All the source files are the .rst files under atlas_documentation directory. You can edit them to add or modify content.

See http://www.sphinx-doc.org/en/stable/rest.html for a short introduction to reStructuredText syntax.

After you finished editing the .rst files, next step is to generate the html files. Under the source directory do: 
```
make html
```
All the newly generated html files will be stored in atlas_build/html. Open index.html to preview the website. 

CORRECTION: ../atlasofliegroups-docs-gh-pages

You can now push everything to the master branch.

If you want to also update the content on the website, you can push the content in atlas_build/html to the gh-pages branch.



