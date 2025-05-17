FROM grafana/grafana-enterprise:10.1.5

ENV GF_AUTH_DISABLE_LOGIN_FORM="true"
ENV GF_AUTH_ANONYMOUS_ENABLED="true"
ENV GF_AUTH_ANONYMOUS_ORG_NAME="Main Org."
ENV GF_AUTH_ANONYMOUS_ORG_ROLE="Viewer"
ENV GF_INSTALL_PLUGINS="ae3e-plotly-panel,grafana-bigquery-datasource"
ENV GF_LOG_LEVEL="warn"
ENV GF_PATHS_PROVISIONING="/etc/grafana/provisioning"
ENV GF_SECURITY_DISABLE_INITIAL_ADMIN_CREATION="true"
ENV GF_SERVER_HTTP_PORT="8080"
ENV GF_USERS_HOME_PAGE="/d/20250110a"
ENV GF_DASHBOARDS_MIN_REFRESH_INTERVAL="1h"

COPY dashboards/* /var/lib/grafana/dashboards/
COPY provisioning/dashboards/* /etc/grafana/provisioning/dashboards/
COPY provisioning/datasources/* /etc/grafana/provisioning/datasources/

