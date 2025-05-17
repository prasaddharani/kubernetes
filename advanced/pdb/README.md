# PodDisruptionBudget (PDB) Example
A PodDisruptionBudget (PDB) limits the number of pods of a replicated application that are down simultaneously from voluntary disruptions (like node drain or cluster upgrades).

## Files
- `pdb.yaml`: Defines a PDB for a deployment.
- `pdb-deployment.yaml`: A deployment managed by the PDB.

## Step-by-Step Exercise
1. **Create the Deployment**
   ```sh
   kubectl apply -f pdb-deployment.yaml
   ```
2. **Create the PodDisruptionBudget**
   ```sh
   kubectl apply -f pdb.yaml
   ```
3. **Check the PDB status**
   ```sh
   kubectl get pdb
   kubectl describe pdb demo-pdb
   ```
4. **Delete resources**
   ```sh
   kubectl delete -f pdb.yaml
   kubectl delete -f pdb-deployment.yaml
   ```

---

**Tip:** PDBs help ensure high availability during voluntary disruptions.

