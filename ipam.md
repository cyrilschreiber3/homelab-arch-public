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
| 10.1.1.140 - 10.1.1.159 | VPNs / Proxy relays            |
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
| 10.1.1.25  | Aquila-VPN-01        | [Hardware](servers.md#aquila-vpn-01), [Containers](apps.md#aquila-vpn-01)                                                     |
| 10.1.1.26  | TMP-ED800G3T-1       |                                                                                                                                               |
| 10.1.1.27  | TMP-ED800G3S-1       |                                                                                                                                               |
| 10.1.1.28  | TMP-ED800G3S-2       |                                                                                                                                               |
| 10.1.1.29  | TMP-ED800G3S-3       |                                                                                                                                               |
| 10.1.1.30  | TMP-ED800G3M-1       |                                                                                                                                               |
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
| 10.1.1.62  | Endeavor-DEV-01      |                                                                                                                                               |
| 10.1.1.80  | Mercury-FS-01-MGMT   |                                                                                                                                               |
| 10.1.1.81  | Kraken-DH-01-MGMT    |                                                                                                                                               |
| 10.1.1.82  | Idris-HV-01-MGMT     | Soon                                                                                                                                          |
| 10.1.1.83  | Gladiator-DH-02-MGMT | Soon                                                                                                                                          |
| 10.1.1.84  | TMP-ED800G3T-1       | Soon                                                                                                                                          |
| 10.1.1.85  | TMP-ED800G3S-1       | Soon                                                                                                                                          |
| 10.1.1.86  | TMP-ED800G3S-2       | Soon                                                                                                                                          |
| 10.1.1.87  | TMP-ED800G3S-3       | Soon                                                                                                                                          |
| 10.1.1.88  | TMP-ED800G3M-1       | Soon                                                                                                                                          |
| 10.1.1.120 | Defender-DNS-12-VIP  | [Master](apps.md#sentinel-dns-01), [Backup](apps.md#mantis-dns-02)                                           |
| 10.1.1.121 | Hornet-PXY-12-VIP    | [Master](apps.md#wildfire-pxy-01), [Backup](apps.md#heartseeker-pxy-02)          |
| 10.1.1.122 | Lightning-PXY-34-VIP | [Master](apps.md#tracker-pxy-03), [Backup](apps.md#ghost-pxy-04)                 |
| 10.1.2.10  | Origin-CL-05         | [Hardware](apps.md#origin-cl-05)                                                                                  |
| 10.1.2.69  | Scorpius-CL-01       |                                                                                                                                               |

