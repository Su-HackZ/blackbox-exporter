# blackbox-exporter

Blackbox-expoter install 

https://github.com/prometheus-community/helm-charts/tree/main/charts/prometheus-blackbox-exporter


Add helm repo:

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts


Install blackbox exporter:

helm install blackbox-exporter prometheus-community/prometheus-blackbox-exporter  -f values.yaml 

YAML Avail at git:
	https://github.com/Su-HackZ/blackbox-exporter/blob/main/values.yaml


Check the deployment:

kubectl get all -n report-builder-development


Check the matrics of blackbox:

kubectl port-forward service/blackbox-exporter-prometheus-blackbox-exporter -n report-builder-development 9115:9115

check at the local host:     http://127.0.0.1:9115


Check svc monitorig:

kubectl descibe servicemonitor blackbox-exporter-prometheus-blackbox-exporter-report-builer-monitoring 
