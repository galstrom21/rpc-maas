The API category contains `remote.http
<https://developer.rackspace.com/docs/rackspace-monitoring/v1/tech-ref-info/check-type-reference/#remote-http>`_
checks and alarms for all supported OpenStack service endpoints. The
checks are deployed to the ``shared-infra_hosts`` inventory group and
are only enabled on a single node. The check queries the associated
service endpoints using the defined ``external_lb_vip_address`` to
determine whether a valid response code is returned. Depending on
whether the endpoint resides within RFC 1918 address space, the
service-specific ``lb_api_check_*`` or ``private_lb_api_check_*`` check
is deployed.
