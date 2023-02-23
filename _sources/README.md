
# Welcome to my jupyter book template 
[![Commits](https://img.shields.io/github/last-commit/cecilehannay/jupyter-book-template?label=Last%20commit&style=flat-square&color=green)](https://github.com/cecilehannay/jupyter-book-template/commits/main) 

**Created by Cecile Hannay**

The present gitbub repository is a simple template to create Jupyter books. 
- The github repository [![here](https://github.com/favicon.ico)](https://github.com/cecilehannay/jupyter-book-template) for this template is available [here](https://github.com/cecilehannay/jupyter-book-template)
- The materials and notebooks in this template is published [here](https://cecilehannay.github.io/jupyter-book-template/README.html) as a Jupyter book  [![Jupyter Book Badge](https://jupyterbook.org/badge.svg)](https://cecilehannay.github.io/jupyter-book-template/README.html)



## Getting set up

### Create a remote repository

Create a new repository on GitHub.com. To avoid errors, do not initialize the new repository with README, license, or gitignore files. 

![image](https://user-images.githubusercontent.com/9723220/220764777-9f8541d2-7338-4ba5-afc5-6ed677a46d1f.png)

In the example below, I am creating a repo called:
```
https://github.com/cecilehannay/new-jupyter-book
```

### Clone the template repository

Next, clone the jupyter-book-template repository to your local directory:
```
git clone https://github.com/cecilehannay/jupyter-book-template
```

### Switch to the remote repository you created

Cloning will bring over the remotes specified in that directory. The new step is to switch to the remote repository just created. 

This can be done in two steps:
```
git remote remove origin
git remote add origin  https://github.com/cecilehannay/new-jupyter-book

```
Or in a single step:
```
git remote set-url origin https://github.com/cecilehannay/new-jupyter-book
```

### Push the template into the new repo
You will also want to --set-upstream-to, or -u to tell git this is the remote repository this branch will update to, presuming you are on the main (or default) branch.

```
git branch -M main
git push -u origin main
```

## Anatomy of the template

The template contains:
- a collection of jupyter notebooks in the directory ``notebooks``
- a file ``_config.yml`` 
- a file ``_toc.yml``


###  The file ``_config.yml`` 
You can configure the Jupyter Book with the file ``_config.yml``. This file controls a number of options and feature flags.

You can use the file  ``_config.yml`` as a template. Make sure to edit ``title`` and ``url`` to reflect what this jupyter book will contains.
In my file it is set to:

```
title: Jupyter-book template
url: https://github.com/cecilehannay/jupyter-book-template 
```

### the file ``_toc.yml``
Te book's structure is determined by a Table of Contents. This is a file called ``_toc.yml`` that defines a structure that Jupyter Book uses to create the order and nesting of pages.

```
format: jb-book
root: index
chapters:
- file: path/to/chapter1
- file: path/to/chapter2
```

You can use the file  ``_toc.yml`` as a template. This are many ways to customize the file ``_toc.yml``. See documentation here https://jupyterbook.org/en/stable/structure/toc.html



### Notebooks

Finally, open the notebooks and interact with them. When you are happy with your notebook, follow your usual workflow to push them on the remote repo.

```
git status
git add --all
git commit -m "new build"
git push -u origin main
```

To connect to NCAR JupyterHub on cheyenne, please open this link in a web browser: https://jupyterhub.hpc.ucar.edu/


## Building and publising the notebook

### Required packages

There are some required packages that are necessary to build and publish the jupyter book. 
```
pip3 install --user jupyter-book
pip3 install --user ghp-import
```

### Build the jupyter book

Once you’ve added content and configured your book, it’s time to build your book. This is done with the ``jupyter-book build`` command.
```
jupyter-book build .
```

### Publish the jupyter book
Once your content is on GitHub, you can easily host it as a GitHub Pages website. Use the ``ghp-import`` tool to automatically push your Github pages to a website.
```
ghp-import -n -p -f _build/html
```
Use the ghp-import tool to automatically push your built documentation to a gh-pages branch.
### Building and publishing your book to the repo 

On cheyenne, I cannot directly use the command ``jupyter-book`` and ``ghp-import``. I have to use the full path.   
```
~/.local/bin/jupyter-book build .
~/.local/bin/ghp-import -n -p -f _build/html
```




