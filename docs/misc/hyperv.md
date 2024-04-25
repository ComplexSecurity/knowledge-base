Hyper-V is a virtualization platform developed by Microsoft. It allows users to create and manage [[Virtual Machines|virtual machines]] (VMs) on a Windows-based system. Originally released alongside Windows Server 2008, it's also available on Windows 10 and later versions, enabling both server and desktop users to utilize virtualization technologies.

Hyper-V uses hardware virtualization to efficiently run multiple operating systems as VMs on a single physical server or computer. It supports various guest operating systems, including Windows, Linux, and others, allowing them to run concurrently on a single hardware platform. Each VM operates in isolation with its own resources (CPU, memory, storage, and networking), which can be adjusted based on workload requirements.

Hyper-V provides the capability to take snapshots of VMs, allowing users to easily save the current state of a VM and revert back to it if needed. In a server environment, Hyper-V supports live migration of VMs from one host to another without downtime, enabling flexibility and improving fault tolerance.

Hyper-V is tightly integrated with other Microsoft products and services, such as [[Azure]] for cloud-based scenarios, System Center for management, and Windows Admin Center. Hyper-V is designed to scale from small environments (like a local development setup) to large data centers, offering robust performance features.

Hyper-V requires a 64-bit processor with Second Level Address Translation (SLAT). It also requires VM Monitor Mode extensions and hardware-assisted virtualization. Hyper-V can be managed using various tools, including [[Hyper-V Manager]] (a graphical tool), [[Windows PowerShell]] (for scripting), or [[System Center Virtual Machine Manager]] (for larger deployments).

