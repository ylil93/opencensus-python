OpenCensus threading Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-threading.svg
   :target: https://pypi.org/project/opencensus-ext-threading/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-threading
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-threading
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-threading
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-threading

OpenCensus can propagate trace across threads when using the threading package.

You can enable Threading integration by specifying ``'threading'`` to ``trace_integrations``.

Installation
------------

::

    pip install opencensus-ext-threading

Usage
-----

.. code:: python

    from opencensus.trace import config_integration

    config_integration.trace_integrations(['threading'])

References
----------

* `OpenCensus Project <https://opencensus.io/>`_
