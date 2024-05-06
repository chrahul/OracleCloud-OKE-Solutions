**Supported Images and Shapes for Worker Nodes in OKE**


**Customization of Worker Nodes:**
- When creating a cluster in Container Engine for Kubernetes (OKE), you can customize worker nodes by selecting the operating system image and the shape.
- Operating system image serves as a template for the worker node's virtual hard drive and determines the installed OS and software.
- Shape defines the CPU and memory allocation for each instance, ensuring it meets specific requirements.
- Customization can be done via the console or REST API, providing flexibility for development teams.

**Supported Images for Managed Nodes:**
- OKE supports provisioning of managed nodes using Oracle Linux images provided by OCI, categorized into platform images, OKE images, and custom images.
- Platform images, exclusively containing Oracle Linux OS, are provided by Oracle and are downloaded, installed, and configured by OKE during node boot-up.
- OKE images, optimized for managed nodes, reduce provisioning time significantly compared to platform images.
- OKE image names follow a specific format, including the platform image name, "OKE," Kubernetes version, and OKE build number.

**Custom Images:**
- Custom images allow flexibility to design worker node images based on supported platform or OKE images, incorporating additional customizations and software.
- Custom images must be based on Oracle Linux images returned by the OCI CLI command "oci ce node-pool-options get."
- Provisioning managed nodes using custom images requires CLI or API, specifying the OCI ID of the custom image.

**Supported Shapes for Managed Nodes:**
- Managed nodes support various shapes including flexible, bare metal, HPC, and VM shapes.
- However, certain shapes like dedicated VM host, micro VM, and specific HPC shapes are not supported for managed nodes.

**Supported Shapes for Virtual Nodes:**
- Virtual nodes offer flexibility in managing Kubernetes clusters and support specific shapes like Pod.Standard.A1.Flex, Pod.Standard.E3.Flex, and Pod.Standard.E4.Flex.
- Other shapes are not supported for virtual nodes, ensuring optimal operation.

**Checking Supported Shapes:**
- To check supported shapes, including options for virtual nodes, execute the command "oci ce node-pool-options get --node-pool-options-id all" and review the response.

**Conclusion:**
- The customization of worker nodes, explored image options, and outlined supported shapes for managed and virtual nodes in OKE. Choosing the right combination of image and shape is crucial for optimal performance and resource allocation.
