Validates returned check metrics from the local ``hp_monitoring.py``
plugin for all deployed hosts. This check utilizes ``ssacli ctrl all
show status`` to verify the ``Battery/Capacitor Status`` value is
``OK``, which returns a ``1`` metric. If the
``hardware_controller_battery_status`` metric is not ``1`` for three
successive intervals, a critical alarm notification is generated.
