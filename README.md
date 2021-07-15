# sphinx_tutorial_dummy
A simple project documented with sphinx

# Sphinx Tutorial
*  Install Sphinx and Rinohtype in the virtual environment of the project you’re working on use the following commands below.
```
conda activate env_name
pip install Sphinx
pip install rinohtype
```
*  Create a docs directory and cd into this directory.
```
mkdir docs
cd docs
```
* Setup Sphinx
```
sphinx-quickstart
```
* Open source/conf.py
* Configure path to root directory
* Add Rinohtype to the list of extension
```
'rinoh.frontend.sphinx'
```
* Open the index.rst and change the content to the following. (Click the index.rst  link for full content)
```
Documentation for the Code
**************************
.. toctree::
   :maxdepth: 2
   :caption: Contents:

TeacherAPI main
===================
.. automodule:: app
   :members:

TeacherAPI controller
=====================
.. automodule:: teacherAPI.controller
   :members:

TeacherAPI models
=================
.. automodule:: teacherAPI.models
   :members:

TeacherAPI database
===================
.. automodule:: teacherAPI.database
   :members:

TeacherAPI populate
===================
.. automodule:: teacherAPI.populate
   :members:
```

* where automodule correspond with the name of the python file 
```
"""
.. module:: Exploratory Data Analysis
   :synopsis: Exploratory Data Analysis of the data set that contains the crimes in the city
    Data path and other configuration settings are indicated in config.ini

.. moduleauthor:: Jose Angel Velasco - (C) Tessella Spain by Capgemini Engineering - 2021
"""
```

* Still inside the docs directory run, Create the HTML documentation files.
```
make html
```
* Create the latex documentation files
```
make html
```
* Create the PDF documentation files
```
sphinx-build -b rinoh source _build/rinoh
```
