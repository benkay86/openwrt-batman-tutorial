# OpenWRT Batman Mesh Tutorial

This tutorial is based on the YouTube guide by [OneMarcFifty](https://www.onemarcfifty.com/), [DIY MESH WiFi with batman-adv and OpenWrt](https://www.youtube.com/watch?v=t4A0kfg2olo). Also check out [Carlos Gomez's OpenWRT batman mesh guide](https://cgomesu.com/blog/Mesh-networking-openwrt-batman/), which shows how to set everything up on the command line. This tutorial assumes familiarity with OpenWRT, installing/flashing OpenWRT, home wireless networks, and the [OSI Model](https://osi-model.com/). The tutorial will demonstrate the simplest way to set up an 802.11s mesh network using the [batman routing protocol](https://www.open-mesh.org/projects/batman-adv/wiki) and OpenWRT's LuCI web interface. Unlike [OneMarcFifty](https://www.onemarcfifty.com/)'s tutorial, we will not delve into VLAN's.

The tutorial is divided into six chapters:

1. [Design a mesh network](chapters/design.md)
2. [Install required software packages](chapters/required_software.md)
3. [Configure batman interfaces](chapters/configure_batman_interfaces.md)
4. [Bridge LAN to the mesh](chapters/bridge_lan_to_mesh.md)
5. [Wireless configuation](chapters/wireless.md)
6. [Create additional mesh nodes](chapters/configuring_client_nodes.md)
7. [Speedy optimizations](chapters/optimizations.md)
