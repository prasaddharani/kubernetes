# Advanced Environment Variables Example
Kubernetes allows you to set environment variables in pods from various sources, such as fieldRef (pod fields), resourceFieldRef (resource limits/requests), and configMap/secret keys.

## Files
- `env-pod.yaml`: A pod demonstrating advanced environment variable sources.

## Step-by-Step Exercise
1. **Create the Pod with advanced environment variables**
   ```sh
   kubectl apply -f env-pod.yaml
   ```
2. **Check the environment variables inside the Pod**
   ```sh
   kubectl exec -it env-demo-pod -- printenv | grep K8S
   ```
3. **Delete the Pod**
   ```sh
   kubectl delete -f env-pod.yaml
   ```

---

**Tip:** Advanced environment variables are useful for injecting pod metadata or resource values into your containers.

