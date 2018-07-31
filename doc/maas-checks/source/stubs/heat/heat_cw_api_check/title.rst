Utilizes a custom plugin, ``service_api_local_check.py``, which runs
locally to generate metrics from each ``heat_api_cloudwatch``
(infrastructure) node. This check subverts the typical load balanced
Heat Cloudwatch API in order to validate functionality at the container
level. This provides an additional level of granularity to ensure the
Heat Cloudwatch API is operationally healthy across all backends.
