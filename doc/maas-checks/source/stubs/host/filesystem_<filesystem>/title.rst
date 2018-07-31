At deployment time, the playbooks enumerate each host to determine mounted
filesystems. Each detected filesystem will have monitoring deployed. The
filesystem check utilizes native ``agent.filesystem`` functionality within the
``rackspace-monitoring-agent`` to build metrics for filesystem-related usage.
