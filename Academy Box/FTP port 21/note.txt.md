# Information Disclosure
ftp> get note.txt
local: note.txt remote: note.txt
229 Entering Extended Passive Mode (|||61394|)
150 Opening BINARY mode data connection for note.txt (776 bytes).
100% |******************************************************************************|   776        2.02 MiB/s    00:00 ETA
226 Transfer complete.
776 bytes received in 00:00 (864.09 KiB/s)
ftp> quit
221 Goodbye.

┌──(user㉿kali)-[~]
└─$ cat note.txt        
Hello Heath !
Grimmie has setup the test website for the new academy.
I told him not to use the same password everywhere, he will change it ASAP.


I couldn't create a user via the admin panel, so instead I inserted directly into the database with the following command:

INSERT INTO `students` (`StudentRegno`, `studentPhoto`, `password`, `studentName`, `pincode`, `session`, `department`, `semester`, `cgpa`, `creationdate`, `updationDate`) VALUES
('10201321', '', <mark>'cd73502828457d15655bbd7a63fb0bc8'</mark>, 'Rum Ham', '777777', '', '', '', '7.60', '2021-05-29 14:36:56', '');

The StudentRegno number is what you use for login.


Le me know what you think of this open-source project, it's from 2020 so it should be secure... right ?
We can always adapt it to our needs.

-jdelta

highlighted above is an MD5 hash of password