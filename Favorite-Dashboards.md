# Favorite Dashboards

1. Cadvisor exporter: 14282 (4.5)
   - Link: https://grafana.com/grafana/dashboards/14282-cadvisor-exporter/
   - Require: cadvisor exporter
   - Advantage: Can manage Docker Hosts and containers inside using only 1 Dashboard
2. Docker and OS metrics ( cadvisor, node_exporter ): 10566 (3)
   - Link: https://grafana.com/grafana/dashboards/10566-docker-and-os-metrics/
   - Similar to 123, but requires additional service setup: cadvisor, node_exporter
3. Docker monitoring with node selection: 8321 (3.5)
   - Advantage:Monitoring host overview.
   - Limit: Not enough detail, cannot monitor all details of containers in the host
   - Link: https://grafana.com/grafana/dashboards/8321-docker-monitoring-with-node-selection/
4. Docker-cAdvisor: 13946 (4.2)
   - Link: https://grafana.com/grafana/dashboards/13946-docker-cadvisor/
   - Advantage: Similar to 3, but displays containers in the host in more detail and is easier to see
