# StatefulSet Example
A StatefulSet is used to manage stateful applications. It provides each pod with a unique, stable identity and stable storage. This is useful for databases and other applications that need stable network identities and persistent storage.

## Files
- `statefulset.yaml`: Defines a StatefulSet with two nginx pods, each with its own persistent volume.

## Step-by-Step Exercise
1. **Create the StatefulSet**
   ```sh
   kubectl apply -f statefulset.yaml
   ```
2. **Check the StatefulSet and pods**
   ```sh
   kubectl get statefulsets
   kubectl get pods -l app=nginx-stateful
   ```
   You should see pods named `nginx-stateful-0`, `nginx-stateful-1`, etc.
3. **Check the persistent volume claims (PVCs)**
   ```sh
   kubectl get pvc
   ```
   Each pod will have its own PVC.
4. **Delete the StatefulSet**
   ```sh
   kubectl delete -f statefulset.yaml
   ```
   PVCs may remain after deletion for data safety.

---

**Tip:** StatefulSets are ideal for databases and clustered applications that need stable identities and storage.

