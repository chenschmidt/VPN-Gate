# VPN-Gate

# vpn.py

This script allows to use the free VPN service provided by [VPNGate](http://www.vpngate.net/en/) in an easy way. The user just needs to provide the desidered output country, and the script automatically chooses the best server.

After this step, OpenVPN is launched with the proper configuration. The VPN can be terminated by pressing <kbd>Ctrl</kbd>+<kbd>C</kbd>.

# Usage

Run the script by providing the desired output country:

    vpn.py US

Both country codes and country names are supported, as listed on the VPNGate website, e.g.:

    vpn.py "United Kingdom"

Moreover, the script allows to input countries with **any case** (`Italy`, `italy`, `ItALy` all work) and with **partial names**:
- `Korea` will work for `Korea Republic Of`
- `Russia` will work for `Russian Federation`
- ... and so on

# Requirements

OpenVPN needs to be installed.

- Install Indicator: $ `sudo apt-get install gir1.2-appindicator3-0.1 gir1.2-notify-0.7 python-gobject`
- openvpn: $ `sudo apt-get install openvpn`
- python-urwid 1.3+: $ `sudo apt-get install python-urwid-doc`
- wmctrl: $ `sudo apt-get install wmctrl`

The script should run on any Linux distribution with the Python [Requests](python-requests.org) module installed. The user running the script must be able to run `sudo` commands in order to start `openvpn`.
