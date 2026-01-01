# Storage

Persistent storage is a critical component for stateful applications in **Jo3**.

## Storage Classes

- **proxmox-aquabot-bpool-xfs-i**:
    - **Type**: CSI Driver for Proxmox / ZFS / Local Storage.
    - **Usage**: High-performance storage for Databases (Postgres, InfluxDB).
- **nfs-client**:
    - **Usage**: Shared storage for media (Jellyfin, Audiobookshelf) and "ReadWriteMany" PVCs.

## Backups

Backups are likely handled by **Velero** or dedicated application-level backups (e.g., Postgres dumps to S3).
