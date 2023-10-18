FROM grafana/grafana-enterprise:10.1.5

#ENV GF_AUTH_DISABLE_LOGIN_FORM="true"
ENV GF_FEATURE_TOGGLES_ENABLE="publicDashboards"
ENV GF_INSTALL_PLUGINS="nline-plotlyjs-panel,grafana-bigquery-datasource"
#ENV GF_SECURITY_DISABLE_INITIAL_ADMIN_CREATION="true"
ENV GF_PATHS_PROVISIONING="/etc/grafana/provisioning"
ENV GF_SERVER_HTTP_PORT="8080"
ENV GF_USERS_ALLOW_ORG_CREATE="false"
ENV GF_USERS_ALLOW_SIGN_UP="false"

COPY dashboards/* /var/lib/grafana/dashboards/
COPY provisioning/dashboards/* /etc/grafana/provisioning/dashboards/
COPY provisioning/datasources/* /etc/grafana/provisioning/datasources/
