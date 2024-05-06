Monitoring clusters in Container Engine for Kubernetes (OKE) is crucial for ensuring their health, capacity, and performance. Here's how you can monitor and observe various aspects of your clusters:

**Monitoring Clusters:**
- Open the navigation menu and navigate to Developer Services > Kubernetes Clusters (OKE).
- Choose the compartment where your clusters are located.
- On the Cluster List page, you can see the status of each cluster, including whether it's creating, active, failed, deleting, or deleted.
- Click on a cluster to view detailed status, metrics, and node pools information.
- Monitor node pools and nodes within the cluster to ensure they are running normally.
- Use the Metrics tab to view granular information about the health, capacity, and performance of the cluster.

**Viewing Container Engine for Kubernetes Service Logs:**
- Use Oracle Cloud Infrastructure Logging to view and search the logs of Kubernetes processes running on the control plane of clusters created with OKE.
- Logs include kube-scheduler, kube-controller-manager, cloud-controller-manager, and kube-apiserver logs.
- These logs are configured at default Kubernetes log level verbosity and contain information useful for troubleshooting cluster issues.

**Viewing Kubernetes API Server Audit Logs:**
- Use the Oracle Cloud Infrastructure Audit service to view operations performed by Container Engine for Kubernetes and the Kubernetes API server as log events.
- These logs help understand activities happening in a cluster, perform compliance checks, identify security anomalies, and troubleshoot errors.
- Operations performed by Container Engine for Kubernetes and the Kubernetes API server are logged as audit events.

Monitoring, logging, and auditing are essential components of managing Kubernetes clusters effectively. By utilizing these tools and features, you can ensure the reliability, security, and performance of your clusters in Container Engine for Kubernetes.
