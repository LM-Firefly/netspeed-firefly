<p align="center"><a href="https://extensions.gnome.org/extension/3724/net-speed-simplified/"><img src="https://raw.githubusercontent.com/prateekmedia/netspeedsimplified/main/images/icon.png" height=80px alt="NSS Logo"/></a></p>
<h1 align="center">Net speed Simplified</h1>
<p align="center"><b>A Net Speed monitor With Loads of Customization.</b></p>
<p align="center">
<a href="https://github.com/LM-Firefly/netspeed-firefly/releases">
 <img alt="GitHub release" src="https://img.shields.io/github/v/release/LM-Firefly/netspeed-firefly"/></a> <a href="LICENSE"><img alt="License" src="https://img.shields.io/github/license/LM-Firefly/netspeed-firefly?color=blue"/></a>
</p>
<p align="center">
 <img src='https://extensions.gnome.org/extension-data/screenshots/screenshot_3724.gif' width="500px"  alt="Screenshot"/>
</p>
<table>
 <th colspan=2>
  <h6>Download options</h6>
 </th>
 <tr>
  <td>
   <a href="https://extensions.gnome.org/extension/3724/net-speed-simplified/">
    <img src="https://raw.githubusercontent.com/andyholmes/gnome-shell-extensions-badge/master/get-it-on-ego.svg?sanitize=true" height="100" alt="Get it on GNOME Extensions">
   </a>
  </td>
  <td>
   <a href="#installing-manually">
    <img alt="Install Manually" src="https://img.shields.io/badge/Install Manually-2 ways-blue"/>
   </a>
  </td>
 </tr>
 <tr>
  <td colspan=10>
 </tr>
 </td>
</table>

***Supports GNOME 45 and 46, for GNOME SHELL < 45 you can use the previous versions of this extension***

**Note** : Full CHANGELOG can be found on [github releases](https://github.com/LM-Firefly/netspeed-firefly/releases) page

#### Features

- [X] Cleaner UI
- [X] Adjustable Refresh rate
- [X] [Preference](#Feature-Highlights-for-Preferences) Menu for extension customization
- [X] *Vertical Alignment* Support
- [X] *Two Icon sets* for Indicators

#### Feature Highlights for Preferences

- [X] **Lock Mouse Actions** option to Freeze [Mouse Events](#mouse-events)
- [X] **Advance Position** options to pinpoint where to place the indicator on the Panel
- [X] **Refresh time** field by which you can change refresh rate value between 1 and 10 seconds
- [X] **Show Upload First** option to show upload speed first
- [X] **Color Customizations** for speed indicators
- [X] **Hide when Disconnected** option
- [X] **Use Shorten Units** option
- [X] **Limit Unit** option
  and more...

If you faced an **issue** then you can **[file an issue here](https://github.com/LM-Firefly/netspeed-firefly/issues)**

#### Modes

1. **Total net speed** in terms of bits per second
2. **Total net speed** in terms of bytes per second
3. **Up & down speed** in terms of bits per second
4. **Up & down speed** in terms of bytes per second
5. **Total downloads** in terms of bytes (Right click to reset counter)

#### Mouse Events

- **Left click**: Cycle through the [modes](#modes).
- **Right click(in 1-4 modes)**: Toggle the visibility of total transfer data.
- **Right click(in 5th mode)**: Reset total transfer data
- **Right Click(Four consecutive times)**: Toggle through horizontal/vertical alignment.
- **Middle click**: Cycle through the font sizes.

#### *Special Thanks to*

- [biji](https://github.com/biji) for Creating [simplenetspeed](https://github.com/biji/simplenetspeed)
- [m0hithreddy](https://github.com/m0hithreddy) for his support in rewriting extension.js with Clutter and rewriting readme.md, Adopting Make build system and more..
- [remisiki](https://github.com/remisiki) for adding support for GNOME 45
- [Know More](https://github.com/LM-Firefly/netspeed-firefly/graphs/contributors)

### Troubleshooting

#### VPN traffics calculated twice
- Some VPN software creates a tun/tap interface (eg. [WireGuard](https://wireguard.com), [OpenVPN](https://openvpn.net)) and traffics are being calculated twice. Currently interfaces with these naming scheme is filtered out, make sure the interface created by your VPN software fits one of the following:
  - `lo`: loop-back interface
  - `ifb[0-9]+`: intermediate functional block pseudo network interface
  - `lxdbr[0-9]+`: bridge interface created by [LXD](https://linuxcontainers.org/lxd/)
  - `virbr[0-9]+`: bridge interface created by [LibVirt](https://libvirt.org)
  - `docker[0-0]+`: bridge interface created by [Docker](https://docker.com)
  - `veth[0-9a-zA-Z]+`: virtual network interface created by [Docker](https://docker.com)
  - `br[0-9]+`: bridge interface
  - `vnet[0-9]+`: virtual network interface
  - `tun[0-9]+`: TUN (l3 tunnel) interface
  - `tap[0-9]+`: TAP (l2 tunnel) interface
  - `wg[0-9]+`: tunnel interface created by [WireGuard](https://wireguard.com)
  - `waydroid[0-9]+`: tunnel interface created by [Waydroid](https://waydro.id)

<h2 align="center">Installing Manually</h2>

### Installing using Make

- **Step 1** : Getting the sources from repository

```bash
git clone "https://github.com/LM-Firefly/netspeed-firefly.git"
```

- **Step 2** : Running make (install)

```bash
make install
```

Likewise extension can be **removed** using

```bash
make remove
```

OR **reinstalled** using

```bash
make reinstall
```

You can manage the extension using extensions app or [website](https://extensions.gnome.org/local)
