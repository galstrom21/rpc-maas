The conntrack_count check utilizes a custom plugin, ``conntrack_count.py``,
which runs locally on all hosts to generate metrics regarding the current
``nf_conntrack_count`` and total ``nf_conntrack_max`` values. If current
conntrack connections exhaust the maximum limit, all subsequent connections
will be dropped on the associated node. This value is crucial to monitor in
OpenStack deployments as differing workloads may uniquely impact environments.
