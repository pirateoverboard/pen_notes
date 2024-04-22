
to set mac address discovery OUI:
`sudo setcap cap_net_raw+p /usr/sbin/arp-scan`

to scan all from network interface:
`arp-scan -l -I eth1`