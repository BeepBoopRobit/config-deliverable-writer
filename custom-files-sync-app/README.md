
### Step 1: Copy Configuration File
Copy the `custom-files-sync.yaml` configuration file to the appropriate TAP-GitOps directory for your cluster.

```bash
cp custom-files-sync.yaml tap-gitops/<cluster_name>/tanzu-sync/app/config/.tanzu-managed/
```

### Step 2: Create Custom Files Directory
Create a directory to store all your custom files. This directory will be used by the Custom File Sync app to synchronize files to your cluster.

```bash
mkdir -p tap-gitops/clusters/<cluster_name>/cluster-config/custom-files
```

### Step 3: Add Custom Files
Place all your custom configuration files into the newly created directory. Ensure that these files are organized in a way that aligns with your cluster's architecture and needs.

```plaintext
# Place all custom files in the directory
# Example: cp my-custom-config.yaml tap-gitops/clusters/<cluster_name>/cluster-config/custom-files/
```