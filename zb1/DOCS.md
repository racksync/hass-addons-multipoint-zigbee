# Home Assistant - Run multipoint Zigbee2MQTT Coordinator separately from an Official 

[![Base Image](https://img.shields.io/badge/Base%20Image-3.18-blue)](https://github.com/home-assistant/docker-base)  [![alpine-armhf](https://img.shields.io/badge/armhf-yes-brightgreen)](https://alpinelinux.org/releases/) 
[![alpine-armv7](https://img.shields.io/badge/armv7-yes-brightgreen)](https://alpinelinux.org/releases/) 
[![alpine-aarch64](https://img.shields.io/badge/aarch64-yes-brightgreen)](https://alpinelinux.org/releases/) 
[![alpine-amd64](https://img.shields.io/badge/amd64-yes-brightgreen)](https://alpinelinux.org/releases/) 
[![alpine-i386](https://img.shields.io/badge/i386-yes-brightgreen)](https://alpinelinux.org/releases/)
[![cloudflare-argo-tunnel-release](https://img.shields.io/github/v/release/racksync/hass-addons-multipoint-zigbee)](https://github.com/racksync/hass-addons-multipoint-zigbee/releases) [![last commit](https://img.shields.io/github/last-commit/racksync/hass-addons-multipoint-zigbee)](https://github.com/racksync/hass-addons-multipoint-zigbee/commit/)

## Disclaimer ###

Suitable for those who want to run zigbee2mqtt and can separate the Coordinator's work at more than 1 point.

## How to Install Add-on

1) Install the addon by adding the repository: https://github.com/racksync/hass-addons-suite to the addon list as usual.
2) Set the addon configuration as follows:
- serial config
```yaml
port: tcp://ip-address:6638
adapter: zstack
baudrate: 115200
disable_led: false
advanced:
  transmit_power: 20
```
- Each addon's specified network port must not be the same. For example, ZB #1 runs with default:```8485```. If you want to run another one (ZB #2), you must change the port so they don't collide, such as ```8486```.

3) Edit the topic in the mqtt setting section (edit through the main zigbee config page) in the **setting -> MQTT** menu. The Base topic must not be the same.

4) Run all Addons at the same time and start Pairing as usual.


### Automation Training

- [Products and Services](http://racksync.com)
- [Training Courses](https://facebook.com/racksync)

### Community

- [Home Automation Thailand](https://www.facebook.com/groups/hathailand)
- [Home Automation Marketplace](https://www.facebook.com/groups/hatmarketplace)
- [Home Automation Thailand Discord](https://discord.gg/Wc5CwnWkp4) 

### [RACKSYNC CO., LTD.](https://racksync.com)

RACKSYNC CO., LTD. is an expert in Automation and Smart Solutions of all sizes. We offer consulting services, system layout, installation, and monitoring by experts. In addition, we are a company that develops full-circle Software As A Service.
\
\
RACKSYNC COMPANY LIMITED \
Suratthani, Thailand 84100 \
Email : devops@racksync.com \
Tel : +66 85 880 8885 

[![Home Automation Thailand Discord](https://img.shields.io/discord/986181205504438345?style=for-the-badge)](https://discord.gg/Wc5CwnWkp4) [![Github](https://img.shields.io/github/followers/racksync?style=for-the-badge)](https://github.com/racksync) 
[![WebsiteStatus](https://img.shields.io/website?down_color=grey&down_message=Offline&style=for-the-badge&up_color=green&up_message=Online&url=https%3A%2F%2Fracksync.com)](https://racksync.com)