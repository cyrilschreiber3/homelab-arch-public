# Mercury-FS-01
[Containers](apps.md#mercury-fs-01)
## Hardware
| Name | Model |
| ---- | ---- |
| CPU | Xeon X3450 |
| Mobo | Supermicro X8SIL-F |
| RAM | 32GB (4x8GB) DDR3 ECC 2Rx8 |
| Boot | 32GB Sata DOM |
| Case | FRACTAL DESIGN Meshify 2 |
| Hard Drive trays | Fractal Design HDD tray |
| HBA | TBD 8 port sata hba |
### Storage pools
| Pool name | vDEV type | Disks |
| ---- | ---- | ---- |
| Vault | Raid-Z2 | 5x 4TB HDD |
| TurboVault pool | Mirror | 2x 500GB SSD |
| Media1 | Stripe | 2x 4TB HDD |
| Media2 | Stripe | 2x 3TB HDD |

>[!INFO]
>Here are some SSD Specs Databases:
> - [TechPowerUp's SSD Database](https://www.techpowerup.com/ssd-specs/)
> - [Some Google Sheet list](https://docs.google.com/spreadsheets/d/1B27_j9NDPU3cNlj2HKcrfpJKHkOf-Oi1DbuuQva2gT4/edit#gid=0)
> - 
## Software 

- OS: TrueNAS Scale

# Kraken-DH-01
[Virtual Machines](apps.md#kraken-dh-01), [Containers](apps.md#kraken-dh-01-1)
## Hardware
| Name       | Model             |
| ---------- | ----------------- |
| CPU        | Xeon E3-1275 V2   |
| Mobo       | Asus P8B-M        |
| RAM        | 16GB            |
| CPU Cooler | Noctua NH-U9s   |
| Case       | LC Power PRO 925B |
| SSD        | 256GB SSD       | 
## Software 
- OS: RHEL

# Idris-HV-01
[Virtual Machines](apps.md#idris-hv-01)
## Hardware
HP ProDesk 400 G5 MT

| Name | Model                             |
| ---- | --------------------------------- |
| CPU  | i7-8700                           |
| Mobo | Proprietary HP Motherboard        |
| RAM  | 32GB (2x16GB) DDR4 |
| GPU  | Radeon RX550                      |
| SSD  | 512GB M.2 Nvme SSD                |
## Software 
- OS: Proxmox VE

# Mantis-DNS-02
[Containers](apps.md#mantis-dns-02)
## Hardware
Raspberry Pi 5 8Gb
## Software
- OS: Raspberry Pi OS Lite (Debian 12)

# Gladiator-DH-02
[Virtual Machines](apps.md#gladiator-dh-02), [Containers](apps.md#gladiator-dh-02-1)
## Hardware
Intel Nuc 11 Essential Kit

| Name | Model                         |
| ---- | ----------------------------- |
| CPU  | Celeron N5105 (11th gen)      |
| Mobo | Proprietary Intel Motherboard |
| RAM  | 16GB DDR4 3200MHz SODIMM    |
| GPU  | Integrated                    |
| SSD  | 256GB SSD                   | 
## Software
- OS: RHEL

# Aquila-VPN-01
[Containers](apps.md#aquila-vpn-01)
## Hardware
Raspberry Pi 3b+
## Software
- OS: Raspberry Pi OS Lite (Debian 12)