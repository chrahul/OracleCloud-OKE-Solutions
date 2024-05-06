**Prerequisites for Creating an OKE Cluster**

In this lesson, we'll cover the fundamental prerequisites necessary to create an OKE (Oracle Kubernetes Engine) cluster.

**1. Access to Oracle Cloud Infrastructure Tenancy:**
   - Access to an Oracle Cloud Infrastructure (OCI) tenancy, which serves as your Oracle Cloud account.
   - OKE is available in all OCI regions, providing flexibility regardless of your location.

**2. Sufficient Quotas on Resources:**
   - Ensure adequate quotas on various resource types:
     - Compute instance quota: Determined by compute cores and memory required for specific shapes.
     - Block volume quota: Necessary for creating Kubernetes persistent volumes.
     - Load balancer quota: Required if creating load balancers for distributing traffic.
   - Quota requirements vary based on cluster configuration and workload demands.

**3. Dedicated Compartment:**
   - Prepare a dedicated compartment within your tenancy for deployment.
   - This compartment will house essential network resources such as VCN, subnets, internet gateways, route tables, and security lists.

**4. Configured Network Resources:**
   - Properly configure network resources within the compartment.
   - Components include VCN, subnets, internet gateways, route tables, and security lists.
   - Best practice: Opt for regional subnets to simplify failover across availability domains.

**5. Understanding Policies:**
   - Belong to a group with necessary permissions:
     - Tenancy administrators group: Grants administrative permissions for managing OKE.
     - Groups with policies granting OKE permissions: Provides access to specific OKE functionalities.
   - Policies are crucial for managing permissions effectively.

**6. Kubernetes Operations:**
   - Possess the Kubernetes command-line tool, kubectl, for performing operations on clusters.
     - Can use CloudShell's included installation or set up a local installation.
   - Configure your own kubeconfig file for cluster access, ensuring each user has their own file.
   - Kubeconfig setup is essential for cluster access and cannot be shared among users.

By ensuring these prerequisites are met, you lay a solid foundation for creating and managing OKE clusters effectively. Each aspect plays a crucial role in the successful deployment and operation of Kubernetes clusters on OCI.

Reference: [Oracle Container Engine for Kubernetes - Prerequisites](https://docs.oracle.com/en-us/iaas/Content/ContEng/Concepts/contengprerequisites.htm)
