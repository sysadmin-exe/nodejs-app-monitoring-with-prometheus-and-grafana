# nodejs-app-monitoring-with-prometheus-and-grafana

This was done with assistance from https://codersociety.com/blog/articles/nodejs-application-monitoring-with-prometheus-and-grafana

## Docker command to start Grafana 
docker run --rm -p 3000:3000 -e GF_AUTH_DISABLE_LOGIN_FORM=true -e GF_AUTH_ANONYMOUS_ENABLED=true -e GF_AUTH_ANONYMOUS_ORG_ROLE=Admin -v `pwd`/datasources.yaml:/etc/grafana/provisioning/datasources/datasources.yaml grafana/grafana:7.1.5

## Docker command to start Prometheus
docker run --rm -p 9090:9090   -v `pwd`/prometheus.yaml:/etc/prometheus/prometheus.yaml   prom/prometheus:v2.20.1

## The above docker commands are run in the project directory

