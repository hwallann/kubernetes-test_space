# Test enviornment for Kubernetes, Helm and Tiller  
Kubernetes files used to test the platform  
  
## Minikube  
_Minikube_ is a platform for allowing _Kubernetes_ to be be used locally on a single computer.  
__Relevant sites:__  
  
- https://medium.com/@JockDaRock/minikube-on-windows-10-with-hyper-v-6ef0f4dc158c  
- https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/  
- https://kubernetes.io/docs/tasks/tools/install-minikube/  
- https://kubernetes.io/docs/setup/minikube/  
  
## Instructions  
- https://docs.helm.sh/using_helm/#quickstart-guide    
  
### Dashboard UI  
Check link: _https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/_  
      
## Project Idea; Raspberry Pi  
Check link: _https://blog.sicara.com/build-own-cloud-kubernetes-raspberry-pi-9e5a98741b49_  
  
## Prometheus monitoring  
Prometheus is a monitoring service which Kubernetes can integrate with. When using helm, one can install a full-house prometheus-kubernetes package with a single command.  
> helm install stable/prometheus-operator --name prometheus-operator --namespace monitoring  
  
The services it uses are:  
- Prometheus  
-- Setup Dashboard: kubectl port-forward -n monitoring prometheus-prometheus-operator-prometheus-0 9090  
-- Dashboard site: _http://localhost:9090_  
- Grafana  
-- Setup Dashboard: kubectl port-forward $(kubectl get  pods --selector=app=grafana -n  monitoring --output=jsonpath="{.items..metadata.name}") -n monitoring  3000  
-- Dashboard site: _http://localhost:3000_  
- Alertmanager  
-- Setup Dashboard: kubectl port-forward -n monitoring alertmanager-prometheus-operator-alertmanager-0 9093  
-- Dashboard site: _http://localhost:9093_  
  
For more information about prometheus and its connected services, you can look up the following site(s):  
- https://itnext.io/kubernetes-monitoring-with-prometheus-in-15-minutes-8e54d1de2e13  
  

