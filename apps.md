# Virtual Machines

## Idris-HV-01
[Hardware](servers.md#idris-hv-01)
### Polaris-DC-01
OS: Windows Server 2022 Datacenter Edition

| Service                          | Description                                         | URL                                                               |
| -------------------------------- | --------------------------------------------------- | ----------------------------------------------------------------- |
| Domain Controller                | -                                                   | ad://polaris-dc-01.internaldomain1.com                               |
| Plex Server                      | -                                                   | https://plex.publicdomain1.com/<br>https://plex.internaldomain1.com/ |
| ~~Windows Server Update Server~~ | Removed due to being impractical and resource heavy | ~~http://polaris-dc-01.internaldomain1.com:8530/~~                   |
#### VM Config
| Setting        | Value                          |
| -------------- | ------------------------------ |
| CPU            | 6 vCPU cores (host)            |
| RAM            | 6 GB                           |
| Storage        | 128 GB                         |
| Network        | VirtIO nic (00:00:00:00:00:00) |
| PCI passthough | Radeon RX 550 2 GB             |

### Sentinel-DNS-01
OS: CentOS Stream 9

| Service    | Description                                                                                                                             | URL                                                          |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| Pi-hole    | -                                                                                                                                       | https://sentinel-dns-01.internaldomain1.com/<br>dns://10.1.1.51 |
| Keepalived | Load blancing and failover service<br>Doesn't work since [Mantis-DNS-02](apps.md#mantis-dns-02) isn't on the same network/subnet anymore | 192.168.1.85 (master)                                        |
| Unbound    | Recursive DNS Server                                                                                                                    | -                                                            |
| Cockpit    | Linux Cockpit                                                                                                                           | https://cockpit.sentinel-dns-01.internaldomain1.com/            |
#### VM Config
| Setting | Value                          |
| ------- | ------------------------------ |
| CPU     | 2 vCPU cores (host)            |
| RAM     | 2 GB                           |
| Storage | 32 GB                          |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Prowler-GSN-01
OS: Red Hat Enterprise Linux

| Service          | Description       | URL                                              |
| ---------------- | ----------------- | ------------------------------------------------ |
| Pterodactyl Node | Game server node  | -                                                |
| Syncthing        | File sync service | https://sync.prowler-gsn-01.internaldomain1.com/    |
| Cockpit          | Linux Cockpit     | https://cockpit.prowler-gsn-01.internaldomain1.com/ |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 4 vCPU cores (host) |
| RAM | 10 GB |
| Storage | 150 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Freelancer-CLD-01
OS: Red Hat Enterprise Linux

| Service       | Description                     | URL                                                                                                  |
| ------------- | ------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Nextcloud-AIO | Nextcloud (All in One Solution) | https://nextcloud-config.freelancer-cld-01.internaldomain1.com/<br>https://nextcloud.publicdomain1.com/ |
| Syncthing     | File sync service               | https://sync.freelancer-cld-01.internaldomain1.com/                                                     |
| Cockpit       | Linux Cockpit                   | https://cockpit.freelancer-cld-01.internaldomain1.com/                                                  |
#### VM Config
| Setting | Value                          |
| ------- | ------------------------------ |
| CPU     | 4 vCPU cores (host)            |
| RAM     | 4 GB                           |
| Storage | 32 GB                          |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Galaxy-RMM-01
OS: Debian 11

| Service      | Description          | URL                                             |
| ------------ | -------------------- | ----------------------------------------------- |
| Tactical RMM | Open source RMM tool | https://rmm.internaldomain1.com/                   |
| Cockpit      | Linux Cockpit        | https://cockpit.galaxy-rmm-01.internaldomain1.com/ |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 1 vCPU core (kvm64) |
| RAM | 4 GB |
| Storage | 32 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Dragonfly-MDA-01
OS: Debian 11

| Service     | Description                          | URL |
| ----------- | ------------------------------------ | --- |
| Roon Server | High-quality music streaming service | -   |
#### VM Config
| Setting | Value                                        |
| ------- | -------------------------------------------- |
| CPU     | 2 vCPU core (kvm64)                          |
| RAM     | 4 GB                                         |
| Storage | 32 GB                                        |
| Network | Emulated Intel E1000 nic (00:00:00:00:00:00) |

### Origin-CL-05
OS: MacOS Sonoma (14.0)
#### VM Config
| Setting | Value                                  |
| ------- | -------------------------------------- |
| CPU     | 4 vCPU core (host)                     |
| RAM     | 4 GB                                   |
| Storage | 90 GB                                  |
| Network | VMware vmxnet3 nic (00:00:00:00:00:00) |

### Gemini-BAK-01
OS: Win 11 Pro Debloated

| Service   | Description   | URL |
| --------- | ------------- | --- |
| Backblaze | Backup client | -   |
#### VM Config
| Setting | Value                          |
| ------- | ------------------------------ |
| CPU     | 4 vCPU core (host)             |
| RAM     | 4 GB                           |
| Storage | 80 GB                          |
| Network | VirtIO nic (00:00:00:00:00:00) |
### Endeavor-DNS-01 (LXC)
OS: Debian 12

| Service     | Description        | URL |
| ----------- | ------------------ | --- |
| Code Server | Development server | -   |
#### VM Config
| Setting | Value                          |
| ------- | ------------------------------ |
| CPU     | 4 vCPU core                    |
| RAM     | 4 GB                           |
| Storage | 32 GB                          |


## Kraken-DH-01
[Hardware](servers.md#kraken-dh-01)
### Wildfire-PXY-01
OS: Alpine Linux 3.17

| Service   | Description       | URL                                            |
| --------- | ----------------- | ---------------------------------------------- |
| Traefik   | Reverse proxy (internet facing)     | https://wildfire-pxy-01.internaldomain1.com/      |
| Keepalived          | Load blancing and failover service                  | 192.168.1.86 (master)                                               |
| Syncthing | File sync service | https://sync.wildfire-pxy-01.internaldomain1.com/ |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 1 vCPU core (host) |
| RAM | 1 GB |
| Storage | 5 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Tracker-PXY-03
OS: Alpine Linux 3.17

| Service   | Description       | URL                                            |
| --------- | ----------------- | ---------------------------------------------- |
| Traefik   | Reverse proxy (local only)     | https://tracker-pxy-03.internaldomain1.com/      |
| Keepalived          | Load blancing and failover service                  | 192.168.1.87 (master)                                               |
| Syncthing | File sync service | https://sync.tracker-pxy-03.internaldomain1.com/ |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 1 vCPU core (host) |
| RAM | 1 GB |
| Storage | 5 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Sabre-DNS-03
OS: Debian 11

| Service | Description | URL |
| ---- | ---- | ---- |
| Pi-hole | - | https://sabre-dns-03.internaldomain1.com/ <br>dns://192.168.1.32 |
| Unbound | Recursive DNS Server | - |

#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 2 vCPU core (host) |
| RAM | 2 GB |
| Storage | 10 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

## Gladiator-DH-02
[Hardware](servers.md#gladiator-dh-02)
### Heartseeker-PXY-02
OS: Alpine Linux 3.17

| Service   | Description       | URL                                            |
| --------- | ----------------- | ---------------------------------------------- |
| Traefik   | Reverse proxy (internet facing)     | https://heartseeker-pxy-02.internaldomain1.com/      |
| Keepalived          | Load blancing and failover service                  | 192.168.1.86 (backup)                                               |
| Syncthing | File sync service | https://sync.heartseeker-pxy-02.internaldomain1.com/ |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 1 vCPU core (host) |
| RAM | 1 GB |
| Storage | 5 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Ghost-PXY-04
OS: Alpine Linux 3.17

| Service    | Description                        | URL                                         |
| ---------- | ---------------------------------- | ------------------------------------------- |
| Traefik    | Reverse proxy (local only)         | https://ghost-pxy-04.internaldomain1.com/      |
| Keepalived | Load blancing and failover service | 192.168.1.87 (backup)                       |
| Syncthing  | File sync service                  | https://sync.ghost-pxy-04.internaldomain1.com/ |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 1 vCPU core (host) |
| RAM | 1 GB |
| Storage | 5 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

## Pegasus-HV-02
[Hardware](servers.md#pegasus-hv-02)
### Crucible-PRO-01
OS: Debian 12

| Service        | Description                     | URL                                                                |
| -------------- | ------------------------------- | ------------------------------------------------------------------ |
| Canonical MAAS | Bare metal provisioning service | https://maas.crucible-pro-01.internaldomain1.com/<br>ipxe://10.1.1.63 |
#### VM Config
| Setting | Value                          |
| ------- | ------------------------------ |
| CPU     | 2 vCPU cores (x86-64-v2-AES)   |
| RAM     | 2 GB                           |
| Storage | 64 GB                          |
| Network | VirtIO nic (00:00:00:00:00:00) |

# Docker Containers

## Kraken-DH-01
[Hardware](servers.md#kraken-dh-01)

| Stack name        | Service                          | Description                                                | URL                                                                                                                                                                                                                                                  |
| ----------------- | -------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| portainer         | Portainer                        | -                                                          | https://portainer.internaldomain1.com/                                                                                                                                                                                                                  |
| ansible-semaphore | Ansible Semaphore                | Web UI for Ansible                                         | https://semaphore.internaldomain1.com/<br>https://semaphore.publicdomain2.com/                                                                                                                                                                               |
| changedetection   | changedetection.io               | Change detection service                                   | https://changedetection.internaldomain1.com/                                                                                                                                                                                                            |
| homer             | -                                | Dashboard for my homelab                                   | https://dashboard.internaldomain1.com/                                                                                                                                                                                                                  |
| immich            | -                                | Photo storage service                                      | https://photos.publicdomain1.com/                                                                                                                                                                                                                    |
| my_spotify        | Your Spotify                     | Spotify stats dashboard                                    | https://myspotify.publicdomain2.com/                                                                                                                                                                                                                      |
| nebula-sync       | -                                | Service to sync the configuration of my 3 pihole instances | -                                                                                                                                                                                                                                                    |
| netboot           | netboot.xyz                      | local iPXE server                                          | ipxe://10.1.1.21/                                                                                                                                                                                                                                    |
| plex-addons-pub   | Overseerr, Wizarr                | Public Plex addons                                         | https://overseerr.publicdomain1.com/ <br>https://join.plex.publicdomain1.com/                                                                                                                                                                        |
| plex-addons-int   | Radarr, Sonarr, Lidarr, Prowlarr | Internal Plex addons                                       | https://radarr.publicdomain2.com/ <br>https://radarr.internaldomain1.com/ <br>https://sonarr.publicdomain2.com/ <br>https://sonarr.internaldomain1.com/ <br>https://lidarr.publicdomain2.com/ <br>https://lidarr.internaldomain1.com/ <br>https://prowlarr.internaldomain1.com/ |
| portfolio-1       | Apache, PHP, mySQL, phpmyadmin   | My personal website                                        | https://publicdomain1.com/ <br>https://portfoliodb.internaldomain1.com/                                                                                                                                                                                 |
| pterodactyl-panel | -                                | Pterodactyl admin panel                                    | https://pterodactyl.publicdomain2.com/                                                                                                                                                                                                                    |
| shlink            | -                                | Link shortener                                             | https://shlink.publicdomain2.com/ <br>https://l.publicdomain2.com/[slug]                                                                                                                                                                                       |
| speedtest-tracker | -                                | Tests my internet speed every hour                         | https://speedtest.internaldomain1.com/                                                                                                                                                                                                                  |
| vaultwarden       | -                                | Password manager                                           | https://passman.publicdomain2.com/                                                                                                                                                                                                                        |
| syncthing         | Syncthing                        | File sync service                                          | https://sync.kraken-dh-01.internaldomain1.com/                                                                                                                                                                                                          |
| zabbix            | Zabbix                           | Monitoring solution                                        | https://zabbix.internaldomain1.com/                                                                                                                                                                                                                     |
| auto-updater      | Watchtower                       | Container updater                                          | -                                                                                                                                                                                                                                                    |


## Gladiator-DH-02
[Hardware](servers.md#gladiator-dh-02)

| Name               | Service                                             | Description                                                     | URL                                                                                                             |
| ------------------ | --------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| almo               | -                                                   | Notifies me of new firefighter calls from my department (by me) | -                                                                                                               |
| ddns-updater       | -                                                   | Updates the dynamic dns records for my domains (by me)          | https://ddns.internaldomain1.com/                                                                                  |
| fake-file-creator  | -                                                   | Fake File Creator app                                           | https://ffc.publicdomain2.com/                                                                                       |
| gitea              | -                                                   | Self hosted git platform                                        | https://git.publicdomain2.com/                                                                                       |
| Grafana-stack      | Grafana, Prometheus, InfluxDB and various exporters | Metrics and log agregation tools                                | https://grafana.internaldomain1.com/<br>https://prometheus.internaldomain1.com/<br>https://influxdb.internaldomain1.com/ |
| homebridge         | Homebridge                                          | Bridge for non-Homekit devices                                  | https://homebridge.internaldomain1.com/                                                                            |
| minio              | Minio                                               | S3 storage                                                      | https://s3.publicdomain2.com/ <br>https://s3-admin.internaldomain1.com/                                                 |
| docs               | Outline                                             | Documentation/Wiki app                                          | https://docs.publicdomain1.com/                                                                                 |
| transfer           | pingvin-share                                       | Swisstransfer/Wetransfer alternative                            | https://transfer.publicdomain1.com/                                                                             |
| personal-website-2 | Apache, PHP, mySQL, phpmyadmin                      | My personal website                                             | https://publicdomain1.com/ <br>https://portfoliodb.internaldomain1.com/                                            |
| portainer-agent    | Portainer Agent                                     | -                                                               | -                                                                                                               |
| syncthing          | Syncthing                                           | File sync service                                               | https://sync.gladiator-dh-02.internaldomain1.com/                                                                  |
| webtop             | Webtop                                              | Web-based virtual desktop                                       | https://webtop.publicdomain2.com/                                                                                    |
| auto-updater       | Watchtower                                          | Container updater                                               | -                                                                                                               |


## Mercury-FS-01
[Hardware](servers.md#mercury-fs-01)

| Name            | Service         | Description            | URL                                                               |
| --------------- | --------------- | ---------------------- | ----------------------------------------------------------------- |
| cdn             | Nginx           | CDN                    | https://cdn.publicdomain2.com/                                         |
| filebrowser     | File Browser    | Web based file browser | https://explorer.mercury-fs-01.internaldomain1.com/                  |
| nzbget          | NZBGet          | Usenet download client | https://nzbget.publicdomain2.com/ <br>https://nzbget.internaldomain1.com/ |
| portainer-agent | Portainer Agent | -                      | -                                                                 |
| syncthing       | Syncthing       | File sync service      | https://sync.mercury-fs-01.internaldomain1.com/                      |


## Mantis-DNS-02
[Hardware](servers.md#mantis-dns-02)

| Service    | Description                        | URL                                                                  |
| ---------- | ---------------------------------- | -------------------------------------------------------------------- |
| Pi-hole    | -                                  | https://admin.mantis-dns-02.internaldomain1.com/ <br>dns://192.168.1.13 |
| Unbound    | Recursive DNS Server               | -                                                                    |
| Keepalived | Load blancing and failover service | 192.168.1.85 (backup)                                                |
| Cockpit    | Linux Cockpit                      | https://cockpit.mantis-dns-02.internaldomain1.com/                      |
| uptimekuma | Uptime monitoring service          | https://uptime.internaldomain1.com/                                     |

# Kubernetes Workloads

## Vanguard-KC-13
[Node 1](servers.md#harbinger-kn-01), [Node 2](servers.md#hoplite-kn-02), [Node 3](servers.md#warden-kn-03) 

| Item                    | Value        |
| ----------------------- | ------------ |
| Kubernetes distribution | K3S          |
| Database                | Embeded etcd |
| Load balancer           | MetalLB      |
| Ingress controller      | Traefik      |

| Service         | Description                                                                           | URL                                                      |
| --------------- | ------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| cert-manager    | Manages TLS certificates for Traefik                                                  | -                                                        |
| portainer-agent | Connection to the main Portainer instance                                             | -                                                        |
| renovate        | Automatic update management                                                           | -                                                        |
| bind9           | Dns server serving as upstream for all local dns entries. (Managed through Terraform) | dns://10.1.1.142 (all)<br>dns://10.1.1.143 (master only) |
| authentik       | SSO for most internal webapps                                                         | https://auth.internaldomain1.com/                           |
| kasm-workspaces | Container desktop streaming platform                                                  | https://desktop.internaldomain1.com/                        |
| longhorn        | Distributed block storage for Kubernetes                                              | https://longhorn.vanguard-kc-13-vip.internaldomain1.com/    |
| qdevice         | Quorum nodes to enable high availability on my 2 nodes proxmox server                 | -                                                        |
| wazuh           | Open source XDR and SIEM service                                                      | https://wazuh.internaldomain1.com/                          |
