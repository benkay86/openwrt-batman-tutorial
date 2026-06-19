## Required software

The default OpenWRT packages do not support wireless mesh or batman mesh routing by default. The following packages are required for 802.11s mesh + batman:

- `kmod-batman-adv` kernel support for batman
- `luci-proto-batman-adv` web interface support for batman
- `wpad-mesh-wolfssl` or `wpad-mesh-openssl` (instead of `wpad-basic-mbedtls`) web interface support for 802.11s mesh

The following packages are recommended in general if you have enough space on the router's flash memory:

- `luci-app-opkg` to install software from the web interface
- `luci-ssl` (instead of `luci`) to access the web interface over https
- `nano` to edit text files from an ssh terminal

### Creating a custom firmware image

Creating a custom firmware image is recommended and [quite easy using OpenWRT's website](required_software/custom_firmware.md). Using custom firmware saves space on the router's read/write partition and speeds deployment since the software you need is already installed.

### Installing packages

If you have already flashed your router and don't wish to flash a new firmware image, you can [install software packages using the web interface](required_software/installing_packages.md).