All devices must follow the naming convention `<codename>-<role/service>-<id>` _(example: `XXXXX-DC-01`)_. Through the Pi-Hole service, every device following this naming convention will get an FQDN based on their hostname and the local domain _(example: `XXXXX-DC-01.internaldomain1.com`)_.

Devices that have multiple network interfaces (LAN + Wifi, 10G LAN + 1G LAN) will get an identifier at the end of the secondary interface's hostname

| Identifier | Description                    |
| ---------- | ------------------------------ |
| BAK        | Secondary backup interface     |
| MGMT       | Managment interface            |
| WLAN       | Wireless interface             |
| HA         | High Availability IP           |

## Code name
Every device following this naming convention will have its `<codename>` be the name of a Star Citizen Ship.

## Ship names
- Avenger
	- [ ] Titan
	- [ ] Warlock
	- [ ] Stalker
	- [ ] Renegade
- [ ] Eclipse
- [ ] Gladius
- [ ] Hammerhead
- [ ] Reclaimer
- [ ] Redeemer
- [ ] Retaliator
- [x] Sabre
- [ ] Carrack
- [x] Hornet
	- [x] Wildfire
	- [x] Heartseeker
	- [x] Tracker
	- [x] Ghost
- [x] Lightning
- [ ] Hawk
- [ ] Hurricane
- [ ] Spartan
- [ ] Terrapin
- [x] Defender
- [x] Nomad
- [ ] Hercules
- [ ] Ares
	- [x] Inferno
	- [x] Ion
- [ ] Caterpillar
- [ ] Cutlass
- [x] Dragonfly
- [ ] Mule
- [ ] Vulture
- [ ] Blade
- [ ] Glaive
- [x] Prowler
- [ ] Talon
- [ ] Prospector
- [ ] Razor
- [ ] Reliant
- [x] Aurora
- [ ] Constellation
	- [ ] Andromeda
	- [x] Phoenix
	- [x] Aquila
	- [ ] Taurus
- [x] Mantis
- [x] Scorpius
- [ ] Cyclone
- [ ] Nova
- [x] Idris
- [x] Kraken
- [ ] Genesis
- [ ] Railen
- [x] Polaris
- [x] Mercury
- [ ] Orion
- [ ] Ursa
- [x] Galaxy
- [ ] Spirit
- [x] Freelancer

## Role or service
The role or service part of every device's name needs to be descriptive of what the device is mainly used for.

| String | Description |
| ---- | ---- |
| DC | Domain Controller |
| CL | Client device |
| WEB | Web server |
| DNS | Domain Name Server |
| DMZ | Demilitarized zone server |
| FS | File Server |
| Rtr | Router |
| SW | Switch |
| MINE | Minecraft server |
| HAc | Home Assistant Core |
| Hb | Homebrige |
| HV | Hypervisor |
| DH | Docker Host |
| Prtn | Printer |
| AP | Access Point |
| VR | Virtual Reality Heaset |
| VIP | Virtual IP |
| PXY | Proxy / Reverse Proxy server |
| GSN | Game Server Node (Pterodactyl) |
| RMM | Remote Moniroting and Managment |
| CLD | Cloud Server |
| MDA | Media Server |
| VPN | VPN Server |

## ID
The ID is a double-digit incrementing number to identify devices when multiple of them have the same role or service.
