# descheduler-v125
Manifests used to install descheduler v1.25 on k8s version v1.25

## Quick Start

The descheduler can be run as a `CronJob`, or `Deployment` inside of a k8s cluster. It has the
advantage of being able to be run multiple times without needing user intervention.
The descheduler pod is run as a critical pod in the `kube-system` namespace to avoid
being evicted by itself or by the kubelet.

### Run As A CronJob

```
kubectl create -f base/rbac.yaml
kubectl create -f base/configmap.yaml
kubectl create -f cronjob/cronjob.yaml
```

### Run As A Deployment

```
kubectl create -f base/rbac.yaml
kubectl create -f base/configmap.yaml
kubectl create -f deployment/deployment.yaml
```
