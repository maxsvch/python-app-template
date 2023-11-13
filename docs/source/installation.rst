.. _installation:

============
Installation
============

This help details installation on ubuntu release. 

Pre requisites
--------------

*   Python3 (3.8) with dev environment and pip

.. code-block:: console

 sudo apt-get install python3.8 python3.8-dev python3.8-venv 

OPTION 1 : Python virtual environment
-------------------------------------

Create virtual env and clone repository
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*   Create your virtual environment and activate it :

.. code-block:: console

    python3 -m venv VENV_NAME
    source VENV_NAME/bin/activate 
    pip install --upgrade pip 

*   Clone repository

.. code-block:: console

    git clone PROJECT_LINK

Install PROJECT_NAME_UPPER in python venv
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

  pip install -e .

*   to install dev env

.. code-block:: console

  pip install -e .[dev]
  pre-commit install

OPTION 2 : Conda virtual environment
------------------------------------

*   Build the conda environment :

.. code-block:: console
  
  conda env create -f environment.yml


*   Activate it : 

.. code-block:: console
  
  conda activate CONDA_ENV_NAME

OPTION 3 : Docker
-----------------

TODO