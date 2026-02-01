# VLAN Schema

| VMID | Function Group | Hostname      | Static IP | Notes                     |
| ---- | -------------- | ------------- | --------- | ------------------------- |
| 001  | Infrastructure | `pve1`        | 10.0.1.2  | Proxmox Node 1            |
| 002  | Infrastructure | `pve2`        | 10.0.1.3  | Proxmox Node 2            |
| 003  | Infrastructure | `pve3`        | 10.0.1.4  | Proxmox Node 3            |
| 004  | Infrastructure | `pve4`        | 10.0.1.5  | Proxmox Node 4            |
| 201  | Storage        | `nfs`         | 10.0.2.2  | NAS/NFS Server            |
| 301  | Net/Security   | `caddy`       | 10.0.3.2  | Reverse Proxy             |
| 302  | Net/Security   | `wireguard`   | 10.0.3.3  | VPN endpoint              |
| 401  | Media          | `plex`        | 10.0.4.2  | Plex server               |
| 410  | Media          | `sonarr`      | 10.0.4.3  | Sonarr                    |
| 420  | Media          | `radarr`      | 10.0.4.4  | Radarr                    |
| 430  | Media          | `overseerr`   | 10.0.4.5  | Overseerr                 |
| 501  | Cloud Apps     | `nextcloud`   | 10.0.5.2  | Self-hosted cloud         |
| 601  | Automation     | `ansible`     | 10.0.6.2  | Automation control node   |
| 701  | Testing        | `k3s-node`    | 10.0.7.2  | K3s worker node           |
| 802  | Monitoring     | `grafana`     | 10.0.8.2  | First in Monitoring range |
| 1001 | Template       | `tmpl-ubuntu` | —         | No IP assigned            |
