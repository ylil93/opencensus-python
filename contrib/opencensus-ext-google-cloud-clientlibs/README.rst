OpenCensus Google Cloud Client Libraries Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-google-cloud-clientlibs.svg
   :target: https://pypi.org/project/opencensus-ext-google-cloud-clientlibs/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-google-cloud-clientlibs
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-google-cloud-clientlibs
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-google-cloud-clientlibs
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-google-cloud-clientlibs

OpenCensus can trace HTTP and gRPC requests made with the `Cloud client libraries`_.
The request URL, method, and status will be collected.

You can enable Google Cloud client libraries integration by specifying ``'google_cloud_clientlibs'`` to ``trace_integrations``.

.. _Cloud client libraries: https://github.com/GoogleCloudPlatform/google-cloud-python#google-cloud-python-client

Installation
------------

::

    pip install opencensus-ext-google-cloud-clientlibs

Usage
-----

.. code:: python

    from opencensus.trace import config_integration

    config_integration.trace_integrations(['google_cloud_clientlibs'])

References
----------

* `OpenCensus Project <https://opencensus.io/>`_
