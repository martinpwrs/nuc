# Hardware
## nuc
model nuc7i5bnh

bios: BNKBL357 BN0083.bio

Update bios: https://downloadcenter.intel.com

# Software
## OS
Debian 10
image: 
burned with: balenaEtcher-1.5.116


# Installations
## Debian user sudo
```
su
[enter root password]
sudo visudo
[ADD martin ALL=(ALL:ALL) ALL]
```

## SSH Server
```
sudo apt install openssh-server
(press y)
sudo systemctl enable ssh
```
## Home Assistant
### Docker CE
https://docs.docker.com/engine/install/debian/

### Install other possible dependencies
```
sudo apt-get install \
  apparmor-utils \
  avahi-daemon \
  dbus \
  jq \
  network-manager \
  socat
```
### Confirm Other versions
```
systemd --version
apt list network-manager
apt list apparmor
```

### Home Assistant
```
curl -Lo installer.sh https://raw.githubusercontent.com/home-assistant/supervised-installer/master/installer.sh
sudo bash installer.sh --machine intel-nuc
```

NOTE: Set `--data-share /media/storage/hassio` if mounting larger drive and `--sysconfdir ` if wanted.

## Plex
https://www.linuxbabe.com/debian/install-plex-media-server-debian-10-buster
https://www.plex.tv/media-server-downloads

https://github.com/linuxserver/docker-plex

[Access](http://nuc.local:32400/)

## Portainer
[Run through docker](https://portainer.readthedocs.io/en/stable/deployment.html)
[Access](http://nuc.local:9000)

## SABNZBD
Download agent

https://hub.docker.com/r/linuxserver/sabnzbd

[Access](http://nuc.local:8080/sabnzbd)

## Sonarr
TV

https://github.com/linuxserver/docker-sonarr

[Access](http://nuc.local:8989)

## Radarr
Movies

https://github.com/linuxserver/docker-radarr

[Access](http://nuc.local:7878)

## Lidarr
Music

https://github.com/linuxserver/docker-lidarr

[Access](http://nuc.local:8686)

## Jackett
Torrent Finder

https://github.com/linuxserver/docker-jackett

[Access](http://nuc.local:9117)

## pyload
Torrent Finder

https://github.com/linuxserver/docker-pyload

[Access](http://nuc.local:8001)

## Bazarr 
TV and Movie subtitles

https://github.com/linuxserver/docker-bazarr

[Access](http://nuc.local:6767)

## Lazy Librarian
Books

https://github.com/linuxserver/docker-lazylibrarian

[Access](http://nuc.local:5299)

## Lychee
Photo

https://github.com/linuxserver/docker-lychee

## Other
Helpful pages along the way: https://medium.com/@jordanrounds/intel-nuc-home-assistant-supervised-7cc52d81744a
