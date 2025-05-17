# TopologySpreadConstraints Example
TopologySpreadConstraints help you control how pods are distributed across your cluster's topology (such as nodes or zones) for high availability and fault tolerance.

## Files
- `topologyspread-pod.yaml`: A deployment with topology spread constraints.

## Step-by-Step Exercise
1. **Create the deployment with topology spread constraints**
   ```sh
   kubectl apply -f topologyspread-pod.yaml
   ```
2. **Check the pod distribution**
   ```sh
   kubectl get pods -o wide
   ```
3. **Delete the deployment**
   ```sh
   kubectl delete -f topologyspread-pod.yaml
   ```

---

**Tip:** Use topology spread constraints to ensure your pods are evenly distributed for resilience and availability.

