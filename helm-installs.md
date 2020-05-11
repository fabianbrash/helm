# Helm installs

<pre><code>
helm repo update

helm install nfs-provisioner --set nfs.server=192.168.1.10 --set nfs.path=/mnt/nfskubernetes/tkg-cluster-1 stable/nfs-client-provisioner -n nfs-provisioner




helm show values stable/prometheus --version 11.1.5 > ~/kubernetes/YAML/helm-prometheus.yaml

helm install prometheus -f ~/kubernetes/YAML/helm-prometheus.yaml stable/prometheus --version 11.1.5 -n monitoring

helm show values stable/grafana --version 5.0.22 > ~/kubernetes/YAML/helm-grafana.yaml

helm install grafana -f ~/kubernetes/YAML/helm-grafana.yaml stable/grafana --version 5.0.22 -n monitoring
</pre></code>
