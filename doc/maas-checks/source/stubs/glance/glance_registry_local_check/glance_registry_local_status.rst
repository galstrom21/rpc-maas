Validates returned check metrics from the local
``glance_registry_local_check.py`` plugin run across ``glance_registry``
nodes. If the ``glance_registry_local_status`` metric is not ``1`` for
three successive intervals, a critical alarm notification is generated.
This indicates the Glance registry is down on the associated backend
container.
