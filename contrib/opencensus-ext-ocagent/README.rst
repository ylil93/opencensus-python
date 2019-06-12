OpenCensus OC-Agent Exporter
============================================================================

|pypi| |compat_check_pypi| |compat_check_github|

.. |pypi| image:: https://badge.fury.io/py/opencensus-ext-ocagent.svg
   :target: https://pypi.org/project/opencensus-ext-ocagent/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=opencensus-ext-ocagent
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=opencensus-ext-ocagent
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-ocagent
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/census-instrumentation/opencensus-python.git%23subdirectory%3Dopencensus-ext-ocagent

Installation
------------

::

    pip install opencensus-ext-ocagent

Usage
-----

Stats
~~~~~

.. code:: python

    from opencensus.ext.ocagent import stats_exporter as ocagent_stats_exporter

    ocagent_stats_exporter.new_stats_exporter(
        service_name='service_name',
        endpoint='localhost:55678')

References
----------

* `OpenCensus Project <https://opencensus.io/>`_
* `OpenCensus Services <https://github.com/census-instrumentation/opencensus-service>`_
