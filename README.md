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

## Plex
https://www.linuxbabe.com/debian/install-plex-media-server-debian-10-buster
https://www.plex.tv/media-server-downloads/


## Portainer
[Run through docker](https://portainer.readthedocs.io/en/stable/deployment.html)
Access at nuc.local:9000

## Other
Helpful pages along the way: https://medium.com/@jordanrounds/intel-nuc-home-assistant-supervised-7cc52d81744a
