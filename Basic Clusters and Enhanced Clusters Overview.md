**Basic Clusters and Enhanced Clusters Overview**

In alignment with ongoing enhancements to the OKE service, when creating a new cluster with Container Engine for Kubernetes, you specify the cluster type as one of the following:

1. **Basic Clusters:**
   - Support all core functionality provided by Kubernetes and Container Engine for Kubernetes.
   - Come with a service level objective but not a financially backed service level agreement (SLA).
   - Oracle guarantees a certain level of availability, but there's no monetary compensation if that level isn't met.

2. **Enhanced Clusters:**
   - Support all available features, including those not supported by basic clusters.
   - Offer advanced functionalities to simplify cluster management and enhance security.

**Features Supported by Enhanced Clusters:**

1. **Virtual Nodes:**
   - Simplify infrastructure management by removing the burden of manual scaling, upgrading, or troubleshooting worker nodes.
   - Ideal for managing large clusters with frequent updates or scaling requirements.

2. **Granular Cluster Add-on Management:**
   - Deploy and configure add-ons such as CoreDNS and kube-proxy in a more granular manner.
   - Complete control over add-ons installation, version selection, and automatic updates.

3. **Scalability:**
   - Provision more worker nodes in a single cluster to deploy larger workloads.
   - Better resource utilization and lower operational overhead.

4. **Workload Identity for Enhanced Security:**
   - Strengthen cluster security through workload identity.
   - Define OCI IAM policies to authorize specific ports for OCI API calls and resource access.

5. **Financially Backed SLA for Kubernetes API Server Uptime:**
   - Expect a certain level of uptime and availability for the Kubernetes API server.
   - Receive compensation if uptime degrades below the stated SLA.

**Notable Features Not Supported by Basic Clusters:**
- Virtual node pools
- Fine-grained cluster add-on deployment and configuration
- Workload identity for enhanced security
- Increased numbers of worker nodes
- Financially backed SLA

**Points to Remember:**
- When using the console, a new cluster is created as an enhanced cluster by default.
- When using CLI or API, you can specify the cluster type (basic or enhanced).
- Creating a new cluster as an enhanced cluster enables adding enhanced features later.
- Upgrading a basic cluster to an enhanced cluster is possible, but downgrading is not allowed.

**Conclusion:**
- Basic clusters provide core functionality, while enhanced clusters offer additional features and a financially backed SLA.
- When creating a cluster, choose between basic and enhanced clusters based on your requirements and preferences.
