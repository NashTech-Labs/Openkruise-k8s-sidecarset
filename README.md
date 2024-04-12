# Openkruise-k8s-sidecarset
SidecarSet is a part of Advanced Workloads in Openkruise for Kubernetes.
This enables the injection of a sidecar container on the pod during scheduling. We do not need to define a sidecar container in the pod definition yaml. It will get attached to the pod by using selectors and matchlabeles.


## Using sidecarset
1. Copy the yaml  

2. Apply the yaml  
```bash 
kubectl apply -f sidecarset.yaml
```
3. Create a pod with matching labels
```bash
kubectl apply -f pod.yaml
```
4. Check the numer of containers in a pod.
```bash
kuebctl get po 
```

You will see that two containers are running in the pod. This is because the sidecar container got injected during the pod creation.