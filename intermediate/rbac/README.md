# RBAC Basics Example
Kubernetes RBAC (Role-Based Access Control) lets you control who can do what in your cluster. ServiceAccounts are used by pods, and Roles/RoleBindings grant permissions within a namespace.

## Files
- `serviceaccount.yaml`: Creates a ServiceAccount.
- `role.yaml`: Grants read access to pods in a namespace.
- `rolebinding.yaml`: Binds the Role to the ServiceAccount.
- `rbac-pod.yaml`: A pod that uses the ServiceAccount.

## Step-by-Step Exercise
1. **Create the ServiceAccount**
   ```sh
   kubectl apply -f serviceaccount.yaml
   ```
2. **Create the Role**
   ```sh
   kubectl apply -f role.yaml
   ```
3. **Create the RoleBinding**
   ```sh
   kubectl apply -f rolebinding.yaml
   ```
4. **Create the Pod using the ServiceAccount**
   ```sh
   kubectl apply -f rbac-pod.yaml
   ```
5. **Check the ServiceAccount and permissions**
   ```sh
   kubectl get serviceaccounts
   kubectl get rolebindings
   kubectl get pods
   ```
6. **Delete resources**
   ```sh
   kubectl delete -f rbac-pod.yaml
   kubectl delete -f rolebinding.yaml
   kubectl delete -f role.yaml
   kubectl delete -f serviceaccount.yaml
   ```

---

**Tip:** RBAC is essential for securing your cluster and following the principle of least privilege.

