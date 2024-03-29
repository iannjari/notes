# k8s
Deployment -> abstraction over pod

minikube -> ochestrates a kubernetes cluster on a single (mostly local machine), requires a VM locally (docker runtime is sufficient), start a minikube session with `minikube start`

## common commands
`kubectl create deployment deployment_name --image=image_to_use`

`kubectl get pod`

`kubectl get replicaset`

`kubectl get services`

`kubectl edit deployment [name]`

`kubectl logs pod_name`

`kubectl describe pod pod_name`

`kubectl exec -it deployment_name -- bin/bash` - get an interactive shell of a container in a pod

`kubectl delete deployment deployment_name`

`kubectl apply -f filename` - use a manifest file to manage a cluster

`minikube image load image_name` - load an image from local docker runtime into minikube

`minikube service service_name`  assign an external IP to a service whose Ext IP status is `<pending>` (minikube does not assign an IP address to a service)

`kubectl api-resources --namespaced=true/false`

## namespaces
- Volumes and nodes are namespace-agnostic.
- ConfigMaps, Secrets are not accessible from another namespace. (`kubectl api-resources --namespaced=true/false`)
