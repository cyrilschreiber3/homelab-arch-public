Every device following the naming convention will get a static IP assigned by DHCP reservation. 

## VLANs


| ID  | CIDR         | Name              |
| --- | ------------ | ----------------- |
| 1   | 10.1.1.0/24  | Default           |
| 2   | 10.1.2.0/24  | Clients           |
| 3   | 10.1.3.0/24  | Untrusted Clients |
| 4   | 10.1.4.0/24  | IoT               |
| 20  | 10.1.20.0/24 | Guests            |

## Ranges

| Range                   | Description                    |
| ----------------------- | ------------------------------ |
| 10.1.1.1 - 10.1.1.9     | Routers / Firewalls / Switches |
| 10.1.1.10 - 10.1.1.19   | APs                            |
| 10.1.1.20 - 10.1.1.49   | Servers                        |
| 10.1.1.50 - 10.1.1.79   | Virtual Machines               |
| 10.1.1.80 - 10.1.1.119  | Managment                      |
| 10.1.1.120 - 10.1.1.139 | High-Availability IPs          |
| 10.1.1.140 - 10.1.1.159 | Kubernetes LB pool             |
| 10.1.1.160 - 10.1.1.179 | Other                          |

## Static Leases

| IP         | Hostname             | References                                                                                                                                    |
| ---------- | -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| 10.1.1.1   | Bengal-GW-01         |                                                                                                                                               |
| 10.1.1.2   | Apollo-SW-01         |                                                                                                                                               |
| 10.1.1.3   | Razor-SW-02          |                                                                                                                                               |
| 10.1.1.4   | Andromeda-SW-03      |                                                                                                                                               |
| 10.1.1.10  | Inferno-AP-01        |                                                                                                                                               |
| 10.1.1.20  | Mercury-FS-01        | [Hardware](servers.md#mercury-fs-01), [Containers](apps.md#mercury-fs-01)                                                     |
| 10.1.1.21  | Kraken-DH-01         | [Hardware](servers.md#kraken-dh-01), [VMs](apps.md#kraken-dh-01), [Containers](apps.md#kraken-dh-01-1)          |
| 10.1.1.22  | Idris-HV-01          | [Hardware](servers.md#idris-hv-01), [VMs](apps.md#idris-hv-01)                                                                 |
| 10.1.1.23  | Mantis-DNS-02        | [Hardware](servers.md#mantis-dns-02), [Containers](apps.md#mantis-dns-02)                                                     |
| 10.1.1.24  | Gladiator-DH-02      | [Hardware](servers.md#gladiator-dh-02), [VMs](apps.md#gladiator-dh-02), [Containers](apps.md#gladiator-dh-02-1) |
| 10.1.1.25  | Pegasus-HV-02        | [Hardware](servers.md#pegasus-hv-02), [VMs](apps.md#pegasus-hv-02)                                                             |
| 10.1.1.26  | Harbinger-KN-01      | [Hardware](servers.md#harbinger-kn-01)                                                                                                         |
| 10.1.1.27  | Hoplite-KN-02        | [Hardware](servers.md#hoplite-kn-02)                                                                                                           |
| 10.1.1.28  | Warden-KN-03         | [Hardware](servers.md#warden-kn-03)                                                                                                            |
| 10.1.1.29  | TMP-ED800G3M-1       |                                                                                                                                               |
| 10.1.1.50  | Polaris-DC-01        | [Hardware/Services](apps.md#polaris-dc-01)                                                                        |
| 10.1.1.51  | Sentinel-DNS-01      | [Hardware/Services](apps.md#sentinel-dns-01)                                                                      |
| 10.1.1.52  | Sabre-DNS-03         | [Hardware/Services](apps.md#sabre-dns-03)                                                                        |
| 10.1.1.53  | Wildfire-PXY-01      | [Hardware/Services](apps.md#wildfire-pxy-01)                                                                     |
| 10.1.1.54  | Heartseeker-PXY-02   | [Hardware/Services](apps.md#heartseeker-pxy-02)                                                               |
| 10.1.1.55  | Tracker-PXY-03       | [Hardware/Services](apps.md#tracker-pxy-03)                                                                      |
| 10.1.1.56  | Ghost-PXY-04         | [Hardware/Services](apps.md#ghost-pxy-04)                                                                     |
| 10.1.1.57  | Prowler-GSN-01       | [Hardware/Services](apps.md#prowler-gsn-01)                                                                       |
| 10.1.1.58  | Freelancer-CLD-01    | [Hardware/Services](apps.md#freelancer-cld-01)                                                                    |
| 10.1.1.59  | Galaxy-RMM-01        | [Hardware/Services](apps.md#galaxy-rmm-01)                                                                        |
| 10.1.1.60  | Dragonfly-MDA-01     | [Hardware/Services](apps.md#dragonfly-mda-01)                                                                     |
| 10.1.1.61  | Gemini-BAK-01        | [Hardware/Services](apps.md#gemini-bak-01)                                                                        |
| 10.1.1.62  | Endeavor-DEV-01      | [Hardware/Services](apps.md#endeavor-dns-01-(lxc))                                                                |
| 10.1.1.63  | Crucible-PRO-01      | [Hardware/Services](apps.md#crucible-pro-01)                                                                    |
| 10.1.1.80  | Mercury-FS-01-IPMI   |                                                                                                                                               |
| 10.1.1.81  | Kraken-DH-01-IPMI    |                                                                                                                                               |
| 10.1.1.82  | Mercury-FS-01-MGMT   |                                                                                                                                               |
| 10.1.1.83  | Kraken-DH-01-MGMT    |                                                                                                                                               |
| 10.1.1.84  | Idris-HV-01-MGMT     |                                                                                                                                               |
| 10.1.1.85  | Gladiator-DH-02-MGMT | Soon                                                                                                                                          |
| 10.1.1.86  | Pegasus-HV-02-MGMT   |                                                                                                                                               |
| 10.1.1.87  | Harbinger-KN-01      | Soon                                                                                                                                          |
| 10.1.1.88  | Hoplite-KN-02        | Soon                                                                                                                                          |
| 10.1.1.89  | Warden-KN-03         | Soon                                                                                                                                          |
| 10.1.1.90  | TMP-ED800G3M-1       | Soon                                                                                                                                          |
| 10.1.1.120 | Defender-DNS-12-VIP  | [Master](apps.md#sentinel-dns-01), [Backup](apps.md#mantis-dns-02)                                           |
| 10.1.1.121 | Hornet-PXY-12-VIP    | [Master](apps.md#wildfire-pxy-01), [Backup](apps.md#heartseeker-pxy-02)          |
| 10.1.1.122 | Lightning-PXY-34-VIP | [Master](apps.md#tracker-pxy-03), [Backup](apps.md#ghost-pxy-04)                 |
| 10.1.1.123 | Vanguard-KC-13-MGMT  | [Node 1](servers.md#harbinger-kn-01), [Node 2](servers.md#hoplite-kn-02), [Node 3](servers.md#warden-kn-03)                                      |
| 10.1.1.140 | Vanguard-KC-13-VIP   | Traefik ingress                                                                                                                               |
| 10.1.1.141 | Vanguard-KC-13-VIP   | Portainer Agent                                                                                                                               |
| 10.1.1.142 | Vanguard-KC-13-VIP   | Bind9 DNS (All)                                                                                                                               |
| 10.1.1.143 | Vanguard-KC-13-VIP   | Bind9 DNS (Master only)                                                                                                                       |
| 10.1.2.10  | Origin-CL-05         | [Hardware](apps.md#origin-cl-05)                                                                                  |
| 10.1.2.69  | Scorpius-CL-01       |                                                                                                                                               |

