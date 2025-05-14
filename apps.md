# Virtual Machines

## Idris-HV-01
[Hardware](servers.md#idris-hv-01)
### Polaris-DC-01
OS: Windows Server 2022 Datacenter Edition

| Service                          | Description                                         | URL                                                               |
| -------------------------------- | --------------------------------------------------- | ----------------------------------------------------------------- |
| Domain Controller                | -                                                   | ad://polaris-dc-01.internaldomain1.com                               |
| PXE Server                       | Preboot Execution Evironment                        | pxe://polaris-dc-01.internaldomain1.com                              |
| Windows Backup Server            | -                                                   | -                                                                 |
| Plex Server                      | -                                                   | https://plex.publicdomain1.com/<br>https://plex.internaldomain1.com/ |
| ~~Windows Server Update Server~~ | Removed due to being impractical and resource heavy | ~~http://polaris-dc-01.internaldomain1.com:8530/~~                   | 
#### VM Config
| Setting        | Value                          |
| -------------- | ------------------------------ |
| CPU            | 6 vCPU cores (host)            |
| RAM            | 6 GB                           |
| Storage        | 128 GB                         |
| Network        | VirtIO nic (00:00:00:00:00:00) |
| PCI passthough | Radeon RC 550 2 GB                               |

### Sentinel-DNS-01
OS: CentOS Stream 9

| Service | Description | URL |
| ---- | ---- | ---- |
| Pi-hole | - | https://sentinel-dns-01.internaldomain1.com/<br>dns://192.168.1.31 |
| Keepalived | Load blancing and failover service | 192.168.1.85 (master) |
| Unbound | Recursive DNS Server | - |
| Cockpit | Linux Cockpit | https://cockpit.sentinel-dns-01.internaldomain1.com/ |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 2 vCPU cores (host) |
| RAM | 2 GB |
| Storage | 32 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Prowler-GSN-01
OS: Red Hat Enterprise Linux

| Service | Description | URL |
| ---- | ---- | ---- |
| Pterodactyl Node | Game server node | - |
| Syncthing | File sync service | https://sync.prowler-gsn-01.internaldomain1.com/ |
| Cockpit | Linux Cockpit | https://cockpit.prowler-gsn-01.internaldomain1.com/ |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 4 vCPU cores (host) |
| RAM | 10 GB |
| Storage | 150 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Freelancer-CLD-01
OS: Red Hat Enterprise Linux

| Service       | Description                     | URL                                                                                                 |
| ------------- | ------------------------------- | --------------------------------------------------------------------------------------------------- |
| Nextcloud-AIO | Nextcloud (All in One Solution) | https://nextcloud-config.freelancer-cld-01.internaldomain1.com/<br>https://nextcloud.publicdomain1.com/ |
| Syncthing              | File sync service                                | https://sync.freelancer-cld-01.internaldomain1.com/                                                                                                    |
| Cockpit       | Linux Cockpit                   | https://cockpit.freelancer-cld-01.internaldomain1.com/                                                  |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 4 vCPU cores (host) |
| RAM | 4 GB |
| Storage | 32 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

### Galaxy-RMM-01
OS: Debian 11

| Service      | Description          | URL                                            |
| ------------ | -------------------- | ---------------------------------------------- |
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

| Service | Description | URL |
| ---- | ---- | ---- |
| Roon Server | High-quality music streaming service | - |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 2 vCPU core (kvm64) |
| RAM | 4 GB |
| Storage | 32 GB |
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
| Setting | Value              |
| ------- | ------------------ |
| CPU     | 4 vCPU core (host) |
| RAM     | 4 GB               |
| Storage | 80 GB              |
| Network | VirtIO nic ()      |

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

| Service   | Description       | URL                                            |
| --------- | ----------------- | ---------------------------------------------- |
| Traefik   | Reverse proxy (local only)     | https://ghost-pxy-04.internaldomain1.com/      |
| Keepalived          | Load blancing and failover service                  | 192.168.1.87 (backup)                                               |
| Syncthing | File sync service | https://sync.ghost-pxy-04.internaldomain1.com/ |
#### VM Config
| Setting | Value |
| ---- | ---- |
| CPU | 1 vCPU core (host) |
| RAM | 1 GB |
| Storage | 5 GB |
| Network | VirtIO nic (00:00:00:00:00:00) |

# Docker Containers

## Kraken-DH-01
[Hardware](servers.md#kraken-dh-01)

| Name               | Service                                             | Description                                                                                      | URL                                                                                                                                                                                                                                                  |
| ------------------ | --------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| portainer          | Portainer                                           | -                                                                                                | https://portainer.internaldomain1.com/                                                                                                                                                                                                                  |
| Grafana-stack      | Grafana, Prometheus, InfluxDB and various exporters | Matrics and log agregation tools                                                                 | https://grafana.internaldomain1.com/<br>https://prometheus.internaldomain1.com/<br>https://influxdb.internaldomain1.com/                                                                                                                                      |
| ansible-semaphore  | Ansible Semaphore                                   | Web UI for Ansible                                                                               | https://semaphore.internaldomain1.com/<br>https://semaphore.publicdomain2.com/                                                                                                                                                                               |
| homer              | -                                                   | Dashboard for my homelab                                                                         | https://dashboard.internaldomain1.com/                                                                                                                                                                                                                  |
| my_spotify         | Your Spotify                                        | Spotify stats dashboard                                                                          | https://myspotify.publicdomain2.com/                                                                                                                                                                                                                      |
| plex-addons-pub    | Overseerr, Wizarr                                   | Public Plex addons                                                                               | https://overseerr.publicdomain1.com/ <br>https://join.plex.publicdomain1.com/                                                                                                                                                                        |
| plex-addons-int    | Radarr, Sonarr, Lidarr, Prowlarr                    | Internal Plex addons                                                                             | https://radarr.publicdomain2.com/ <br>https://radarr.internaldomain1.com/ <br>https://sonarr.publicdomain2.com/ <br>https://sonarr.internaldomain1.com/ <br>https://lidarr.publicdomain2.com/ <br>https://lidarr.internaldomain1.com/ <br>https://prowlarr.internaldomain1.com/ |
| shlink             | -                                                   | Link shortener                                                                                   | https://shlink.publicdomain2.com/ <br>https://l.publicdomain2.com/[slug]                                                                                                                                                                                       |
| vaultwarden        | -                                                   | Password manager                                                                                 | https://passman.publicdomain2.com/                                                                                                                                                                                                                        |
| pterodactyl-panel  | -                                                   | Pterodactyl admin panel                                                                          | https://pterodactyl.publicdomain2.com/                                                                                                                                                                                                                    |
| personal-website-1 | Apache, PHP, mySQL, phpmyadmin                      | My personal website                                                                              | https://publicdomain1.com/ <br>https://portfoliodb.internaldomain1.com/                                                                                                                                                                                 |
| unifi-controller   | Unifi Controller                                    | -                                                                                                | https://ui.internaldomain1.com/                                                                                                                                                                                                                         |
| coder              | Coder / code-server                                 | Centralized Code server                                                                          | https://code.publicdomain2.com/                                                                                                                                                                                                                           |
| speedtest-tracker  | -                                                   | Tests my internet speed every hour                                                               | https://speedtest.internaldomain1.com/                                                                                                                                                                                                                  |
| syncthing          | Syncthing                                           | File sync service                                                                                | https://sync.kraken-dh-01.internaldomain1.com/                                                                                                                                                                                                          |
| pivpn-web          | -                                                   | Web GUI for the PiVPN project running on [Aquila-VPN-01](apps.md#aquila-vpn-01) | https://pivpn-web.internaldomain1.com/                                                                                                                                                                                                                  |
| auto-updater       | Watchtower                                          | Container updater                                                                                | -                                                                                                                                                                                                                                                    |


## Gladiator-DH-02
[Hardware](servers.md#gladiator-dh-02)

| Name               | Service                        | Description                                                     | URL                                                                  |
| ------------------ | ------------------------------ | --------------------------------------------------------------- | -------------------------------------------------------------------- |
| portainer-agent    | Portainer Agent                | -                                                               | -                                                                    |
| cta-notifier       | -                              | Notifies me of new firefighter calls from my department (by me) | -                                                                    |
| ddns-updater       | -                              | Updates the dynamic dns records for my domains (by me)          | https://ddns.internaldomain1.com/                                       |
| fake-file-creator  | -                              | Fake File Creator app                                           | https://ffc.publicdomain2.com/                                            |
| homebridge         | Homebridge                     | Bridge for non-Homekit devices                                  | https://homebridge.internaldomain1.com/                                 |
| minio              | Minio                          | S3 storage                                                      | https://s3.publicdomain2.com/ <br>https://s3-admin.internaldomain1.com/      |
| docs               | Outline                        | Documentation/Wiki app                                          | https://docs.publicdomain1.com/                                      |
| personal-website-2 | Apache, PHP, mySQL, phpmyadmin | My personal website                                             | https://publicdomain1.com/ <br>https://portfoliodb.internaldomain1.com/ |
| transfer           | pingvin-share                  | Alternative to swisstransfer                                    | https://transfer.publicdomain1.com/                                  |
| syncthing          | Syncthing                      | File sync service                                               | https://sync.gladiator-dh-02.internaldomain1.com/                       |
| auto-updater       | Watchtower                     | Container updater                                               | -                                                                    |


## Mercury-FS-01
[Hardware](servers.md#mercury-fs-01)

| Name      | Service   | Description                        | URL                                                               |
| --------- | --------- | ---------------------------------- | ----------------------------------------------------------------- |
| nzbget    | NZBGet    | Usenet download client             | https://nzbget.publicdomain2.com/ <br>https://nzbget.internaldomain1.com/ |
| syncthing | Syncthing | File sync service                  | https://sync.mercury-fs-01.internaldomain1.com/                      |
| cdn       | Nginx     | CDN                                | https://cdn.publicdomain2.com/                                         |


## Mantis-DNS-02
[Hardware](servers.md#mantis-dns-02)

| Service | Description | URL |
| ---- | ---- | ---- |
| Pi-hole | - | https://admin.mantis-dns-02.internaldomain1.com/ <br>dns://192.168.1.13 |
| Unbound | Recursive DNS Server | - |
| Keepalived | Load blancing and failover service | 192.168.1.85 (backup) |
| Cockpit | Linux Cockpit | https://cockpit.mantis-dns-02.internaldomain1.com/ |
| uptimekuma | Uptime monitoring service | https://uptime.internaldomain1.com/ |

## Aquila-VPN-01
[Hardware](servers.md#aquila-vpn-01)

| Service | Description | URL |
| ---- | ---- | ---- |
| PiVPN | Wireguard VPN Server | openvpn://vpn.publicdomain2.com/ |
| Cockpit | Linux Cockpit | https://cockpit.aquila-vpn-01.internaldomain1.com/ |
