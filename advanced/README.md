# Advanced Kubernetes Concepts

This section covers advanced and cluster-wide features for scaling, security, custom resources, and high availability.

## Must-Know Concepts
- **StatefulSet:** Manage stateful applications with stable identities and storage.
- **DaemonSet:** Run a pod on every node (e.g., for monitoring or logging).
- **Job & CronJob:** Run batch and scheduled tasks.
- **Ingress:** Expose HTTP/HTTPS services with advanced routing.
- **NetworkPolicy:** Secure pod-to-pod and pod-to-external communication.
- **PodDisruptionBudget (PDB):** Ensure high availability during voluntary disruptions.
- **ClusterRole & ClusterRoleBinding:** Grant cluster-wide or multi-namespace permissions.
- **ResourceQuota & LimitRange:** Enforce resource usage limits in namespaces.

## Good-to-Know Concepts
- **CustomResourceDefinition (CRD):** Extend Kubernetes with your own API objects.
- **Multi-Container Pod Patterns:** Use sidecar, ambassador, or adapter containers for advanced pod design.
- **PriorityClass:** Control pod scheduling and eviction priority.
- **Ephemeral Containers:** Debug running pods without restarting them.
- **TopologySpreadConstraints:** Distribute pods evenly across nodes or zones for resilience.

## Structure
Each subfolder contains:
- A README.md with explanations and exercises
- YAML manifests for hands-on practice

**Tip:** Master the must-know concepts for production-grade clusters. Explore the good-to-know features for advanced use cases, custom controllers, and high-availability architectures.
