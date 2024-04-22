
Need to know version information

`msfconsole`

Auxiliary are enumeration
`search smb`

`use auxillary/scanner/smb/smb_version`
#### Show info and options
`info` OR `options`

#### Set options
`set RHOSTS <IP>`

#### Run
`run`

### smbclient
`smbclient -L \\\\<IP>\\`

can use `-U guest`
`-W WORKGROUP`
`-m SMB1`

shows fileshare
`smbclient \\\\<IP>\\<SHARE>`

#### Nmap
`nmap --script "safe or smb-enum-*" -p 445 <IP>`



