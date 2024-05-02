
### Configure virt-viewer dual screens

- Find VM name:
	- `sudo virsh list --all`
- Find network name and start it
	- `sudo virsh net-list`
	- Start domain if not started
		- `sudo virsh net-start --domain <network>`
- Change xml config
	- `sudo virsh edit <VM_name>`
		- Change:  heads='1' to heads='2'
- Edit `nano ~/.config/virt-viewer/settings`
	-  add to end of list
		- ``` [fallback]
			monitor-mapping=1:1;2:2
- Install spice-vgagent inside linux vm & reboot
- Start VM
	-  `sudo virsh start --domain <VM_name> && virt-viewer --connect qemu:///system <VM_name> &`
