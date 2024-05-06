Working with self-managed nodes in Container Engine for Kubernetes (OKE) allows you to host worker nodes on compute instances that you've created yourself in the Compute service, rather than using instances provisioned by OKE. Here's how to set up and use self-managed nodes:

**1. Creating Compute Instances for Self-Managed Nodes:**
   - Use the Compute service to create compute instances to host self-managed nodes.
   - Configure compute instances for specialized workloads, such as GPU shapes or high-performance computing (HPC) shapes.
   - Optionally, create a compute instance pool to manage multiple self-managed nodes as a group.

**2. Adding Self-Managed Nodes to an OKE Cluster:**
   - Create a dynamic group and a policy to allow members of the dynamic group to join the cluster.
   - Prepare a cloud-init script containing the cluster's Kubernetes API private endpoint and base64-encoded CA certificate.
   - When creating the compute instance, provide the cloud-init script to add it to the OKE cluster as a self-managed node.

**3. Managing Self-Managed Nodes:**
   - If you delete the OKE cluster, the compute instances hosting self-managed nodes are not terminated automatically. You must terminate them manually.
   - To upgrade the version of Kubernetes running on a self-managed node, replace the existing node with a new one.

**4. Using Self-Managed Nodes with Cluster Networks:**
   - Create a compute instance pool to host self-managed nodes, which can be managed as an Oracle Cloud Infrastructure cluster network.
   - Compute instances within the cluster network are connected by a high-bandwidth, ultra-low-latency RDMA network.

**Notable Features and Capabilities:**
   - Self-managed node metrics are not shown on the Container Engine for Kubernetes Metrics page in the Console. Use kubectl to view Kubernetes metrics for self-managed nodes.
   - Currently, only OKE OL7 and OL8 images are supported for self-managed nodes.
   - Kubernetes skew policy enforcement, Kubernetes Cluster Autoscaler, VCN-native pod networking, and Container Engine for Kubernetes cordon and drain options are not yet available for self-managed nodes.
   - Node cycling during upgrades or updates is also not yet available.

By leveraging self-managed nodes, you gain flexibility in configuring compute instances for specialized workloads and managing them according to your specific requirements within an OKE cluster.
