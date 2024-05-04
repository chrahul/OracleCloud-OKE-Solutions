**Prerequisites for Container Engine for Kubernetes**

Before utilizing Container Engine for Kubernetes to create a Kubernetes cluster, ensure the following prerequisites are met:

1. **Oracle Cloud Infrastructure Tenancy**: Access to an Oracle Cloud Infrastructure tenancy subscribed to regions where Container Engine for Kubernetes is available.

2. **Quotas**: Ensure adequate quotas for various resources:
   - Compute instance quota: Dependent on the selected shape and required compute cores and memory.
   - Block volume quota: Sufficient quota for persistent volume claims (minimum 50 GB).
   - Load balancer quota: If load balancers will be utilized.
   
3. **Compartment and Network Resources**: 
   - A compartment containing necessary network resources (VCN, subnets, internet gateway, route table, security lists).
   - Appropriately configured network resources within the compartment in each desired region.

4. **Network Configuration**: For high availability clusters, ensure appropriate configuration including:
   - Worker nodes: Regional subnet or availability domain-specific subnets.
   - Load balancers: Additional regional subnet or availability domain-specific subnets.
   - Utilize regional subnets for simpler failover across availability domains.

5. **Cluster Management Permissions**: Belong to either:
   - Tenancy's Administrators group.
   - A group with Container Engine for Kubernetes permissions granted via policy.

6. **Kubernetes Operations**:
   - Ability to run kubectl command-line tool.
   - Set up kubeconfig configuration file for cluster access.
   - Appropriate permissions to access the cluster.

**Availability by Region**: Container Engine for Kubernetes is available in all Oracle Cloud Infrastructure regions. Refer to official documentation for details.

**References**:
- Oracle Cloud Infrastructure Regions Documentation: [Link](https://docs.oracle.com/iaas/Content/General/Concepts/regions.htm)
- Container Engine for Kubernetes Prerequisites Documentation: [Link](https://docs.oracle.com/en-us/iaas/Content/ContEng/Concepts/contengprerequisites.htm#regional-availability)
- Oracle Cloud Infrastructure Service Limits Documentation: [Link](https://docs.oracle.com/iaas/Content/General/Concepts/servicelimits.htm#computelimits)
