# Nodes & Hardware

The **Jo3** cluster is composed of multiple nodes, likely a mix of physical and virtual machines managed via Proxmox.

## Node Topology

> [!NOTE]
> Specific node details (CPU, RAM, IP) are managed dynamically.

- **Control Plane**: Manages the Kubernetes API, Scheduler, and Controllers.
- **Worker Nodes**: Run the actual workloads.
- **GPU Nodes**: Dedicated nodes (e.g., `vm169`) equipped with NVIDIA GPUs for AI workloads like Ollama and Whisper.

## Operating System

Nodes typically run a Linux distribution optimized for Kubernetes (e.g., Talos, Ubuntu with K3s/RKE2).
