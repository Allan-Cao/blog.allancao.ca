---
title: "Installing Cisco Packettracer on Ubuntu 24.04"
categories:
- tech
- software
tags:
- ubuntu
- ubuntu-24.04
---

# Fix broken dependencies

Apparently `libgl1-mesa-glx` is an obsolete packet which is depended on by cisco packet tracer. Here is how to fix the unmet dependency:

```bash
wget http://archive.ubuntu.com/ubuntu/pool/universe/m/mesa/libgl1-mesa-glx_23.0.4-0ubuntu1~22.04.1_amd64.deb
sudo dpkg -i libgl1-mesa-glx_23.0.4-0ubuntu1~22.04.1_amd64.deb
sudo dpkg -i Packet_Tracer822_amd64_signed.deb
```
