# ResourceQuota & LimitRange Example
ResourceQuota limits the total amount of resources (CPU, memory, objects) that can be used in a namespace. LimitRange sets default/min/max resource requests and limits for pods/containers in a namespace.

## Files
- `resourcequota.yaml`: Defines a ResourceQuota for a namespace.
- `limitrange.yaml`: Defines a LimitRange for a namespace.

## Step-by-Step Exercise
1. **Create a namespace for the example**
   ```sh
   kubectl create namespace quota-demo
   ```
2. **Apply the ResourceQuota**
   ```sh
   kubectl apply -f resourcequota.yaml -n quota-demo
   ```
3. **Apply the LimitRange**
   ```sh
   kubectl apply -f limitrange.yaml -n quota-demo
   ```
4. **Check the quotas and limits**
   ```sh
   kubectl get resourcequota -n quota-demo
   kubectl get limitrange -n quota-demo
   ```
5. **Delete the resources and namespace**
   ```sh
   kubectl delete -f resourcequota.yaml -n quota-demo
   kubectl delete -f limitrange.yaml -n quota-demo
   kubectl delete namespace quota-demo
   ```

---

**Tip:** Use ResourceQuota and LimitRange to enforce fair resource usage and prevent resource exhaustion in shared clusters.

