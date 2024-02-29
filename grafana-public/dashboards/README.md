# Dashboards

Any dashboard here will be automatically loaded by Grafana.

Each dashboard `uid` should be a short number or phrase to minimize URL length.
The uid must be unique across all dashbords here. No duplicates are allowed.

When exporting dashboards from another Grafana instance and copying them here,
remember to update the uid accordingly.

## Configuring datasources

Datasources should be configured indirectly through a variable. Recommended settings are:

* Use "Data source" variable type
* Name the variable "datasource" and do not use a label
* Show "Nothing" on dashboard so that the variable is hidden
* Data source type "Google BigQuery"
* Use no filters

Since there is only one datasource in the public instance, the first one will
become the default. Your development dashboard and the exported dashboard will
refer to a "${datasource}" variable rather than a specific datasource only
present in your development environment.
