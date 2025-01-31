OpenCensus gRPC Integration
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-grpc.svg
   :target: https://pypi.org/project/opencensus-ext-grpc/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-grpc
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-grpc
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-grpc
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-grpc

OpenCensus provides the implementation of interceptors for both the client side
and server side to instrument the gRPC requests and responses. The client
interceptors are used to create a decorated channel that intercepts client
gRPC calls and server interceptors act as decorators over handlers.

gRPC interceptor is a new feature in the grpcio1.8.0 release, please upgrade
your grpcio to the latest version to use this feature.

For sample usage, please refer to the hello world example in the examples
directory.

More information about the gRPC interceptors please see the `proposal`_.

.. _proposal: https://github.com/mehrdada/proposal/blob/python-interceptors/L13-Python-Interceptors.md

Installation
------------

::

    pip install opencensus-ext-grpc

Usage
-----

.. code:: python

    from opencensus.trace import config_integration

    config_integration.trace_integrations(['grpc'])

References
----------

* `gRPC <https://grpc.io/>`_
* `OpenCensus Project <https://opencensus.io/>`_
