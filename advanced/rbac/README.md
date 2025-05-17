# ClusterRole & ClusterRoleBinding Example
ClusterRoles and ClusterRoleBindings are used for granting permissions cluster-wide or across multiple namespaces. This example shows how to grant read access to pods in all namespaces.

## Files
- `clusterrole.yaml`: Defines a ClusterRole with read access to pods.
- `clusterrolebinding.yaml`: Binds the ClusterRole to a ServiceAccount.
- `crb-serviceaccount.yaml`: A ServiceAccount to use with the binding.
- `crb-pod.yaml`: A pod using the ServiceAccount.

## Step-by-Step Exercise
1. **Create the ServiceAccount**
   ```sh
   kubectl apply -f crb-serviceaccount.yaml
   ```
2. **Create the ClusterRole**
   ```sh
   kubectl apply -f clusterrole.yaml
   ```
3. **Create the ClusterRoleBinding**
   ```sh
   kubectl apply -f clusterrolebinding.yaml
   ```
4. **Create the Pod using the ServiceAccount**
   ```sh
   kubectl apply -f crb-pod.yaml
   ```
5. **Check the ServiceAccount and permissions**
   ```sh
   kubectl get serviceaccounts
   kubectl get clusterrolebindings
   kubectl get pods
   ```
6. **Delete resources**
   ```sh
   kubectl delete -f crb-pod.yaml
   kubectl delete -f clusterrolebinding.yaml
   kubectl delete -f clusterrole.yaml
   kubectl delete -f crb-serviceaccount.yaml
   ```

---

**Tip:** ClusterRoles and ClusterRoleBindings are essential for cluster-wide access control and multi-namespace permissions.

