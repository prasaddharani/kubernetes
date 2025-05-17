# Affinity & Anti-Affinity Example
Pod affinity and anti-affinity allow you to control how pods are scheduled relative to other pods. Affinity attracts pods to run together, while anti-affinity keeps them apart.

## Files
- `affinity-pod.yaml`: A pod with affinity and anti-affinity rules.

## Step-by-Step Exercise
1. **Create the Pod with affinity/anti-affinity**
   ```sh
   kubectl apply -f affinity-pod.yaml
   ```
2. **Check the Pod's scheduling**
   ```sh
   kubectl get pods -o wide
   ```
3. **Delete the Pod**
   ```sh
   kubectl delete -f affinity-pod.yaml
   ```

---

**Tip:** Use affinity to co-locate pods for performance, and anti-affinity to spread pods for high availability.

