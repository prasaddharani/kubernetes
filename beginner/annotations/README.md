# Annotations Example
Annotations are key/value pairs used to attach arbitrary non-identifying metadata to objects. Unlike labels, annotations are not used to select and group objects.

## Files
- `annotation-pod.yaml`: A pod with custom annotations.

## Step-by-Step Exercise
1. **Create the Pod with annotations**
   ```sh
   kubectl apply -f annotation-pod.yaml
   ```
2. **Check the Pod and its annotations**
   ```sh
   kubectl get pod annotation-demo-pod -o yaml | grep annotations -A 5
   ```
3. **Delete the Pod**
   ```sh
   kubectl delete -f annotation-pod.yaml
   ```

---

**Tip:** Annotations are useful for attaching build info, contact info, or any custom metadata to resources.

