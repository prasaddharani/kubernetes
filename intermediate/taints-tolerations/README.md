# Taints & Tolerations Example
Taints are applied to nodes and allow a node to repel a set of pods. Tolerations are applied to pods and allow (but do not require) the pods to schedule onto nodes with matching taints.

## Files
- `toleration-pod.yaml`: A pod with a toleration for a specific taint.

## Step-by-Step Exercise
1. **Add a taint to a node**
   ```sh
   kubectl taint nodes <node-name> key=value:NoSchedule
   ```
2. **Create the Pod with a matching toleration**
   ```sh
   kubectl apply -f toleration-pod.yaml
   ```
3. **Check the Pod's scheduling**
   ```sh
   kubectl get pods -o wide
   ```
4. **Remove the taint from the node (cleanup)**
   ```sh
   kubectl taint nodes <node-name> key:NoSchedule-
   ```
5. **Delete the Pod**
   ```sh
   kubectl delete -f toleration-pod.yaml
   ```

---

**Tip:** Taints and tolerations are useful for dedicating nodes to specific workloads or isolating critical applications.

