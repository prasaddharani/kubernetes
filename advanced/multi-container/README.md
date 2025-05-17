# Multi-Container Pod Patterns Example
Kubernetes allows you to run multiple containers in a single pod. Common patterns include sidecar, ambassador, and adapter. This example demonstrates a sidecar pattern.

## Files
- `sidecar-pod.yaml`: A pod with an app container and a sidecar container.

## Step-by-Step Exercise
1. **Create the Pod with a sidecar**
   ```sh
   kubectl apply -f sidecar-pod.yaml
   ```
2. **Check the Pod and containers**
   ```sh
   kubectl get pods
   kubectl describe pod sidecar-demo-pod
   ```
3. **Delete the Pod**
   ```sh
   kubectl delete -f sidecar-pod.yaml
   ```

---

**Tip:** Sidecar containers are often used for logging, monitoring, or proxying traffic for the main app container.

