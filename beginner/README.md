# Beginner Kubernetes Concepts

This section covers the foundational Kubernetes concepts. Mastering these is essential for anyone starting with Kubernetes.

## Must-Know Concepts
- **Pods:** The smallest deployable unit in Kubernetes, representing a single instance of a running process.
- **Deployments:** Manage stateless applications, handle scaling, rolling updates, and rollbacks.
- **ReplicaSet:** Ensures a specified number of pod replicas are running at all times.
- **Services:** Expose your applications as network services (ClusterIP, NodePort, LoadBalancer).
- **Namespace:** Provides resource isolation and organization within a cluster.
- **Labels & Selectors:** Attach metadata to objects and select groups of resources for management.

## Good-to-Know Concepts
- **Annotations:** Attach arbitrary metadata to objects for tools and libraries.

## Structure
Each subfolder contains:
- A README.md with explanations and exercises
- YAML manifests for hands-on practice

**Tip:** Start with Pods and Deployments, then move to Services, ReplicaSets, and Namespaces. Labels/Selectors and Annotations are used throughout Kubernetes and are fundamental for resource management.
