OpenCensus httplib Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-httplib.svg
   :target: https://pypi.org/project/opencensus-ext-httplib/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-httplib
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-httplib
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-httplib
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-httplib

OpenCensus can trace HTTP requests made with the httplib library.

You can enable requests integration by specifying ``'httplib'`` to ``trace_integrations``.

It's possible to configure a list of URL you don't want traced. See requests integration
for more information. The only difference is that you need to specify hostname and port
every time.

Installation
------------

::

    pip install opencensus-ext-httplib

Usage
-----

.. code:: python

    import requests
    from opencensus.trace import config_integration
    from opencensus.trace.tracer import Tracer

    config_integration.trace_integrations(['httplib'])
    tracer = Tracer()

    with tracer.span(name='parent'):
        response = requests.get('https://www.wikipedia.org/wiki/Rabbit')

References
----------

* `OpenCensus Project <https://opencensus.io/>`_
