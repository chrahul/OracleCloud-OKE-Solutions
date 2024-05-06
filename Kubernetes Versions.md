The Kubernetes versioning scheme follows the format x.y.z, where:
- **x** is the major version,
- **y** is the minor version, and
- **z** is the patch version.

For example, `1.29.1` denotes major version 1, minor version 29, and patch version 1.

**Support for Kubernetes Versions:**
- The Kubernetes project supports the three most recent minor versions.
- When creating a Kubernetes cluster with Container Engine for Kubernetes (OKE), you specify the Kubernetes versions for control plane nodes and worker nodes.
- Control plane nodes must run the same or up to two (or three, starting from Kubernetes v1.28) versions ahead of the worker nodes.
- Worker nodes can lag behind control plane nodes by up to two (or three, starting from Kubernetes v1.28) versions but cannot run a more recent version.
- This ensures compatibility between components across different nodes in the cluster.

**Minor Version Support:**
- Kubernetes minor versions introduce new features and improvements, released approximately three times a year.
- OKE supports three minor versions for new clusters.
- Support for the fourth oldest minor version continues for at least 30 days after support for a new version is announced.
- After this period, the fourth oldest version is no longer supported.
- It's recommended to upgrade existing clusters to a supported minor version before support for the older version ends.

**Patch Version Support:**
- Kubernetes patch versions address critical bugs or security vulnerabilities.
- Patch versions are released frequently, typically once a month.
- OKE validates and supports critical patch versions promptly.
- After announcing support for a new patch version, clusters running the corresponding minor version should be upgraded within 30 days.
- After this period, clusters running the older patch version are no longer supported.
- Although older patch versions may still be available for selection, it's advised to choose the latest patch version for security and stability.

By adhering to Kubernetes versioning and support policies, OKE ensures compatibility, stability, and security for Kubernetes clusters deployed on Oracle Cloud Infrastructure.
