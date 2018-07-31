The ``disk_utilisation`` check utilizes a custom plugin,
``disk_utilisation.py``, which runs locally on all hosts to generate metrics
regarding the current disk  I/O values. For all hosts outside the
``infra_hosts`` inventory group, metrics are generated but not evaluated in any
form. Therefore, no alarm notifications or corresponding tickets are created.
For infrastructure hosts that fall in scope, disk I/O is measured and evaluated
when the ``disk_utilisation_{{device}}`` metric falls below a given threshold.
In these situations, it typically indicates a problem which may be impacting to
the environment.
