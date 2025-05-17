# DaemonSet Example
A DaemonSet ensures that a copy of a specific pod runs on all (or some) nodes in the cluster. This is useful for running node-level agents like log collectors or monitoring daemons.

## Files
- `daemonset.yaml`: Defines a DaemonSet that runs a busybox pod on every node.

## Step-by-Step Exercise
1. **Create the DaemonSet**
   ```sh
   kubectl apply -f daemonset.yaml
   ```
2. **Check the DaemonSet and pods**
   ```sh
   kubectl get daemonsets
   kubectl get pods -l app=daemon-demo -o wide
   ```
   You should see one pod per node.
3. **Delete the DaemonSet**
   ```sh
   kubectl delete -f daemonset.yaml
   ```

---

**Tip:** DaemonSets are ideal for background tasks that must run on every node, such as log shippers or monitoring agents.

