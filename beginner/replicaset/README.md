# ReplicaSet Example
A ReplicaSet ensures that a specified number of pod replicas are running at any given time. It is often used by Deployments, but can be managed directly.

## Files
- `replicaset.yaml`: Defines a ReplicaSet that manages 2 nginx pods.

## Step-by-Step Exercise
1. **Create the ReplicaSet**
   ```sh
   kubectl apply -f replicaset.yaml
   ```
2. **Check the ReplicaSet and pods**
   ```sh
   kubectl get replicasets
   kubectl get pods -l app=nginx-replicaset
   ```
3. **Scale the ReplicaSet**
   ```sh
   kubectl scale replicaset nginx-replicaset --replicas=3
   ```
4. **Delete the ReplicaSet**
   ```sh
   kubectl delete -f replicaset.yaml
   ```

---

**Tip:** ReplicaSets are rarely used directly, but understanding them helps you understand how Deployments work under the hood.

