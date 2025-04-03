#Install Blackbox Exporter
helm install blackbox-exporter prometheus-community/prometheus-blackbox-exporter -f blackbox-values.yaml -n monitoring

#Add Blackbox Exporter as a Target in Prometheus
helm upgrade prometheus-stack prometheus-community/kube-prometheus-stack -f kube-prometheus-values.yaml -n monitoring
