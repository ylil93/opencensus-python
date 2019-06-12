OpenCensus Zipkin Exporter
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-zipkin.svg
   :target: https://pypi.org/project/opencensus-ext-zipkin/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-zipkin
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-zipkin
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-zipkin
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-zipkin

Installation
------------

::

    pip install opencensus-ext-zipkin

Usage
-----

The **OpenCensus Zipkin Exporter** allows you to export `OpenCensus`_ traces to `Zipkin`_.

.. _OpenCensus: https://github.com/census-instrumentation/opencensus-python/
.. _Zipkin: https://zipkin.io/

.. code:: python

    from opencensus.ext.zipkin.trace_exporter import ZipkinExporter
    from opencensus.trace import tracer as tracer_module

    tracer = tracer_module.Tracer(exporter=ZipkinExporter(
        service_name='my service',
        host_name='localhost',
        port=9411,
    ))

    with tracer.span(name='hello'):
        print('Hello, World!')

References
----------

* `OpenCensus Project <https://opencensus.io/>`_
* `Zipkin <https://zipkin.io/>`_
