# PersistentVolume & PersistentVolumeClaim Example
A PersistentVolume (PV) is a piece of storage in the cluster. A PersistentVolumeClaim (PVC) is a request for storage by a user. Together, they allow pods to use persistent storage.

## Files
- `pv.yaml`: Defines a PersistentVolume.
- `pvc.yaml`: Defines a PersistentVolumeClaim.
- `pv-pod.yaml`: A pod that uses the PVC for storage.

## Step-by-Step Exercise
1. **Create the PersistentVolume**
   ```sh
   kubectl apply -f pv.yaml
   ```
2. **Create the PersistentVolumeClaim**
   ```sh
   kubectl apply -f pvc.yaml
   ```
3. **Create the Pod that uses the PVC**
   ```sh
   kubectl apply -f pv-pod.yaml
   ```
4. **Check the resources**
   ```sh
   kubectl get pv
   kubectl get pvc
   kubectl get pods
   ```
5. **Delete resources**
   ```sh
   kubectl delete -f pv-pod.yaml
   kubectl delete -f pvc.yaml
   kubectl delete -f pv.yaml
   ```

---

**Tip:** PVs and PVCs are essential for stateful applications that need to store data beyond the pod lifecycle.

