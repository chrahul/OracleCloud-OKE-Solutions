Setting up storage for Kubernetes clusters in Container Engine for Kubernetes (OKE) involves defining and applying persistent volume claims (PVCs). With Oracle Cloud Infrastructure (OCI) as the underlying provider, you can provision PVCs by attaching volumes from the Block Volume service or by mounting file systems from the File Storage service.

**Persistent Volume (PV) and Persistent Volume Claim (PVC):**
- A PV offers persistent storage outside of containers, ensuring data integrity even if containers are terminated.
- A PVC is a request for storage, which is fulfilled by binding the PVC to a PV, providing an abstraction layer to the underlying storage.

**Provisioning PVCs:**
1. **Block Volume Service:**
   - Attach volumes from the OCI Block Volume service to clusters using CSI (Container Storage Interface) or FlexVolume volume plugins.
   - Oracle recommends the CSI volume plugin, as the FlexVolume plugin is deprecated in Kubernetes v1.23.
   - This method allows for durable storage by connecting volumes to managed or self-managed nodes.
   - Oracle automatically encrypts customer data at rest in persistent storage.

2. **File Storage Service:**
   - Mount file systems from the OCI File Storage service inside containers using a CSI volume plugin.
   - This approach enables mounting file systems into containers running on managed or self-managed nodes.
   - Oracle's default encryption ensures data security without any additional configuration.

**Note:** 
- This setup applies to managed node pools and managed/self-managed nodes, excluding virtual node pools and virtual nodes.
- Containers on virtual nodes cannot access persistent storage.

By leveraging PVCs and OCI's storage services, you can ensure data durability and reliability for your Kubernetes clusters in OKE, facilitating seamless data management and application deployment.
