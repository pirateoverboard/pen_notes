┌──(user㉿kali)-[~]
└─$ hashcat -m 0 hashes.txt /usr/share/wordlists/metasploit/password.lst
hashcat (v6.2.6) starting

OpenCL API (OpenCL 3.0 PoCL 4.0+debian  Linux, None+Asserts, RELOC, SPIR, LLVM 15.0.7, SLEEF, DISTRO, POCL_DEBUG) - Platform #1 [The pocl project]
==================================================================================================================================================
* Device #1: cpu-skylake-avx512-11th Gen Intel(R) Core(TM) i7-11800H @ 2.30GHz, 1428/2921 MB (512 MB allocatable), 6MCU

Minimum password length supported by kernel: 0
Maximum password length supported by kernel: 256

Hashes: 1 digests; 1 unique digests, 1 unique salts
Bitmaps: 16 bits, 65536 entries, 0x0000ffff mask, 262144 bytes, 5/13 rotates
Rules: 1

Optimizers applied:
* Zero-Byte
* Early-Skip
* Not-Salted
* Not-Iterated
* Single-Hash
* Single-Salt
* Raw-Hash

ATTENTION! Pure (unoptimized) backend kernels selected.
Pure kernels can crack longer passwords, but drastically reduce performance.
If you want to switch to optimized kernels, append -O to your commandline.
See the above message to find out about the exact limits.

Watchdog: Hardware monitoring interface not found on your system.
Watchdog: Temperature abort trigger disabled.

Host memory required for this attack: 0 MB

Dictionary cache built:
* Filename..: /usr/share/wordlists/metasploit/password.lst
* Passwords.: 88398
* Bytes.....: 820674
* Keyspace..: 88398
* Runtime...: 0 secs

<mark>cd73502828457d15655bbd7a63fb0bc8:student</mark>                  
                                                          
Session..........: hashcat
<mark>Status...........: Cracked</mark>
Hash.Mode........: 0 (MD5)
Hash.Target......: cd73502828457d15655bbd7a63fb0bc8
Time.Started.....: Sat Sep 16 09:30:08 2023 (0 secs)
Time.Estimated...: Sat Sep 16 09:30:08 2023 (0 secs)
Kernel.Feature...: Pure Kernel
Guess.Base.......: File (/usr/share/wordlists/metasploit/password.lst)
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:  1417.0 kH/s (0.07ms) @ Accel:256 Loops:1 Thr:1 Vec:16
Recovered........: 1/1 (100.00%) Digests (total), 1/1 (100.00%) Digests (new)
Progress.........: 76800/88398 (86.88%)
Rejected.........: 0/76800 (0.00%)
Restore.Point....: 75264/88398 (85.14%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidate.Engine.: Device Generator
Candidates.#1....: stroud -> syncopation

Started: Sat Sep 16 09:29:50 2023
Stopped: Sat Sep 16 09:30:09 2023

<mark>Password = student</mark>
