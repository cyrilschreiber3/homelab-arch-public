This will explain every step of the upgrade process to be sure no data is lost.

1. [x] Backup the OS drive of `WinS2k19-DC01` to ISO and VM image (Directly attatched boot ssd to VM)
2. [x] Shutdown `WinS2k19-DC01` 
3. [x] Disconnect all drives and check data integrity on `Win10P-CL01`
4. [x] Assemble all systems
5. [x] Install proxmox on `Idris-HV-01` 
	1. [x] Create a temporary VM of `WinS2k19-DC01` with the same properties as the barebones system
6. [x] Setup `Mercury-FS-01` 
	1. [x] Install OS
	2. [x] Setup `vault` pool (5x4tb in raidz 2)
	3. [x] Transfer data from `data2` pool on the temp VM of `WinS2k19-DC01`
	4. [x] Transfer data from `plex` pool to `vault`
	5. [x] Setup `plex` pool (2x 4tb stripe + 3x 3tb stripe)
	6. [x] Transfer media from `vault` to `plex`
	7. [x] Setup NZBGet and transfer data and history from the temp VM of `WinS2k19-DC01`
7. [x] Setup os on all servers 
	1. [x] Install OS on `Kraken-DH-01`
	2. [x] Install Portainer on `Kraken-DH-01`
	3. [x] Install OS on `Mantis-DNS-03`
	4. [x] Install OS on `Gladiator-DH-02`
	5. [x] Install Portainer on `Gladiator-DH-02`
8. [x] Setup all 4 PiHole instances 
	1. [x] Create VM `Sentinel-DNS-01`
	2. [x] Install OS on `Sentinel-DNS-01`
	3. [x] Install PiHole on `Sentinel-DNS-01`
	4. [x] Deploy PiHole stack for `Sabre-DNS-03` on `Kraken-DH-01` (Migrated to vm)
	5. [x] Setup gravity sync (activate with dns-03 when ip 192.168.1.32 gets freed)
	6. [x] Setup keepalived on `Sentinel-DNS-01` and `Sabre-DNS-03` (`Defender-DNS-23-VIP`)
	7. [x] Install PiHole on `Mantis-DNS-02`
9. [x] Setup all 4 reverse proxy instances 
	1. [x] Setup VM `Wildfire-PXY-01` on  `Kraken-DH-01`
	2. [x] Setup Traefik on `Wildfire-PXY-01`
	3. [x] Setup VM `Heartseeker-PXY-02` on `Gladiator-DH-02`
	4. [x] Setup Traefik on `Heartseeker-PXY-02`
	5. [x] Setup sync between `Wildfire-PXY-01` and `Heartseeker-PXY-02` (later)
	6. [x] Setup keepalived between `Wildfire-PXY-01` and `Heartseeker-PXY-02` (`Hornet-PXY-12-VIP`)
	7. [x] Setup VM `Tracker-PXY-03` on `Kraken-DH-01`
	8. [x] Setup Traefik on `Tracker-PXY-03`
	9. [x] Setup VM `Ghost-PXY-04` on `Gladiator-DH-02`
	10. [x] Setup Traefik on `Ghost-PXY-04`
	11. [x] Setup sync between `Tracker-PXY-03` and `Ghost-PXY-04` (later)
	12. [x] Setup keepalived between `Tracker-PXY-03` and `Ghost-PXY-04` (`Lightning-PXY-34-VIP`)
11. [ ] Setup `Polaris-DC-01` VM on `Idris-HV-01` 
	1. [x] Setup domain controller and transfer domain ownership
		1. [x] Rename domain from `.local` to `.dev`
	2. [x] Setup Windows Backup Server
	3. [ ] Setup PXE server
	4. [x] Setup Plex and transfer library
12. [ ] Deploy all containers on `Kraken-DH-01`
	1. [ ] Grafana
	2. [x] Homer
	3. [x] Your Spotify
	4. [x] Plex-addons-pub
	5. [x] Plex-addons-int
	6. [x] shlink
	7. [x] vaultwarden
	8. [x] roon (Will use a VM in the end)
	9. [x] fake file creator
	10. [x] unifi controller
	11. [x] roundcube
	12. [x] pingvin-share
	13. [ ] vs-code
		1. [ ] setup auto deploy of config files (maybe later)
	14. [x] watchtower
13. [x] Deploy all containers on `Gladiator-DH-02`
	1. [x] homebridge
	2. [x] personal website
		1.  [ ] migrate photos to cdn on vault
		2.  [ ] fix contact form
	3. [x] uptimekuma
	4. [x] watchtower
14. [x] Setup nextcloud
	1. [x] Create VM `Freelancer-CLD-01`
	2. [x] Install OS
	3. [x] Install Docker
	4. [x] Deploy Nextcloud AIO stack
15. [x] Setup Tactical RMM on VM `Galaxy-RMM-01`
	1. [x] Install OS
	2. [x] Install service
	3. [x] Install agent on all nodes
16. [x] Setup pterodactyl
	1. [x] Deploy dashboard on `Kraken-DH-01`
	2. [x] Create VM `Prowler-GSN-01`
	3. [x] Install OS
	4. [x] Setup node
17. [x] Migrate notifications to Discord