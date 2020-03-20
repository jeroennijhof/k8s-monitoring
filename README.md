# k8s-monitoring
Set of deployment files to monitoring k8s with prometheus

## Deploy monitoring
Execute the following to deploy monitoring to k8s in a namespace called monitoring.<br>
Alertmanager is just an example so you might need to adjust settings as well as the alert rules for prometheus.
```
$ kubectl apply -f namespace.yml
$ kubectl apply -f kube-state-metrics/deployment.yaml
$ kubectl apply -f kube-state-metrics/rbac.yml
$ kubectl apply -f kube-state-metrics/service.yaml
$ kubectl apply -f prometheus-rbac.yml
$ kubectl apply -f prometheus.yml
$ kubectl apply -f alertmanager.yml
```
