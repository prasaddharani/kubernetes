# Job Example
A Job creates one or more pods and ensures that a specified number of them successfully complete. Jobs are useful for running batch or one-time tasks.

## Files
- `job.yaml`: Defines a Job that runs a simple calculation and then exits.

## Step-by-Step Exercise
1. **Create the Job**
   ```sh
   kubectl apply -f job.yaml
   ```
2. **Check the Job and pods**
   ```sh
   kubectl get jobs
   kubectl get pods -l job-name=pi-job
   ```
   Wait for the pod to complete (STATUS should be `Completed`).
3. **View the Job output**
   ```sh
   kubectl logs <pod-name>
   ```
   Replace `<pod-name>` with the actual pod name from the previous command.
4. **Delete the Job**
   ```sh
   kubectl delete -f job.yaml
   ```

---

**Tip:** Jobs are ideal for tasks that need to run to completion, such as data processing or database migrations.

