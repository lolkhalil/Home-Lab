# Home-Lab
In my Home Lab I run many things like Jellyfin, Jellyseer, Transmission, Radarr, Sonarr and much more. Most of these are deployed through Portainer.

# Setup

## Hardware & OS
I've recently built a new PC to host everything on my Server. I'm currently using the latest Proxmox version, 9.0.11

### Specs:
- MB: MSI B550-A PRO
- CPU: AMD Ryzen 5 5600 6-Core Processor
- CPU Cooler: be quiet! Pure Rock 3
- RAM: 32GB DDR4 3200MHz
- SSD: Samsung 850 EVO 500GB (LVM-Thin)
- HDD: 2x4TB WD Red Plus 3.5" Drives (Mirror ZFS Pool)
- GPU: GeForce GTX 960
- Case: Corsair ICUE 220T
- Fans: 3x be quiet! Pure Wings 3 120mm
- PSU: be quiet! Pure Power12 650W 80+ Gold

## WireGuard
I recently setup a VPN Service so I can access my Lab from wherever using a modified [Proxmox Helper Script](https://community-scripts.github.io/ProxmoxVE/scripts?id=wireguard)


## Shared Drive
I'm currently running Cockpit on an Ubuntu LXC as my Shared Drive. 

### Shares:
- Configuration
- Media


## Portainer
Portainer is where I host most of the Arr Stack and the majority of my configuration.

### Arr Stack:
- [Bazarr](https://github.com/morpheus65535/bazarr): Generating Subtitles for the Media
- [Deunhealth](https://github.com/qdm12/deunhealth): Monitoring if Containers are Healthy or not
- [Flaresolverr](https://github.com/FlareSolverr/FlareSolverr): A Proxy Server to help Prowlarr with Indexers
- [Gluetun](https://github.com/qdm12/gluetun): Configured to go through my Surfshark VPN 
- [Prowlarr](https://github.com/Prowlarr/Prowlarr): Using Indexers to find Torrents
- [Radarr](https://github.com/Radarr/Radarr): Uses Prowlarr to find and request to download Movies
- [Sonarr](https://github.com/Sonarr/Sonarr): Same as Radarr but with TV Shows
- [Transmission](https://github.com/transmission/transmission): Downloads from the Torrents to get the actual Media

### Homepage Stack:
- [Mafl](https://github.com/hywax/mafl): Just a nice simple Homepage which I really like

### Media Stack:
- [Jellyseer](https://github.com/Fallenbagel/jellyseerr): Used to request Movies/Anime/TV Shows
- [Tachidesk](https://github.com/Suwayomi/Suwayomi-Server-docker): Just to read Manga really


## Jellyfin
I run my Jellyfin instance on an LXC using one of the [Proxmox Helper Scripts](https://tteck.github.io/Proxmox/) which are great!

### Plugins:
- [Intro Skipper](https://github.com/intro-skipper/intro-skipper): I mean it's in the name, 50/50 on when it'll work
- Open Subtitles: Just in case Bazarr doesn't generate the Subtitles
- [Skin Manager](https://github.com/danieladov/jellyfin-plugin-skin-manager): Some nice Themes to put on the Jellyfin interface
- AniDB, Fanart, TheTVDB: Mostly for metadata like pictures, info about the movie etc.


## Craft
Me and a couple friends wanted to play Minecraft together, so I found a [Proxmox Helper Script](https://community-scripts.github.io/ProxmoxVE/scripts?id=crafty-controller) to run a Minecraft Server for us


## Retro
I've setup an Ubuntu Virtual Machine to host a couple of Games that I wanted to be able to stream from my Phone, TV, Xbox, anywhere. 

### Services:
- [Sunshine](https://github.com/LizardByte/Sunshine): Streaming the Games
- Xrandr: Configure a Virtual Display for a Headless setup (this took FOREVER to figure out)

### Emulators
- [PCSX2](https://github.com/PCSX2/pcsx2): Running PS2 Games
- [RPCS3](https://github.com/RPCS3/rpcs3): Running PS3 Games
- [Cemu](https://github.com/cemu-project/Cemu): Running Wii U Games
- [Azahar](https://github.com/azahar-emu/azahar): Running 3DS Games

### GPU Passthrough
I passed through my GTX 960 to the VM so everything on the VM runs through it. This gives me very good performance for all my Emulators, for my PS3 Games they have been crashing a bit often however I think once all the textures are rendered in it'll be fine.


## Inspiration
From my Home Lab setup I followed a lot of Tutorials from [TechHut](https://www.youtube.com/@TechHut) and he was super useful!