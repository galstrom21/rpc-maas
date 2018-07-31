Validates returned check metrics from the local ``hp_monitoring.py``
plugin for all deployed hosts. This check utilizes ``ssacli ctrl all
show status`` to verify the ``Cache Status`` value is ``OK`` or ``Not
Configured``, which both return a ``1`` metric. If the
``hardware_controller_cache_status`` metric is not ``1`` for three
successive intervals, a critical alarm notification is generated.
