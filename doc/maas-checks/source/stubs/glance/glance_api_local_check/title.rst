Utilizes a custom plugin, ``glance_api_local_check.py``, which runs
locally to generate metrics from each ``glance_api`` (infrastructure)
node. This check subverts the typical load balanced Glance API in order
to validate functionality at the container level. This provides an
additional level of granularity to ensure the Glance API is
operationally healthy across all backends.
