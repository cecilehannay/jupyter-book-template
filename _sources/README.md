
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



Finally, open the notebooks and interact with them. Make sure to choose the "NPL 2023a" kernel.


### [NCAR JupyterHub](https://github.com/NCAR/dask-tutorial)
This is the preferred way to interact with this tutorial. Users with access to Casper can run the notebooks interactively, and will be able to save their work and pull in new updates.
To connect to NCAR JupyterHub, please open this link in a web browser: https://jupyterhub.hpc.ucar.edu/


### Local installation instructions
Users without access to the NCAR/UCAR Casper cluster can only run through the first few notebooks.
To run the notebooks locally:

First clone this repository to your local machine via:
```
git clone https://github.com/NCAR/dask-tutorial
```

Next, download conda (if you haven't already)

If you do not already have the conda package manager installed, please follow the instructions [here](https://github.com/conda-forge/miniforge#install).

Now, create a conda environment:

Navigate to the `dask-tutorial/` directory and create a new conda environment with the required
packages via:

```terminal
cd dask-tutorial
conda env update --file environment.yml
```

This will create a new conda environment named "dask-tutorial".

Next, activate the environment:

```
conda activate dask-tutorial
```

Finally, launch JupyterLab with:

```
jupyter lab
```

## Contributing
We welcome contributions from the community! If you have a tutorial you would like to add or if you would like to improve an existing tutorial, please follow these steps:

Fork the repository.

Clone the repository to your local machine:
```
git clone https://github.com/your-username/dask-tutorial-repository.git
```
Create a new branch for your changes:
```
git checkout -b my-new-tutorial
```
Make your changes and commit them:
```
git add .
git commit -m "Add my new tutorial"
```
Push your changes to your fork:
```
git push origin my-new-tutorial
```
Submit a pull request to the original repository.



## Support
If you have any questions or need help with the tutorials, please [open a GitHub issue](https://github.com/NCAR/dask-tutorial/issues/new?title=Issue%20on%20page%20%2FREADME.html&body=Your%20issue%20content%20here.) in the repository.

## 👍 Acknowledgments

* NCAR CISL/CSG Team
* ESDS Initiative

## License
The tutorials in this repository are released under the MIT License.
 

