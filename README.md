Flask-Boost
===========

Flask application generator for boosting your development.


Installation
------------

::

    pip install boot

Development Guide
-----------------

Init project
~~~~~~~~~~~~

::

    boot new <your_project_name>

Setup backend requirements
~~~~~~~~~~~~~~~~~~~~~~~~~~
 
::

    cd <your_project_dir>
    virtualenv venv
    source venv/bin/activate 
    pip install -r requirements.txt

**Note**: if you failed in ``pip install -r requirements.txt`` in Windows, try to install package binaries directly:

* pycrpyto: try to follow this article compiling-pycrypto-on-win7-64_, or get the complied pycrypyto library directly: archive_pycrpyto_library_.

.. _compiling-pycrypto-on-win7-64: https://yorickdowne.wordpress.com/2010/12/22/compiling-pycrypto-on-win7-64/
.. _archive_pycrpyto_library: http://archive.warshaft.com/pycrypto-2.3.1.win7x64-py2.7x64.7z

Init database
~~~~~~~~~~~~~

Create database with name ``your_project_name`` and encoding ``utf8``.

Update ``SQLALCHEMY_DATABASE_URI`` in ``config/development.py`` as needed.

Then init tables::

    python manage.py db upgrade

Run app
~~~~~~~

Run local server::

    python manage.py run


MIT