# Labels & Selectors Example
Labels are key/value pairs attached to objects. Selectors are used to filter resources by label. This is fundamental for grouping and managing Kubernetes resources.

## Files
- `label-pod.yaml`: A pod with custom labels.
- `label-selector-service.yaml`: A service that selects pods by label.

## Step-by-Step Exercise
1. **Create the Pod with labels**
   ```sh
   kubectl apply -f label-pod.yaml
   ```
2. **Create the Service with a selector**
   ```sh
   kubectl apply -f label-selector-service.yaml
   ```
3. **Check the Pod and Service**
   ```sh
   kubectl get pods --show-labels
   kubectl get svc
   ```
4. **Delete resources**
   ```sh
   kubectl delete -f label-selector-service.yaml
   kubectl delete -f label-pod.yaml
   ```

---

**Tip:** Labels and selectors are used everywhere in Kubernetes for grouping, selecting, and managing resources.

