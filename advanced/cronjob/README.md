# CronJob Example
A CronJob creates Jobs on a repeating schedule. This is useful for periodic tasks such as backups, report generation, or scheduled cleanups.

## Files
- `cronjob.yaml`: Defines a CronJob that runs a simple command every minute.

## Step-by-Step Exercise
1. **Create the CronJob**
   ```sh
   kubectl apply -f cronjob.yaml
   ```
2. **Check the CronJob and Jobs**
   ```sh
   kubectl get cronjobs
   kubectl get jobs
   kubectl get pods
   ```
   You should see new Jobs and Pods created every minute.
3. **View the output of a Pod**
   ```sh
   kubectl logs <pod-name>
   ```
   Replace `<pod-name>` with the actual pod name from the previous command.
4. **Delete the CronJob**
   ```sh
   kubectl delete -f cronjob.yaml
   ```

---

**Tip:** CronJobs are ideal for automating recurring tasks in your cluster.

