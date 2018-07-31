The Heat category is driven by plugins ``heat_api_local_check.py``, and
``service_api_local_check.py``, which run contextually on ``heat_api``,
``heat_api_cfn``, and ``heat_api_cloudwatch`` inventory groups. These
plugins generate metrics via the associated Heat APIs at a local
container level to ensure all Heat APIs are up-and-running. Check
templates are deployed to each node in the mentioned inventory groups.
