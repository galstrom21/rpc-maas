The Glance category is driven by plugins ``glance_api_local_check.py``
and ``glance_registry_local_check.py``, which run contextually on
``glance_api`` and ``glance_registry`` inventory groups. These plugins
generate metrics via the Glance API at a local container level and from
the load balanced endpoint targeting all aspects of Glance
functionality. Check templates are deployed to each node in the
mentioned inventory groups.
