# Namespaces & cgroups Overview

Linux namespaces and control groups (cgroups) are foundational to containerization technologies like Docker and Kubernetes. Together, they isolate and manage processes on the same host system, making containers lightweight yet secure.

## Linux Namespaces

Namespaces provide isolation by wrapping global system resources in per-process views. There are **six major namespaces**:

1. **PID (Process ID)** – Isolates process IDs so that processes inside a namespace only see and manage their own PID tree. This makes `PID 1` inside a container act like the init process.

2. **NET (Network)** – Provides separate network stacks, including interfaces, routing tables, and firewall rules. Each container can have its own virtual Ethernet interface.

3. **MNT (Mount)** – Isolates filesystem mount points. Processes can have a different view of the file system hierarchy, ensuring containers only see their own file tree.

4. **UTS (UNIX Timesharing System)** – Allows containers to have their own hostname and domain name. This is useful for distinguishing environments without affecting the host.

5. **IPC (Interprocess Communication)** – Isolates IPC resources such as message queues and shared memory. Prevents cross-container communication via IPC.

6. **USER** – Provides user and group ID mappings. A process can have root privileges inside the container while being mapped to a non-privileged user on the host, enhancing security.

## cgroups v2

Control groups (cgroups) limit and prioritize resource usage (CPU, memory, I/O) among process groups. **cgroups v2** unifies resource control under a single hierarchy and improves consistency and simplicity over v1. It introduces features like:

- Delegation of controllers
- Better memory management
- Nested cgroup handling

cgroups v2 is essential for fair and secure resource allocation in containerized environments, especially in multi-tenant systems.

Together, namespaces and cgroups provide the core functionality that allows containers to behave like isolated, resource-controlled mini-systems.
