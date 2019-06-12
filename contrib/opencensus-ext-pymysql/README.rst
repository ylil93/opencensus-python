OpenCensus PyMySQL Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-pymysql.svg
   :target: https://pypi.org/project/opencensus-ext-pymysql/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-pymysql
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-pymysql
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-pymysql
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-pymysql

Installation
------------

::

    pip install opencensus-ext-pymysql

Usage
-----

.. code:: python

    from opencensus.trace import config_integration

    config_integration.trace_integrations(['pymysql'])

References
----------

* `OpenCensus Project <https://opencensus.io/>`_

