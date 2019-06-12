OpenCensus Django Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-django.svg
   :target: https://pypi.org/project/opencensus-ext-django/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-django
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-django
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-django
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-django

Installation
------------

::

    pip install opencensus-ext-django

Usage
-----

For tracing Django requests, you will need to add the following line to
the ``MIDDLEWARE_CLASSES`` section in the Django ``settings.py`` file.

.. code:: python

    MIDDLEWARE_CLASSES = [
        ...
        'opencensus.ext.django.middleware.OpencensusMiddleware',
    ]

And add this line to the ``INSTALLED_APPS`` section:

.. code:: python

    INSTALLED_APPS = [
        ...
        'opencensus.ext.django',
    ]

Additional configuration can be provided, please read
`Customization <https://github.com/census-instrumentation/opencensus-python#customization>`_
for a complete reference.

.. code:: python

    OPENCENSUS = {
        'TRACE': {
            'SAMPLER': 'opencensus.trace.samplers.ProbabilitySampler(rate=1)',
            'EXPORTER': '''opencensus.ext.ocagent.trace_exporter.TraceExporter(
                service_name='foobar',
            )''',
        }
    }

References
----------

* `OpenCensus Project <https://opencensus.io/>`_
