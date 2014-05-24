Racoon Based IPSec Configuration

!! Server IP in here is described as `1.1.1.1`, should be replace with yours

Site to site VPN network

Home Site

wan - dynamically assigned IP
network 192.168.1.0/24
gateway 192.168.1.1

Remote Site

wan 1.1.1.1
internal IP 10.9.9.1

Server

Supports 2 types of connections

* IPSec connection only, for site to site VPN connection, use OpenWrt as client
* IPSec with L2tpd (via xl2tpd), to support iOS device as client

Software

* OS - Debian Wheezy (7.5)
* iptables
* racoon
* danted (optional, socks server)

Client

OpenWrt as router, a site to site VPN configuartion

Software

* opkg install ipsec-tools kmod-ipsec4

Reference

* http://wiki.openwrt.org/doc/howto/vpn.ipsec.basics.racoon
* http://www.mad-hacking.net/documentation/linux/networking/ipsec/dynamic-nat-vpn.xml
* https://www.frozentux.net/iptables-tutorial/iptables-tutorial.html (explanation on iptables)
