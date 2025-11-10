# VLAN Schema

| VLAN                                 | Purpose                         | Subnet             | Example IPs                                | Notes                           |
| ------------------------------------ | ------------------------------- | ------------------ | ------------------------------------------ | ------------------------------- |
| **10 – Management**                  | Proxmox host mgmt, SSH, Web UI  | `10.0.<node>.0/24` | `10.0.1.10` (Node1), `10.0.2.10` (Node2)   | Used for cluster + admin access |
| **20 – Cluster / Internal Services** | Corosync, migration, metrics    | `10.20.0.0/24`     | `10.20.1.10`, `10.20.1.11`                 | Optional, good for HA later     |
| **30 – Storage**                     | NFS / ZFS replication / backups | `10.30.0.0/24`     | NAS = `10.30.0.2`, Nodes = `10.30.x.x`     | Jumbo-frames OK here            |
| **40 – Apps / Servers**              | Plex, Radarr, Sonarr, Nextcloud | `10.40.0.0/24`     | `10.40.1.10` (Plex1), `10.40.2.10` (Plex2) | VMs/CTs connect here            |
| **50 – DMZ / Proxy**                 | Caddy2 / public-facing          | `10.50.0.0/24`     | Reverse proxy = `10.50.0.2`                | Route-limited to LAN+WAN        |
| **60 – IoT / Home Assistant**        | Smart devices                   | `10.60.0.0/24`     | HA OS = `10.60.0.10`                       | Strict firewall rules           |
| **70 – Client LAN**                  | Desktops / laptops              | `10.70.0.0/24`     | Your desktop/laptop                        | Normal user access              |
