# Vertical Pod Autoscaler Operator

## Usage

This is to deploy the [Vertical Pod Autoscaler Operator](https://docs.openshift.com/container-platform/latest/nodes/pods/nodes-pods-vertical-autoscaler.html) into an OpenShift 4.8 or later cluster.
Vertical Pod Autoscaler (VPA) can be configured to monitor a workload's resource utilization, and then adjust its CPU and memory resource requests by updating the pod (future) or restarting the pod with updated resource requests.

## Install Operator Only

Reference on of the `operator/overlay` directories.  For example:

```
oc apply -k vertical-pod-autoscaler-operator/operator/overlays/stable?ref=main
```

Or as part of your own `kustomization.yaml` file:

```
kind: Kustomization
apiVersion: kustomize.config.k8s.io/v1beta1

bases:
- github.com/redhat-cop/gitops-catalog/vertical-pod-autoscaler-operator/operator/overlays/stable?ref=main
```
