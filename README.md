# linux-monitoing
use docker container to monitor linux usage and generate alert via email

# docker containers
- node-exporter
- prometheus
- alertmanager
- grafana

# node-exporter
- export linux metrics to [http://localhost:9100/metrics](http://localhost:9100/metrics)
- node-exporter is targeted and collected by prometheus

# prometheus
- collect metrics from node-exporter [http://localhost:9090/targets](http://localhost:9090/targets)
- define monitoring rules in /prometheus/testing_rules.yml
- send requests to AlertManager when alerts need to be sent to receivers

# alertmanager
- handle alert sending to receiver via sms, wechat, email, discord...

# grafana
- visualize metrics collected by prometheus from node-exporter
- import dashboard from community
- monitoring rules can reference dashboard
