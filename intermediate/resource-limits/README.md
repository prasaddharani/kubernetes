# Resource Requests & Limits Example
Resource requests and limits allow you to control how much CPU and memory a container can use. Requests are the minimum guaranteed resources, and limits are the maximum allowed.

## Files
- `resource-limits-pod.yaml`: A pod with CPU and memory requests and limits set.

## Step-by-Step Exercise
1. **Create the Pod with resource requests and limits**
   ```sh
   kubectl apply -f resource-limits-pod.yaml
   ```
2. **Check the Pod's resource settings**
   ```sh
   kubectl get pod resource-limits-demo -o yaml | grep resources -A 6
   ```
3. **Delete the Pod**
   ```sh
   kubectl delete -f resource-limits-pod.yaml
   ```

---

**Tip:** Setting requests and limits helps ensure fair resource sharing and prevents a single pod from overusing cluster resources.

