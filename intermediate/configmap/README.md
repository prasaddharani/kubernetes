# ConfigMap Example
A ConfigMap is used to store non-sensitive configuration data as key-value pairs. This folder demonstrates how to create a ConfigMap and use it in a Deployment.

## Files
- `configmap.yaml`: Defines a ConfigMap with a sample environment variable.
- `deployment.yaml`: Deploys a pod that uses the ConfigMap as an environment variable.

## Step-by-Step Exercise
1. **Create the ConfigMap**
   ```sh
   kubectl apply -f configmap.yaml
   ```
2. **Deploy the Pod using the ConfigMap**
   ```sh
   kubectl apply -f deployment.yaml
   ```
3. **Verify the Pod is running**
   ```sh
   kubectl get pods
   ```
4. **Check the environment variable inside the Pod**
   ```sh
   kubectl exec -it <pod-name> -- printenv | grep DEMO_ENV
   ```
   You should see: `DEMO_ENV=This is a demo config value from ConfigMap!`
5. **Clean up**
   ```sh
   kubectl delete -f deployment.yaml
   kubectl delete -f configmap.yaml
   ```

---

**Tip:** Replace `<pod-name>` with the actual pod name from `kubectl get pods`.

