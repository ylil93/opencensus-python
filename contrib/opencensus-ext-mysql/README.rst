OpenCensus MySQL Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-mysql.svg
   :target: https://pypi.org/project/opencensus-ext-mysql/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-mysql
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-mysql
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-mysql
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-mysql

The integration with MySQL supports the `mysql-connector`_ library and is specified
to ``trace_integrations`` using ``'mysql'``.

.. _mysql-connector: https://pypi.org/project/mysql-connector

Installation
------------

::

    pip install opencensus-ext-mysql

Usage
-----

.. code:: python

    from opencensus.trace import config_integration

    config_integration.trace_integrations(['mysql'])

References
----------

* `OpenCensus Project <https://opencensus.io/>`_
