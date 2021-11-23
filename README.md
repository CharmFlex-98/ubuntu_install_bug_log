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

sudo wget -P /usr/lib \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libbcm_host.so \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libvcos.so \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libmmal.so \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libmmal_core.so \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libmmal_components.so \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libmmal_util.so \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libmmal_vc_client.so \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libvchiq_arm.so \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libvcsm.so \
https://github.com/raspberrypi/firmware/raw/master/opt/vc/lib/libcontainers.so

systemctl enable vncserver-x11-serviced.service
systemctl start vncserver-x11-serviced.service
```
[Source](https://github.com/openfans-community-offical/Debian-Pi-Aarch64/issues/51)

