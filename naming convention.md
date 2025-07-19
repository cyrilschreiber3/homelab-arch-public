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
- [x] Apollo
- [ ] Ares
    - [x] Inferno
    - [ ] Ion
- [ ] Arrastra
- [ ] Arrow
- [ ] Asgard
- [ ] Aurora
- [ ] Avenger
    - [ ] Renegade
    - [ ] Stalker
    - [ ] Titan
    - [ ] Warlock
- [ ] Ballista
    - [ ] Dunestalker
    - [ ] Snowblind
- [x] Bengal
- [ ] Blade
- [ ] Buccaneer
- [ ] Carrack
- [ ] Caterpillar
- [ ] Centurion
- [ ] Constellation
    - [x] Andromeda
    - [ ] Aquila
    - [x] Phoenix
    - [ ] Taurus
- [ ] Corsair
- [ ] Crucible
- [ ] Cutlass
- [ ] Cutter
    - [ ] Rambler
    - [ ] Scout
- [ ] Cyclone
- [x] Defender
- [x] Dragonfly
- [ ] Eclipse
- [x] Endeavor
- [ ] Expanse
- [ ] Fortune
- [x] Freelancer
- [ ] Fury
- [x] Galaxy
- [x] Genesis
- [x] Gladiator
- [ ] Gladius
  - [ ] Valiant
- [ ] Glaive
- [ ] Golem
- [ ] Guardian
- [ ] Hammerhead
- [ ] Hawk
- [ ] Herald
- [ ] Hercules
- [x] Hornet
    - [x] Ghost
    - [x] Heartseeker
    - [x] Tracker
    - [x] Wildfire
- [ ] Hurricane
- [x] Idris
- [ ] Intrepid
- [ ] Ironclad
- [ ] Javelin
- [x] Kraken
    - [ ] Privateer
- [ ] Legionaire
- [ ] Liberator
- [x] Lightning
- [ ] Lynx
- [x] Mantis
- [x] Mercury
- [ ] Meteor
- [ ] Mole
    - [ ]  Talus
- [ ] Mule
- [ ] Mustang
- [ ] Nautilus
    - [ ] Solstice
- [ ] Nomad
- [ ] Nova
- [ ] Nox
- [ ] Odyssey
- [x] Origin
- [ ] Orion
- [ ] Paladin
- [ ] Perseus
- [ ] Pioneer
- [ ] Pisces
- [x] Polaris
- [ ] Prospector
- [x] Prowler
- [ ] Pulse
- [ ] Raft
- [ ] Railen
- [ ] Ranger
- [x] Razor
- [ ] Reclaimer
- [ ] Redeemer
- [ ] Reliant
- [ ] Retaliator
- [x] Sabre
    - [ ] Comet
    - [ ] Firebird
    - [ ] Peregrine
    - [ ] Raven
- [x] Scorpius
    - [ ] Antares
- [ ] Scythe
- [ ] Spartan
- [ ] Spirit
- [ ] Starfarer
    - [x] Gemini
- [ ] Starlancer
- [ ] Talon
- [ ] Terrapin
- [ ] Ursa
- [ ] Valkyrie
- [ ] Vanguard
    - [ ] Harbinger
    - [ ] Hoplite
    - [x] Sentinel
    - [ ] Warden
- [ ] Vulcan
- [ ] Vulture
- [ ] Zeus

## Role or service
The role or service part of every device's name needs to be descriptive of what the device is mainly used for.

| String | Description                     |
| ------ | ------------------------------- |
| DC     | Domain Controller               |
| CL     | Client device                   |
| WEB    | Web server                      |
| DNS    | Domain Name Server              |
| DMZ    | Demilitarized zone server       |
| FS     | File Server                     |
| Rtr    | Router                          |
| SW     | Switch                          |
| MINE   | Minecraft server                |
| HAc    | Home Assistant Core             |
| Hb     | Homebrige                       |
| HV     | Hypervisor                      |
| DH     | Docker Host                     |
| Prtn   | Printer                         |
| AP     | Access Point                    |
| VR     | Virtual Reality Heaset          |
| VIP    | Virtual IP                      |
| PXY    | Proxy / Reverse Proxy server    |
| GSN    | Game Server Node (Pterodactyl)  |
| RMM    | Remote Moniroting and Managment |
| CLD    | Cloud Server                    |
| MDA    | Media Server                    |
| VPN    | VPN Server                      |
| BAK    | Backup Server                   |
| GW     | Gateway                         |
| DEV    | Developpement server            |

## ID
The ID is a double-digit incrementing number to identify devices when multiple of them have the same role or service.
