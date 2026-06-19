## Configuring client nodes

The gateway mesh node connected to the Internet/WAN has been configured. Now you will want to configure several mesh satellite, or client nodes. The client nodes will be bridged to the gateway node on OSI layer 2 via the batman mesh, so the client nodes do not need to perform (and should not perform) any OSI layer 3 functions such as DHCP lease assignment, firewall/packet filtering, or routing. In fact, having the client nodes try to provide this functionality would interfere with proper operation of the mesh network!

Thus, **before** you add your client node to the mesh using the steps above, you will want to configure the client nodes as ["dumb" access points](https://openwrt.org/docs/guide-user/network/wifi/dumbap). You will likely still want to give the client nodes IP addresses on the lan so that you can log into them for maintenance and diagnostics.

### Setting a static IP address

First, [give the client node a static IP address](client_nodes/static_ip.md) so that you can continue to access it during the other configuration steps. See below for IPv6 configuration.

### Disabling Layer 3 services

Next, you will want to [disable the DHCP server, DNS sever, and firewall](client_nodes/layer3.md) so that the client node will not conflict with the gateway node providing these service.

### Connecting client nodes to the mesh

Now it is safe for your client note to [join the mesh](client_nodes/mesh.md) and begin routing traffic.

### Using the WAN port as a LAN port

Assuming you have elected to [bridge the lan to the mesh](bridge_lan_to_mesh.md), you can plug an ethernet-connected device such as a desktop computer with no wireless card into the LAN port of your client node and it will be connected to your home network and the Internet. Cool! The ASUS Lyra has a second ethernet port, the WAN port, that is typically connected to your Internet modem. Since the client node will not be connected directly to the Internet modem, you can [repurpose the WAN port](client_nodes/wan_as_lan.md) to serve a second ethernet connected device.

### IPv6 connectivity

Wireless and ethernet devices connecting via the client mesh node can already receive IPv6 address normally. Although not typically necessary, if you want, you may [configure the client node itself to have an IPv6 address](client_nodes/ipv6.md).