┌──(user㉿kali)-[~]
└─$ ftp 192.168.100.178
Connected to 192.168.100.178.
220 (vsFTPd 3.0.3)
Name (192.168.100.178:user): anonymous
331 Please specify the password.
Password: 
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls
229 Entering Extended Passive Mode (|||32981|)
150 Here comes the directory listing.
-rw-r--r--    1 1000     1000          776 May 30  2021 note.txt
226 Directory send OK.