# atlas Documentation Project
This is the sphinx source directory which stores the reStructuredText files. 

## Sphinx

Sphinx is a tool that makes it easy to create beautiful documentation. For more information see http://www.sphinx-doc.org/en/stable/index.html

It automatically generated webpages using .rst source files. Sphinx also supports inline math or display math.

**Install Sphinx**

Sphinx supports all three major operating systems. For details of how to install Sphinx on your machine, see http://www.sphinx-doc.org/en/stable/install.html

## How to use this repository

### Download and preview website

Under desired directory on your machine, do 
```
git clone https://github.com/cuiran/atlas_documentation.git
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
You'll find all the automatically generated html files here. Open the index.html file with your browser, you can have a preview of the documentation website.

### To contribute

All the source files are the .rst files under atlas_documentation directory.

See http://www.sphinx-doc.org/en/stable/rest.html for a short introduction to reStructuredText syntax.

