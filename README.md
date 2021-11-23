## ubuntu_references
You can refer
## raspberry pi config
### VNC
```
dpkg --add-architecture armhf
sudo apt update
sudo apt install ./VNC-Server-6.6.0-Linux-ARM.deb
rm -rf ./VNC-Server-6.6.0-Linux-ARM.deb
dpkg --remove-architecture armhf
sudo apt update
systemctl enable vncserver-x11-serviced.service
systemctl start vncserver-x11-serviced.service
```
[Source](https://github.com/openfans-community-offical/Debian-Pi-Aarch64/issues/51)

