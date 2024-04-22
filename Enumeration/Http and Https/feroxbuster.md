
`sudo apt install feroxbuster`


#### filter out 404 | follow redirects | use ext. | write to file
`feroxbuster -C 404 -r -u http://192.168.100.201/ -x php,xml,txt --force-recursion --add-slash  -d 0 -o test.txt`

```
-C 404 # Ignore 404
-r follow redirects
-u URL
-x extensions
-d 0 # depth unlimited
-w # use wordlist
```
