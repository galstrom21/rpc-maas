The Host category is driven by a multitude of agent-based functionality
(rackspace-monitoring-agent) and local plugins in order to gather a wide
gamut of metrics for bare-metal nodes. These metrics range from the
following sub-categories:

- CPU idle (*CDM*)
- Disk IO utilization (*CDM*)
- Memory usage (*CDM*)
- Conntrack limits
- Filesystem usage
- Network interface throughput (*CDM*)
- IMCP (Ping) validation
- SSH port validation
- Hardware (Only on Rackspace supported chassis models)

  * HP

    + Processor status
    + Memory status
    + Disk status
    + RAID controller status
    + RAID battery status
    + RAID cache status

  * Dell

    + Processor status
    + Memory status
    + Virtual/physical disk status

At a minimum, metrics and alarms are deployed across all hosts. However,
items labeled as *CDM* in the above list do not generate alarm
notifications (tickets) for any node outside of the ``infra_hosts``
inventory group. This is enforced as Rackspace engineers are typically
unable to remediate issues as a result of overallocation or general high
utilization of underlying resources.
