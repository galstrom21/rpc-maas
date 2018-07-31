The HP check utilizes a custom plugin, ``hp_monitoring.py``, which
incorporates the native HP Management Control Pack (MCP) utilities to
provide system-level commands for interfacing with HP hardware. This
tooling is not installed as part of rpc-maas playbooks. The plugin
generates metrics based on the status of the following components:

- Processor status
- Memory status
- Disk status
- Power supply status
- RAID controller status
- RAID battery status
- RAID cache status

Rackspace currently supports the following HP chassis:

- DL 380 Gen 9
- DL 380 Gen 10
