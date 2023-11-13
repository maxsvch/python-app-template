.. _development:

===========
Development
===========

Development goals
=================

PROJECT_NAME_UPPER is a top level library. The main driving goals are the following ones:

*   validation
*   maintainability

The first goal, validation, implies tests must be as extensive as possible. They should include realistic operational cases but also contingency cases. A very high level of coverage is desired.

The second goal, maintainability, implies code must be readable, clear and well documented. Part of this goal is enforced by the stylistic rules explained in the next section, but this is only for the automatic and simple checks. It is important to keep a clean and extensible design. Achieving simplicity is really hard, so this goal should not be taken too lightly. Good designs are a matter of balance between two few objects that do too many things internally an ignore each other and too many objects that do nothing alone and always need a bunch of other objects to work. Always think in terms of balance, and check what happens if you remove something from the design. Quite often, removing something improves the design and should be done.

Style Rules
===========

For reading ease and consistency, the existing code style should be preserved for all new developments. PROJECT_NAME_UPPER follows `PEP8`_ coding rules.

Pre-commit validation
---------------------

A pre-commit validation is installed with code quality tools (see below).

Here is the way to install it in the dev virtual env:

.. code-block:: console

  $ pre-commit install

This installs the pre-commit hook in `.git/hooks/pre-commit`  from `.pre-commit-config.yaml` file configuration.

It is possible to test pre-commit before commiting:

.. code-block:: console

  $ pre-commit run --all-files                # Run all hooks on all files
  $ pre-commit run --files PROJECT_NAME_LOWER/__init__.py   # Run all hooks on one file
  $ pre-commit run pylint                     # Run only pylint hook


Code quality
~~~~~~~~~~~~

PROJECT_NAME_UPPER uses `Isort`, `Black`, `Flake8` and `Pylint` quality code checking.


Tests
======

PROJECT_NAME_UPPER includes a set of tests executed with `pytest <https://docs.pytest.org/>`_ tool.

To launch tests:

.. code-block:: console

    $ pytest

It is also possible to execute only a specific part of the test, either by indicating the test file to run by using the ``-k`` option.

.. _`PEP8`: https://peps.python.org/pep-0008/
