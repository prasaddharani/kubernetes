# Ephemeral Containers Example
Ephemeral containers are special containers that can be added to running pods for debugging purposes. They are not part of the pod spec and are not restarted when they exit or crash.

## Files
- `ephemeral-demo-pod.yaml`: A pod to which you can add an ephemeral container.

## Step-by-Step Exercise
1. **Create the demo pod**
   ```sh
   kubectl apply -f ephemeral-demo-pod.yaml
   ```
2. **Add an ephemeral container for debugging**
   ```sh
   kubectl debug -it ephemeral-demo-pod --image=busybox --target=main
   ```
   This will start a shell in a new ephemeral container attached to the running pod.
3. **Check the ephemeral container**
   ```sh
   kubectl describe pod ephemeral-demo-pod
   ```
4. **Delete the pod**
   ```sh
   kubectl delete -f ephemeral-demo-pod.yaml
   ```

---

**Tip:** Ephemeral containers are useful for troubleshooting running pods without restarting them.

