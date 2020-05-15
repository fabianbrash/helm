# Helm installs

<pre><code>
helm repo update

helm install metrics-server -f ~/kubernetes/YAML/helm-metrics-server.yaml stable/metrics-server -n metrics
helm install nfs-provisioner --set nfs.server=192.168.1.10 --set nfs.path=/mnt/nfskubernetes/tkg-cluster-1 stable/nfs-client-provisioner -n nfs-provisioner

helm show values stable/nfs-server-provisioner --version 1.0.0 > ~/kubernetes/YAML/helm-nfs-server.yaml

helm install nfs-server -f ~/kubernetes/YAML/helm-nfs-server.yaml stable/nfs-server-provisioner --version 1.0.0 -n nfs-server | tee -a ~/kubernetes/helm-nfs-server.log

helm show values stable/prometheus --version 11.1.5 > ~/kubernetes/YAML/helm-prometheus.yaml

helm install prometheus -f ~/kubernetes/YAML/helm-prometheus.yaml stable/prometheus --version 11.1.5 -n monitoring | tee -a ~/helm-prometheus.log

helm show values stable/grafana --version 5.0.22 > ~/kubernetes/YAML/helm-grafana.yaml

helm install grafana -f ~/kubernetes/YAML/helm-grafana.yaml stable/grafana --version 5.0.22 -n monitoring | tee -a ~/helm-grafana.log

helm install nginx-ingress -f ~/kubernetes/YAML/helm-nginx-ingress.yaml stable/nginx-ingress --version 1.36.3 -n nginx-ingress

</pre></code>

# More to come..
