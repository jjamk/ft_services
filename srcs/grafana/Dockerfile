FROM	alpine:latest

RUN		apk update && apk upgrade
RUN     apk add grafana --repository=http://dl-3.alpinelinux.org/alpine/edge/testing/

COPY	cfg/grafana.ini /usr/share/grafana/conf/custom.ini
COPY	cfg/datasources.yaml /usr/share/grafana/conf/provisioning/datasources/influxdb.yaml
COPY	cfg/dashboards.yaml /usr/share/grafana/conf/provisioning/dashboards/dashboards.yaml
COPY	cfg/skang-dashboard.json /var/lib/grafana/dashboards/skang-dashboard.json
COPY	cfg/skang-dashboard1.json /var/lib/grafana/dashboards/skang-dashboard1.json
COPY	cfg/skang-dashboard2.json /var/lib/grafana/dashboards/skang-dashboard2.json
COPY	cfg/skang-dashboard3.json /var/lib/grafana/dashboards/skang-dashboard3.json
COPY	cfg/skang-dashboard4.json /var/lib/grafana/dashboards/skang-dashboard4.json
COPY	cfg/skang-dashboard5.json /var/lib/grafana/dashboards/skang-dashboard5.json
COPY	cfg/skang-dashboard6.json /var/lib/grafana/dashboards/skang-dashboard6.json
COPY	cfg/skang-dashboard7.json /var/lib/grafana/dashboards/skang-dashboard7.json

EXPOSE	3000

CMD		/usr/sbin/grafana-server --homepath=/usr/share/grafana
