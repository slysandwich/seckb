# Hashcat

## Examples

```
# SHA512 $6$ shadow file 
hashcat -m 1800 -a 0 hash.txt rockyou.txt --username

# MD5 $1$ shadow file  
hashcat -m 500 -a 0 hash.txt rockyou.txt --username

# MD5 Apache webdav file  
hashcat -m 1600 -a 0 hash.txt rockyou.txt

# SHA1  
hashcat -m 100 -a 0 hash.txt rockyou.txt --force

# Wordpress  
hashcat -m 400 -a 0 --remove hash.txt rockyou.txt
```
