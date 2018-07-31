Utilizes a custom ``agent.plugin`` check type, ``ceph_monitoring.py``.
The plugin runs locally from all Ceph osd nodes in the inventory, resulting
in metrics based on the overall health status of each underlying OSD.

The ``osd.{{osd_id}}_up`` metric is a boolean:

.. code-block:: console

    0: OSD is unhealthy
    1: OSD is healthy


An example of properly executing ``ceph_osd_stats``:

.. code-block:: console

    root@ceph1:~# /usr/lib/rackspace-monitoring-agent/plugins/run_plugin_in_venv.sh \
      /usr/lib/rackspace-monitoring-agent/plugins/ceph_monitoring.py \
      --name client.raxmon \
      --keyring /etc/ceph/ceph.client.raxmon.keyring \
      osd \
      --osd_ids "3 1"
    status okay
    metric osd.3_up uint32 1
    metric osd.1_up uint32 1
