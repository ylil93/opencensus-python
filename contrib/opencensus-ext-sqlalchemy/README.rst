OpenCensus SQLAlchemy Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-sqlalchemy.svg
   :target: https://pypi.org/project/opencensus-ext-sqlalchemy/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-sqlalchemy
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-sqlalchemy
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-sqlalchemy
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-sqlalchemy

You can trace usage of the `sqlalchemy package`_, regardless of the underlying
database, by specifying ``'sqlalchemy'`` to ``trace_integrations``.

.. _SQLAlchemy package: https://pypi.org/project/SQLAlchemy

.. note:: If you enable tracing of SQLAlchemy as well as the underlying database
    driver, you will get duplicate spans. Instead, just trace SQLAlchemy.

Installation
------------

::

    pip install opencensus-ext-sqlalchemy

Usage
-----

.. code:: python

    from opencensus.trace import config_integration

    config_integration.trace_integrations(['sqlalchemy'])

References
----------

* `OpenCensus Project <https://opencensus.io/>`_
