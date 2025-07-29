
# Systems

## Mercury-FS-01

| Service                                         | Depends on                  | Host system       |
| ----------------------------------------------- | --------------------------- | ----------------- |
| CDN                                             | Vault                       | Local             |
| NZBGet                                          | Media1, Media2              | Local             |
| UrBackup                                        | Vault                       | Local             |
| Plex Addons - Internal (Sonarr, Radarr, Lidarr) | Media1, Media2              | Kraken-DH-01      |
| Minio                                           | Turbo Vault / Minio         | Gladiator-DH-02   |
| Pingvin-Share                                   | Turbo Vault / Pingvin-Share | Gladiator-DH-02   |
| Nextcloud                                       | Vault                       | Freelancer-CLD-01 |
 
# Services

## Minio
Host: Mercury-FS-01

| Service | Depends on        | Host system     |
| ------- | ----------------- | --------------- |
| Outline | S3 Object Storage | Gladiator-DH-02 |
## Traefik
Host: 
- External: Wildfire-PXY-01, Heartseeker-PXY-02
- Internal: Tracker-PXY-03, Ghost-PXY-04

Every service with a web interface since it's the reverse proxy for all webapps.