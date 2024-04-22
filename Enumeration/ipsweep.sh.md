
```
#!/bin/bash

if [ "$1" == ""]; then
	echo "you forgot an IP address like: 192.168.1"
else
	for ip in `seq 1 254`; do
	ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &
	done
fi
```

usee:
`./ipsweep.sh 192.168.x >> ips.txt`

note: using ; at end only one process at a time & allows multiple

One liner:

`for ip in $(cat ips.txt); do nmap $ip; done`