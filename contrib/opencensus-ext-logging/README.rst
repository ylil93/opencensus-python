OpenCensus logging Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-logging.svg
   :target: https://pypi.org/project/opencensus-ext-logging/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-logging
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-logging
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-logging
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-logging

The logging integration enriches the log records with trace ID, span ID and sampling flag.
The following attributes will be added to ``LogRecord``:

    * traceId
    * spanId
    * traceSampled

Note that this only takes effect for loggers created after the integration.

Installation
------------

::

    pip install opencensus-ext-logging

Usage
-----

.. code:: python

    import logging

    from opencensus.trace import config_integration
    from opencensus.trace.samplers import AlwaysOnSampler
    from opencensus.trace.tracer import Tracer

    config_integration.trace_integrations(['logging'])
    logging.basicConfig(format='%(asctime)s traceId=%(traceId)s spanId=%(spanId)s %(message)s')
    tracer = Tracer(sampler=AlwaysOnSampler())

    logger = logging.getLogger(__name__)
    logger.warning('Before the span')
    with tracer.span(name='hello'):
        logger.warning('In the span')
    logger.warning('After the span')


References
----------

* `OpenCensus Project <https://opencensus.io/>`_
