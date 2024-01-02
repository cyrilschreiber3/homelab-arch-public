All devices must follow the naming convention `<os/distro>-<role/service><id>` _(example: `WinS2k19-DC01`)_. 

## OS / Distro
Every machine following this naming convention will have its `<os/distro>` part be composed of 3 particules:
- The base OS or distro name
- The edition (optional)
- The version

The order of the parts above can be chaned except for the base OS or distro name which always comes first.

### Base OS or distro name
| String | Name                     |
| ------ | ------------------------ |
| Win    | Windows                  |
| Cent   | CentOS                   |
| Ubu    | Ubuntu                   |

### Edition
| String | Name             |
| ------ | ---------------- |
| H      | Home             |
| P      | Pro              |
| E      | Enterprise       |
| S      | Server or Stream | 

### Version
This particle is is pretty straight forward. Just use a 1 - 4 character string with the exception of dates which are written with a lowercase `k` instead of a `0` _(example: `2019` --> `2k19`)_.

## Role or service
The role or service part of every device's name needs to be descriptive of what the device is mainly used for.

| String | Description               |
| ------ | ------------------------- |
| DC     | Domain Controller         |
| CL     | Client device             |
| WEB    | Web server                |
| PiH    | Pi-Hole server            |
| DMZ    | Demilitarized zone server |
| LB     | Load-Balancer             |
| FS     | File Server               |
| MINE   | Minecraft server          |
| HAc    | Home Assistant Core       |

## ID
The ID is a double-digit incrementing number to identify devices when multiple of them have the same role or service.