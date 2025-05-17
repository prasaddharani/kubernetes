# HorizontalPodAutoscaler (HPA) Example
The HorizontalPodAutoscaler automatically scales the number of pods in a deployment or replica set based on observed CPU utilization or other select metrics.

## Files
- `hpa-deployment.yaml`: A deployment to be autoscaled.
- `hpa.yaml`: An HPA resource that scales the deployment based on CPU usage.

## Step-by-Step Exercise
1. **Create the Deployment**
   ```sh
   kubectl apply -f hpa-deployment.yaml
   ```
2. **Create the HPA**
   ```sh
   kubectl apply -f hpa.yaml
   ```
3. **Check the HPA status**
   ```sh
   kubectl get hpa
   kubectl describe hpa hpa-demo
   ```
4. **(Optional) Generate load to see scaling**
   Use a load generator or `kubectl exec` into a pod and run a CPU-intensive command.
5. **Delete resources**
   ```sh
   kubectl delete -f hpa.yaml
   kubectl delete -f hpa-deployment.yaml
   ```

---

**Tip:** HPA is essential for automatically scaling your applications based on demand.

