Queries the OpenStack Horizon API using remote pollers and standard HTTP
GET method. The check returns metrics that are used to validate custom
SSL certificates configured on the Horizon endpoint. This check is
deployed to each controller node, but only enabled on the first node of
the inventory group when endpoints are configured with a custom SSL
certificate.
