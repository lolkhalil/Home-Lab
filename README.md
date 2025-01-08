# Home-Lab
In my Home Lab I run many things like Jellyfin, Jellyseer, Transmission, Radarr, Sonarr and much more. Most of these are deployed through Portainer.

# Setup

## Hardware & OS
For my Hardware I'm currently using a Dell Optiplex 5040 which I have refurbished. For the OS side of things I'm using Promox 8.3 to host everything.

### Specs:
- CPU: 4 x Intel(R) Core(TM) i5-6500 CPU @ 3.20GHz
- RAM: 16GB DDR3 1600MHz
- SSD: SAMSUNG SATA 2.5" 256GB (ZFS Pool 1)
- HDD: Seagate 1x1TB and 2x500GB (ZFS Pool 2)


## Portainer
Portainer is where I host most of the Arr Stack and the majority of my configuration.

### Arr Stack:
- Bazarr: Generating Subtitles for the Media
- [Deunhealth](https://github.com/qdm12/deunhealth): Monitoring if Containers are Healthy or not
- Flaresolverr: A Proxy Server to help Prowlarr with Indexers
- [Gluetun](https://github.com/qdm12/gluetun): Configured to go through my Surfshark VPN 
- Prowlarr: Using Indexers to find Torrents
- Radarr: Uses Prowlarr to find and request to download Movies
- Sonarr: Same as Radarr but with TV Shows
- Transmission: Downloads from the Torrents to get the actual Media

### Homepage Stack:
- [Mafl](https://github.com/hywax/mafl): Just a nice simple Homepage which I really like

### Jellyfin Stack:
- [Jellyseer](https://github.com/Fallenbagel/jellyseerr): Used to request Movies/Anime/TV Shows

## Shared Drive
I'm currently running Cockpit on an Ubuntu 22.04.5 LTS Virtual Machine as my Shared Drive. 

### Shares:
- Configuration
- Media

## Jellyfin
I run my Jellyfin instance on an LXC using one of the [Promox Helper Scripts](https://tteck.github.io/Proxmox/) which are great!

### Plugins:
- [Intro Skipper](https://github.com/intro-skipper/intro-skipper): I mean it's in the name, 50/50 on when it'll work
- Open Subtitles: Just in case Bazarr doesn't generate the Subtitles
- [Skin Manager](https://github.com/danieladov/jellyfin-plugin-skin-manager): Some nice Themes to put on the Jellyfin interface
- AniDB, Fanart, TheTVDB: Mostly for metadata like pictures, info about the movie etc.

## Inspiration
From my Home Lab setup I followed a lot of Tutorials from [TechHut](https://www.youtube.com/@TechHut) and he was super useful!
