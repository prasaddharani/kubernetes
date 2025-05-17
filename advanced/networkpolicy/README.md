# NetworkPolicy Example
A NetworkPolicy controls the network access to and from Kubernetes pods. It lets you specify which pods can communicate with each other and with resources outside the cluster.

## Files
- `networkpolicy.yaml`: Defines a NetworkPolicy that allows ingress traffic to pods with the label `app=nginx` only from pods with the label `access=true`.

## Step-by-Step Exercise
1. **Create the NetworkPolicy**
   ```sh
   kubectl apply -f networkpolicy.yaml
   ```
2. **Check the NetworkPolicy**
   ```sh
   kubectl get networkpolicies
   ```
3. **Test the Policy**
   - Deploy test pods with and without the `access=true` label.
   - Try to access the `nginx` pod from both test pods to see the effect of the policy.
4. **Delete the NetworkPolicy**
   ```sh
   kubectl delete -f networkpolicy.yaml
   ```

---

**Tip:** NetworkPolicies are essential for securing communication between pods in production environments.

