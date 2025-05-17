# Ingress Example
An Ingress exposes HTTP and HTTPS routes from outside the cluster to services within the cluster. It provides advanced routing, SSL termination, and virtual hosting.

## Files
- `ingress.yaml`: Defines an Ingress that routes traffic to the `nginx-clusterip` service.

## Step-by-Step Exercise
1. **Prerequisite:** Ensure you have an Ingress controller running in your cluster (e.g., NGINX Ingress Controller).
2. **Create the Ingress**
   ```sh
   kubectl apply -f ingress.yaml
   ```
3. **Check the Ingress**
   ```sh
   kubectl get ingress
   ```
   You should see an address assigned to the Ingress.
4. **Test the Ingress**
   - Add an entry to your `/etc/hosts` file (or Windows equivalent) to map `example.local` to your cluster's Ingress IP.
   - Access `http://example.local/` in your browser or with `curl`.
5. **Delete the Ingress**
   ```sh
   kubectl delete -f ingress.yaml
   ```

---

**Tip:** Ingress is ideal for exposing multiple services under the same IP and managing external access to your cluster.

