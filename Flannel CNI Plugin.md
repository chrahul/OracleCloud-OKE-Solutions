Using the Flannel CNI Plugin for Pod Networking in OKE Clusters

1. **Overview:**
    - Flannel CNI plugin for pod communication on worker nodes in clusters created using Container Engine for Kubernetes (OKE).
    
2. **Flannel CNI Plugin:**
    - Provides pod networking without using IP addresses from a VCN's CIDR block.
    - Communication between pods is encapsulated in the flannel overlay network, a simple private overlay virtual network.
    - Satisfies the requirements of the Kubernetes networking model by attaching IP addresses to containers.
    - Pods in the private overlay network are only accessible from other pods in the same cluster.
    
3. **Flannel CIDR Block:**
    - Uses its own CIDR block to provision pods and worker nodes with IP addresses.
    - The default flannel CIDR block is large enough to support 65,534 pods and 512 worker nodes.
    - Can be increased in size to support many more.
    - The number of pods per worker node is not determined by the node shape.
    
4. **Compatibility and Usage:**
    - Can be used with managed node pools but not with virtual node pools.
    - Default CNI plugin for clusters created prior to July 2022 in OKE.
    - Can be selected during cluster creation using the 'Custom Create' workflow.
    - Still the default if using the API to create clusters.
    
5. **Additional Information:**
    - [Flannel Documentation](link-to-flannel-docs)
    - [OCI VCN-Native Pod Networking CNI Plugin Documentation](link-to-oci-docs)
