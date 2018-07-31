Utilizes a custom ``agent.plugin`` check type, ``ceph_monitoring.py``.
The plugin runs locally from the all Ceph radosgw nodes in the
inventory, resulting in metrics based on the overall health status of
the local radosgw API. Each radosgw address is dynamically generated
based on the HTTP protocol and local address and port.

Valid ``rgw_up`` metrics are ``0``, ``1``, and ``2`` with the following
descriptions:

.. code-block:: console

    0: RGW node is in an ERROR state
    1: RGW node is in a WARNING state
    2: RGW node is in an OK state


An example of properly executing ``ceph_rgw_stats``:

.. code-block:: console

    root@ceph1:~# /usr/lib/rackspace-monitoring-agent/plugins/run_plugin_in_venv.sh \
      /usr/lib/rackspace-monitoring-agent/plugins/ceph_monitoring.py \
      --name client.raxmon \
      --keyring /etc/ceph/ceph.client.raxmon.keyring \
      rgw \
      --rgw_address http://172.29.236.36:8080
    status okay
    metric rgw_up uint32 2
