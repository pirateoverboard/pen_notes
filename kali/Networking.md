
Configure 2 interfaces: `sudo nano /etc/network/interfaces`
```
# Add this to file

allow-hotplug eth0
auto eth0
iface eth0 inet dhcp

allow-hotplug eth1
auto eth1
iface eth1 inet dhcp
```

`sudo service networking restart`

`echo "nameserver $(route | grep default | awk '{print $2}')" | sudo tee /etc/resolv.conf`


`echo `

%% 
Disable dhclient from writing to /etc/resolv.conf
`sudo cp /etc/dhcp/dhclient.conf /etc/dhcp/dhclient.conf.bak`
`sudo nano /etc/dhcp/dhclient.conf`

delete requested items dns items from request line:
domain-name, domain-name-servers, domain-search,

add `supersede domain-name-servers 192.168.122.1, 192.168.100.1;`

Restart dhclient request:
`sudo dhclient -v` %%

### Disable programs from writing /etc/resolv.conf
`sudo apt install openresolv`

`sudo nano /etc/resolvconf.conf`

%% ADD:
`resolvconf=NO` %%

