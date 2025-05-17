# Services

## Concept
A Service exposes a set of pods as a network service. Types include ClusterIP, NodePort, and LoadBalancer.

## Exercise
1. Apply the service manifests:
   ```sh
   kubectl apply -f clusterip-service.yaml
   kubectl apply -f nodeport-service.yaml
   kubectl apply -f loadbalancer-service.yaml
   ```
2. Check services:
   ```sh
   kubectl get svc
   ```
3. Delete the services:
   ```sh
   kubectl delete -f clusterip-service.yaml
   kubectl delete -f nodeport-service.yaml
   kubectl delete -f loadbalancer-service.yaml
   ```

## Example YAMLs
- clusterip-service.yaml
- nodeport-service.yaml
- loadbalancer-service.yaml

