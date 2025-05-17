# PriorityClass Example
PriorityClass allows you to assign priorities to pods. Pods with higher priority are scheduled first and are less likely to be evicted in case of resource pressure.

## Files
- `priorityclass.yaml`: Defines a custom PriorityClass.
- `priority-pod.yaml`: A pod using the custom PriorityClass.

## Step-by-Step Exercise
1. **Create the PriorityClass**
   ```sh
   kubectl apply -f priorityclass.yaml
   ```
2. **Create the Pod with the custom PriorityClass**
   ```sh
   kubectl apply -f priority-pod.yaml
   ```
3. **Check the Pod's priority**
   ```sh
   kubectl get pod priority-demo-pod -o jsonpath='{.spec.priorityClassName}'
   ```
4. **Delete the Pod and PriorityClass**
   ```sh
   kubectl delete -f priority-pod.yaml
   kubectl delete -f priorityclass.yaml
   ```

---

**Tip:** Use PriorityClass to ensure critical workloads are scheduled and protected from eviction before lower-priority pods.

