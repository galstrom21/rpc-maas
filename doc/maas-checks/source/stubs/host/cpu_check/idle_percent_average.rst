Validates check metrics from the native ``agent.cpu`` functionality for all
``infra_hosts`` inventory hosts. If metric ``idle_percent_average`` falls below
the ``1`` percent threshold for 3 successive intervals, a critical alarm
notification is generated. This is typically indicative of an issue as the
infrastructure hosts should not be resource constrained.
