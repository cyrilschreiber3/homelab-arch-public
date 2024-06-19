Every device following the naming convention will get a static IP assigned by DHCP reservation. 
## Ranges

| Range                       | Description                          |
| --------------------------- | ------------------------------------ |
| 192.168.1.1 - 192.168.1.4   | Routers / Firewalls / APs            |
| 192.168.1.5 - 192.168.1.9   | Switches                             |
| 192.168.1.10 - 192.168.1.29 | Servers                              |
| 192.168.1.30 - 192.168.1.49 | Virtual Machines / Docker containers |
| 192.168.1.50 - 192.168.1.69 | Clients                              | 
| 192.168.1.70 - 192.168.1.79 | Managment                            |
| 192.168.1.80 - 192.168.1.84 | VPNs / Proxy relays                  |
| 192.168.1.85 - 192.168.1.89 | High-Availability IPs                |
| 192.168.1.90 - 192.168.1.99 | Other                                |

## Static Leases

| IP               | Hostname             | References                                                                                                                                    |
| ---------------- | -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| 192.168.1.1      | Internet-Box         | [Config](http://192.168.1.1)                                                                                                                  |
| 192.168.1.2      | Inferno-AP-01        | -                                                                                                                                             |
| 192.168.1.3      | Ion-AP-02            | -                                                                                                                                             |
| 192.168.1.5      | Apollo-SW-01         | [Config](https://ui.internaldomain1.com)                                                                                                         |
| 192.168.1.10     | Mercury-FS-01        | [Hardware](servers.md#mercury-fs-01), [Containers](apps.md#mercury-fs-01)                                                     |
| 192.168.1.11     | Kraken-DH-01         | [Hardware](servers.md#kraken-dh-01), [VMs](apps.md#kraken-dh-01), [Containers](apps.md#kraken-dh-01-1)          |
| 192.168.1.12     | Idris-HV-01          | [Hardware](servers.md#idris-hv-01), [VMs](apps.md#idris-hv-01)                                                                 |
| 192.168.1.13     | Mantis-DNS-02        | [Hardware](servers.md#mantis-dns-02), [Containers](apps.md#mantis-dns-02)                                                     |
| 192.168.1.14     | Gladiator-DH-02      | [Hardware](servers.md#gladiator-dh-02), [VMs](apps.md#gladiator-dh-02), [Containers](apps.md#gladiator-dh-02-1) |
| 192.168.1.15                 | Aquila-VPN-01                     | [Hardware](servers.md#aquila-vpn-01), [Containers](apps.md#aquila-vpn-01)                                                                                                                                              |
| 192.168.1.30     | Polaris-DC-01        | [Hardware/Services](apps.md#polaris-dc-01)                                                                        |
| 192.168.1.31     | Sentinel-DNS-01      | [Hardware/Services](apps.md#sentinel-dns-01)                                                                      |
| 192.168.1.32     | Sabre-DNS-03         | [Hardware/Services](apps.md#sabre-dns-03)                                                                        |
| 192.168.1.33     | Wildfire-PXY-01      | [Hardware/Services](apps.md#wildfire-pxy-01)                                                                     |
| 192.168.1.34     | Heartseeker-PXY-02   | [Hardware/Services](apps.md#heartseeker-pxy-02)                                                               |
| 192.168.1.35     | Tracker-PXY-03       | [Hardware/Services](apps.md#tracker-pxy-03)                                                                      |
| 192.168.1.36     | Ghost-PXY-04         | [Hardware/Services](apps.md#ghost-pxy-04)                                                                     |
| 192.168.1.37     | Prowler-GSN-01       | [Hardware/Services](apps.md#prowler-gsn-01)                                                                       |
| 192.168.1.38     | Freelancer-CLD-01    | [Hardware/Services](apps.md#freelancer-cld-01)                                                                    |
| 192.168.1.39     | Galaxy-RMM-01        | [Hardware/Services](apps.md#galaxy-rmm-01)                                                                        |
| 192.168.1.40     | Dragonfly-MDA-01     | [Hardware/Services](apps.md#dragonfly-mda-01)                                                                     |
| 192.168.1.50     | Scorpius-CL-01-WLAN  |                                                                                                                                               |
| 192.168.1.51     | Arrow-CL-02          |                                                                                                                                               |
| 192.168.1.52     | Arrow-CL-02-WLAN     |                                                                                                                                               |
| 192.168.1.53     | Aurora-CL-03         |                                                                                                                                               |
| 192.168.1.54     | Aurora-CL-03-WLAN    |                                                                                                                                               |
| 192.168.1.55     | Nomad-CL-04          |                                                                                                                                               |
| 192.168.1.56     | Phoenix-VR-01        |                                                                                                                                               |
| 192.168.1.69     | Scorpius-CL-01       |                                                                                                                                               |
| 192.168.1.70     | Mercury-FS-01-MGMT   | [Config](http://192.168.1.70)                                                                                                                 |
| 192.168.1.71     | Kraken-DH-01-MGMT    | [Config](http://192.168.1.71)                                                                                                                 |
| ~~192.168.1.72~~ | ~~Idris-HV-01-MGMT~~ |                                                                                                                                               |
| 192.168.1.80     | VPN-taasccy3         |                                                                                                                                               |
| 192.168.1.81     | VPN-Guest            |                                                                                                                                               |
| 192.168.1.85     | Defender-DNS-12-VIP  | [Master](apps.md#sentinel-dns-01), [Backup](apps.md#mantis-dns-02)                                           |
| 192.168.1.86     | Hornet-PXY-12-VIP    | [Master](apps.md#wildfire-pxy-01), [Backup](apps.md#heartseeker-pxy-02)          |
| 192.168.1.87     | Lightning-PXY-34-VIP | [Master](apps.md#tracker-pxy-03), [Backup](apps.md#ghost-pxy-04)                 |

