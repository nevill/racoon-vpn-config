# Racoon Based IPSec Configuration

#### NOTE

Server IP here is described as `1.1.1.1`, should be replace with yours

## Brief of a site-to-site network

### Home Site

* wan - dynamically assigned IP
* network - 192.168.1.0/24
* gateway - 192.168.1.1

### Remote Site

* wan IP - 1.1.1.1
* internal IP - 10.9.9.1

## Server

### Supports 2 types of connections

* IPSec connection only, for site to site VPN connection, use OpenWrt as client
* IPSec with L2tpd (via xl2tpd), to support iOS device as client

### Software

* OS - Debian Wheezy (7.5)
* iptables
* racoon
* danted (optional, socks server)

## Client

Using OpenWrt as router

### Software

* opkg install ipsec-tools kmod-ipsec4

## Reference

* [Use racoon on OpenWrt](http://wiki.openwrt.org/doc/howto/vpn.ipsec.basics.racoon)
* [A Sample of racoon configuration](http://www.mad-hacking.net/documentation/linux/networking/ipsec/dynamic-nat-vpn.xml)
* [Explanation on iptables](https://www.frozentux.net/iptables-tutorial/iptables-tutorial.html)
