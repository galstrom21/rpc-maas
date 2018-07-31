Validates returned check metrics from the local ``hp_monitoring.py``
plugin for all deployed hosts. This check utilizes ``hpasmcli -s 'show
dimm'`` to verify the ``Status`` value is ``Ok``, which returns a ``1``
metric. If the ``hardware_memory_status`` metric is not ``1`` for three
successive intervals, a critical alarm notification is generated.
