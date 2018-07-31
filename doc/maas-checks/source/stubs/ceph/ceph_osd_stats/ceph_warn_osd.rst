Validates returned check metrics from the local ``ceph_monitoring.py`` plugin.
If the ``osd.{{osd_id}}_up`` metric is ``0`` for three successive intervals, a
critical alarm notification is generated.
