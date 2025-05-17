# Namespace Example
A Namespace is used to divide cluster resources between multiple users. It provides a scope for names and is useful for resource isolation.

## Files
- `namespace.yaml`: Defines a custom namespace called `demo-namespace`.

## Step-by-Step Exercise
1. **Create the Namespace**
   ```sh
   kubectl apply -f namespace.yaml
   ```
2. **Check the Namespace**
   ```sh
   kubectl get namespaces
   ```
3. **Create resources in the Namespace**
   Add `namespace: demo-namespace` under `metadata` in any resource YAML, or use `-n demo-namespace` with kubectl.
4. **Delete the Namespace**
   ```sh
   kubectl delete -f namespace.yaml
   ```

---

**Tip:** Namespaces are ideal for separating environments (dev, test, prod) or teams.

