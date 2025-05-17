# Deployments

## Concept
A Deployment manages a ReplicaSet to keep a specified number of pods running. It supports rolling updates and rollbacks.

## Exercise
1. Apply the deployment.yaml manifest:
   ```sh
   kubectl apply -f deployment.yaml
   ```
2. Scale the deployment:
   ```sh
   kubectl scale deployment nginx-deployment --replicas=3
   ```
3. Update the image in deployment.yaml and re-apply to see a rolling update.
4. Delete the deployment:
   ```sh
   kubectl delete -f deployment.yaml
   ```

## deployment.yaml Example
A simple nginx deployment is provided in deployment.yaml.
