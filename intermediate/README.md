# Intermediate Kubernetes Concepts

This section covers core features for running production workloads and managing configuration, storage, security, and scheduling.

## Must-Know Concepts
- **ConfigMap & Secret:** Manage configuration and sensitive data for your applications.
- **PersistentVolume (PV) & PersistentVolumeClaim (PVC):** Provide and claim persistent storage for pods.
- **Resource Requests & Limits:** Control CPU and memory usage for containers.
- **RBAC (ServiceAccount, Role, RoleBinding):** Secure your cluster with role-based access control.
- **Liveness & Readiness Probes:** Monitor and manage pod health and availability.
- **HorizontalPodAutoscaler (HPA):** Automatically scale pods based on resource usage.

## Good-to-Know Concepts
- **Advanced Environment Variables:** Inject pod metadata and resource values into containers.
- **Init Containers:** Run setup tasks before main containers start.
- **Affinity/Anti-Affinity:** Influence pod scheduling for high availability or co-location.
- **Taints & Tolerations:** Control which pods can be scheduled on which nodes.

## Structure
Each subfolder contains:
- A README.md with explanations and exercises
- YAML manifests for hands-on practice

**Tip:** Focus on mastering ConfigMaps, Secrets, storage, RBAC, and probes. These are critical for real-world Kubernetes usage. Explore the rest for advanced scheduling and configuration control.
