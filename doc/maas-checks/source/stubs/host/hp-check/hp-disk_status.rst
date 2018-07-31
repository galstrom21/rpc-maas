Validates returned check metrics from the local ``hp_monitoring.py`` plugin for
all deployed hosts. This check utilizes ``ssacli ctrl all show config`` to
verify any ``logicaldrive`` values are ``OK`` or ``OK, Encrypted``, which
returns a ``1`` metric. If the ``hardware_disk_status`` metric is not ``1`` for
three successive intervals, a critical alarm notification is generated.
