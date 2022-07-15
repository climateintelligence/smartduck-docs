# GUIDE: Writing documentation and tests

Last but not least, a very very important point is to write a good documentation about your work! Each WPS (bird) has a docs folder for this where the documentation is written in reStructuredText_ and generated with Sphinx_.

* http://sphinx-doc.org/tutorial.html
* http://quick-sphinx-tutorial.readthedocs.io/en/latest/

The documentation is automatically published to ReadTheDocs_ with GitHub webhooks.
It is important to keep the :ref:`codestyle` and write explanations to your functions. There is an auto-api for documentation of functions.

The main `documentation`_ (which you are reading now) is the starting point to
get an overview of birdhouse. Each birdhouse component comes with
its own Sphinx documentation and is referenced by the main birdhouse document. Projects using birdhouse components like PAVICS_ or `COPERNICUS Data Store`_ generally have their own documentation as well. To include documentation from external repository here, two custom made sphinx directives can be used. The `gittoctree` directive behaves like a normal table of content directive (`toctree`), but takes as an argument the URL to the git repo and refers to files inside this directory through their full path. The `gitinclude` directive acts like an normal `include` directive, but takes as a first argument the URL to the git repo this file belongs to. For example:

.. code-block:: sphinx
   :linenos:

   Here is the text of the birdhouse main documentation. At the place where you want to integrate
   a part of a remote sphinx documentation stored in a `git` repository you can fetch the docs
   parts and integrated it with a table of content referring to external files:

   .. gittoctree:: https://github.com/Ouranosinc/pavics-sdi.git

      docs/source/arch/backend.rst

   or include an individual file:

   .. gitinclude:: https://github.com/Ouranosinc/pavics-sdi.git docs/source/arch/backend.rst

   The directive will clone and checkout the repository, then include these external files as if
   they were part of the native documentation.

 .. _writing_tests:

 Writing tests
 .............

 Writing tests is an essential part of software development. The WPS templates produced by Cookiecutter_ include the initial folders needed for units tests and basic dependencies in the environment.
 There are two parts of tests:

 * Unit tests:
 python pytest to check the functionality of functions and processes. They are stored in the folder `{bird WPS}/tests` and appropriate test data  `{bird WPS}/tests/testdata`.

 * notebook tests:
 Code examples of the documentation to demonstrate the usage of WPS services. The examples are written in jupyter notebooks and stored in the documentation folder `{bird WPS}/docs/source/notebooks/`
