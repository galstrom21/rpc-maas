Validates returned check metrics from the local ``disk_utilisation.py`` plugin
from all nodes. If the ``disk_utilisation_{{device}}`` metric reaches a 99%
threshold for three successive intervals, a critical alarm notification is
generated.
