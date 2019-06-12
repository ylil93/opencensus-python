OpenCensus PostgreSQL Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-postgresql.svg
   :target: https://pypi.org/project/opencensus-ext-postgresql/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-postgresql
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-postgresql
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-postgresql
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-postgresql

The integration with PostgreSQL supports the `psycopg2`_ library and is specified
to ``trace_integrations`` using ``'postgresql'``.

.. _psycopg2: https://pypi.org/project/psycopg2

Installation
------------

::

    pip install opencensus-ext-postgresql

Usage
-----

.. code:: python

    from opencensus.trace import config_integration

    config_integration.trace_integrations(['postgresql'])

References
----------

* `OpenCensus Project <https://opencensus.io/>`_
