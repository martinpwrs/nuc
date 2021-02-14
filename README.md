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
## SSH Server
[Ubuntu documentation](https://ubuntu.com/server/docs/service-openssh)
```
sudo apt install openssh-server
(press y)
sudo systemctl enable ssh
```

## Docker
[Install using the repository](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)

Add myself to Docker group: `sudo usermod -aG docker martin`

## Portainer
[Run through docker](https://portainer.readthedocs.io/en/stable/deployment.html)
Access at nuc.local:9000

## Other
Helpful pages along the way: https://medium.com/@jordanrounds/intel-nuc-home-assistant-supervised-7cc52d81744a
