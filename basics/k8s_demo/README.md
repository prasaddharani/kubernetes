# Kubernetes Demo

This project demonstrates basic Kubernetes concepts using NGINX, including Pods, Deployments, and different types of Services (ClusterIP, NodePort, LoadBalancer).

## Files

- [`pod.yaml`](k8s_demo/pod.yaml): Defines a single NGINX Pod.
- [`deployment.yaml`](k8s_demo/deployment.yaml): Defines a Deployment with 2 NGINX replicas.
- [`clusterip-service.yaml`](k8s_demo/clusterip-service.yaml): Exposes the Deployment internally using a ClusterIP Service.
- [`nodeport-service.yaml`](k8s_demo/nodeport-service.yaml): Exposes the Deployment on a static port on each Node using a NodePort Service.
- [`loadbalancer-service.yaml`](k8s_demo/loadbalancer-service.yaml): Exposes the Deployment externally using a LoadBalancer Service (for supported cloud providers).

## Definitions

- **Pod**: The smallest deployable unit in Kubernetes, representing a single instance of a running process.
- **Deployment**: Manages a set of identical Pods, ensuring the desired number are running and updating them as needed.
- **Service**: An abstraction that defines a logical set of Pods and a policy by which to access them.
  - **ClusterIP**: Exposes the Service on an internal IP in the cluster (default).
  - **NodePort**: Exposes the Service on a static port on each Node’s IP.
  - **LoadBalancer**: Exposes the Service externally using a cloud provider’s load balancer.

## Usage

Apply each resource using `kubectl`:

```sh
# Create a Pod
kubectl apply -f pod.yaml

# Create a Deployment
kubectl apply -f deployment.yaml

# Expose Deployment with ClusterIP Service
kubectl apply -f clusterip-service.yaml

# Expose Deployment with NodePort Service
kubectl apply -f nodeport-service.yaml

# Expose Deployment with LoadBalancer Service
kubectl apply -f loadbalancer-service.yaml
```

## Accessing the Application

- **ClusterIP**: Accessible only within the cluster.
- **NodePort**: Accessible via `<NodeIP>:<NodePort>`, e.g., `http://localhost:30007` if running locally with Minikube or Docker Desktop.
- **LoadBalancer**: Accessible via the external IP assigned by your cloud provider.

## Clean Up

To delete all resources:

```sh
kubectl delete -f .
```

---

For more information, see the [Kubernetes documentation](https://kubernetes.io/docs/home/).