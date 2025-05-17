# Pods

## Concept
A Pod is the smallest deployable unit in Kubernetes. It can contain one or more containers.

## Exercise
1. Apply the pod.yaml manifest:
   ```sh
   kubectl apply -f pod.yaml
   ```
2. Check pod status:
   ```sh
   kubectl get pods
   ```
3. Delete the pod:
   ```sh
   kubectl delete -f pod.yaml
   ```

## pod.yaml Example
A simple nginx pod is provided in pod.yaml.
