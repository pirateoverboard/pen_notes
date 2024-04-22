DNS takeover attacks better than responder/smb relay

DNS takeover more reliable

Most windows machine default to IPv4 for dns and no dns on IPv6

Mitm6

Mitigation Strategies:
- if ipv6 is not used, disable DHCPv6 traffic and incoming router advertisments in windows firewall via group policy. Disabling IPv6 entirely may have unwanted side effects. Setting the following rules to block instead of allow prevents the attack from working:
	- (Inbound) Core Networking - Dynamic Host Configuration Protocol for IPv6(DHCPv6-In)
	- (Inbound) Core Networking - Router Advertisement (ICMPv6-In)
	- (Outbound) Core Networking - Dynamic Host Configuration Protocol for IPv6 (DHCPv6 - Out)

- If WPAD is not in use internally, disable it via Group Policy and disable the WinHttpAutoProxySvc service.
- Relaying to LDAP and LDAPS can only be mitigated by enabling both LDAP signing and LDAP channel binding.
- Consider Administrative users to the Protective Users group or marking them as Account is sensitive and cannot be delegated, which will prevent any impersonation of that user via delegation.
