# Kubernetes Learning Repository

Welcome! This repository is a comprehensive, hands-on guide to learning Kubernetes from beginner to advanced concepts. It is organized by topic and difficulty, with practical YAML manifests and step-by-step exercises.

---

## What is Kubernetes?
Kubernetes (K8s) is an open-source platform for automating deployment, scaling, and management of containerized applications. It groups containers into logical units (pods) for easy management and discovery.

---

## Kubernetes Architecture (High-Level)
- **Master Node (Control Plane):**
  - **API Server:** Entry point for all REST commands.
  - **Controller Manager:** Governs controllers that regulate the state of the cluster.
  - **Scheduler:** Assigns pods to nodes.
  - **etcd:** Distributed key-value store for cluster data.
- **Worker Nodes:**
  - **kubelet:** Ensures containers are running in a pod.
  - **kube-proxy:** Handles networking and load balancing.
  - **Container Runtime:** (e.g., containerd, Docker) Runs containers.

---

## Folder Structure
- **beginner/**: Core concepts (pods, deployments, services, etc.)
- **intermediate/**: Storage, RBAC, probes, autoscaling, scheduling, etc.
- **advanced/**: StatefulSets, DaemonSets, Ingress, CRDs, quotas, advanced scheduling, etc.

Each folder contains:
- A README.md with explanations and exercises
- YAML manifests for hands-on practice

---

## Common kubectl Commands
- **Cluster Info & Nodes**
  - `kubectl cluster-info`
  - `kubectl get nodes`
- **Namespaces**
  - `kubectl get namespaces`
  - `kubectl create namespace <name>`
- **Pods**
  - `kubectl get pods`
  - `kubectl describe pod <pod-name>`
  - `kubectl logs <pod-name>`
  - `kubectl exec -it <pod-name> -- sh`
- **Deployments**
  - `kubectl get deployments`
  - `kubectl apply -f deployment.yaml`
  - `kubectl scale deployment <name> --replicas=3`
  - `kubectl rollout status deployment <name>`
- **Services**
  - `kubectl get svc`
  - `kubectl expose deployment <name> --port=80 --type=NodePort`
- **ConfigMaps & Secrets**
  - `kubectl get configmaps`
  - `kubectl get secrets`
- **Storage**
  - `kubectl get pv`
  - `kubectl get pvc`
- **RBAC**
  - `kubectl get serviceaccounts`
  - `kubectl get roles,rolebindings`
  - `kubectl get clusterroles,clusterrolebindings`
- **Scaling & Autoscaling**
  - `kubectl autoscale deployment <name> --min=2 --max=5 --cpu-percent=80`
- **Cleanup**
  - `kubectl delete -f <file-or-folder>`
  - `kubectl delete pod <pod-name>`

---

## How to Use This Repo
1. Start with the **beginner** folder and work your way up.
2. Read the README.md in each folder for explanations and exercises.
3. Apply YAML files using `kubectl apply -f <filename>`.
4. Clean up resources with `kubectl delete -f <filename>`.
5. Use the provided commands above for troubleshooting and exploration.

Happy learning!
