Validates returned check metrics from the local
``cinder_service_check.py`` plugin run across ``cinder_volume`` nodes.
If the ``cinder-volume-{{key}}_status`` metric is not ``1`` for three
successive intervals, a critical alarm notification is generated. This
indicates the Cinder volume service is down on the associated backend.
