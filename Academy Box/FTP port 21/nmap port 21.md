
┌──(user㉿kali)-[~]
└─$ nmap -T4 -p21,22,80 -A 192.168.100.178
Starting Nmap 7.94 ( https://nmap.org ) at 2023-09-16 09:06 CDT
Nmap scan report for academy.isloated (192.168.100.178)
Host is up (0.00045s latency).

PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 3.0.3
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:192.168.100.191
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 1
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_-rw-r--r--    1 1000     1000          776 May 30  2021 note.txt
