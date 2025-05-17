# CustomResourceDefinition (CRD) Example
A CustomResourceDefinition (CRD) lets you extend Kubernetes with your own API objects. This example shows how to define a simple CRD and create a custom resource.

## Files
- `crd.yaml`: Defines a new custom resource type called `DemoResource`.
- `demo-resource.yaml`: An instance of the custom resource.

## Step-by-Step Exercise
1. **Create the CRD**
   ```sh
   kubectl apply -f crd.yaml
   ```
2. **Check the CRD**
   ```sh
   kubectl get crds
   ```
3. **Create a custom resource**
   ```sh
   kubectl apply -f demo-resource.yaml
   ```
4. **Check the custom resource**
   ```sh
   kubectl get demoresources
   ```
5. **Delete resources**
   ```sh
   kubectl delete -f demo-resource.yaml
   kubectl delete -f crd.yaml
   ```

---

**Tip:** CRDs are the foundation for building Kubernetes Operators and custom controllers.

