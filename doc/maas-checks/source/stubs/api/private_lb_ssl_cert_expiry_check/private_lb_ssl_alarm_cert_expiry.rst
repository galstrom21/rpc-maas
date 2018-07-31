Validates returned check metrics from the Horizon API. If the ``cert_end_in``
metric is less than ``604800`` seconds (7 days) for three successive intervals,
a critical alarm notification is generated.
