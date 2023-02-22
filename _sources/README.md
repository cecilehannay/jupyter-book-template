## jupyter-book-template
This is template about to build and publish Jupyter books. 

## create a new repo on github
https://github.com/cecilehannay/jupyter-book-template

## clone the repo on cheyenne
``git clone git@github.com:cecilehannay/jupyter-book-template.git``

##  add the file ``_config.yml`` 
You can use the file  ``_config.yml`` as a tempalte. 
Make sure to edit ``title`` and ``url`` to reflect what this jupyter book will contains.
In my file it is set to:
```
title: Jupyter-book template
url: https://github.com/cecilehannay/jupyter-book-template 
```

## add the file ``_toc.yml``
You can use the file  ``_toc.yml`` as a template. 

## required packages
```
pip3 install --user jupyter-book
pip3 install --user ghp-import
```

## Build the book
```
module load npl
~/.local/bin/jupyter-book build .
```

## publish the notebook
```
~/.local/bin/ghp-import -n -p -f _build/html
```

## Where to look for the webpage
https://cecilehannay.github.io/jupyter-book-template

