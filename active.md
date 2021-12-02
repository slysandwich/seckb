# Active

## Network

### Sweeping

```
$ nmap -sn
```

Windows:

```
for /L %i in (1,1,255) do @ping -n 1 -w 200 10.0.0.%i > nul && echo 10.0.0.%i is up.
```

### Port Scanning

* [Nmap ](toolbox/network/nmap.md)(TCP & UDP)
  * [Extensive host scanning](toolbox/network/nmap.md#extensive-host-scanning)
* [Masscan](toolbox/network/masscan.md)
* [Netcat](toolbox/network/netcat.md)
* Bash

```
#!/bin/bash
host=<ip>
for port in {1..65535}; do
    timeout .1 bash -c "echo >/dev/tcp/$host/$port" &&
        echo "port $port is open"
done
echo "Done"
```

### UDP Services Recon

* [https://github.com/CiscoCXSecurity/udp-proto-scanner](https://github.com/CiscoCXSecurity/udp-proto-scanner)

### IPv6

* [https://blog.zsec.uk/ipv6-pwn/](https://blog.zsec.uk/ipv6-pwn/)

## DNS

Goal: Enumeration & zone transfer

```
host -t ns target.com
dig a target.com @nameserver
dig mx target.com @nameserver
dig axfr target.com @nameserver
```

### Tools

* [DNSrecon](toolbox/network/dnsrecon.md)
* [DNSenum](toolbox/network/dnsenum.md)

### Lists

* [https://github.com/danielmiessler/SecLists/tree/master/Discovery/DNS](https://github.com/danielmiessler/SecLists/tree/master/Discovery/DNS)

## SMB

* [Nmap ](toolbox/network/nmap.md)-p139,445 --script smb\*
* [nbtscan](toolbox/network/nbtscan.md) -r \<IP range>
* [enum4linux.pl](toolbox/network/enum4linux.md)

Download everything in a share:

```
smbclient /<IP>/Replication
recurse ON
prompt OFF
mget *
```

Mounting a share:

```
mount -t cifs -o username=Administrator,password=Password123$ //<IP>/C$ /mnt/winxp/
mount -t cifs //<IP>/Replication /mnt/Replication -o username=<username>,password=<password>,domain=<domain>
```

Test NULL connect:

```
rpcclient -U "" 127.0.0.1
```

## NFS

* [Nmap ](toolbox/network/nmap.md)-p111 --script nfs\*
* [Nmap ](toolbox/network/nmap.md)-sV -p111 --script rpcinfo

```
# If a share is mountable
$ mkdir <SHARE>
$ sudo mount -o nolock <IP>:/<SHARE> ~/<SHARE>/

# Depending on the rights, create a user with appropriate uid/gid
$ sudo adduser woot
$ sudo sed -i -e 's/<CURRENT UID>/<TARGET UID>/g' /etc/passwd
```

## SMTP

* [Nmap ](toolbox/network/nmap.md)-p25,465,587 --script=smtp\*
*   Commands:

    ```
    VRFY <account> (verify an email account)
    EXPN <mailing-list> (list mailing list members)
    ```

## SNMP

* [Nmap ](toolbox/network/nmap.md)-sU -p 161 --open
* [onesixtyone](toolbox/network/onesixtyone.md)

```
$ echo public > community
$ echo private >> community
$ echo manager >> commnity
$ onesixtyone -c community -i ips_file
```

* [snmpwalk ](toolbox/network/snmpwalk.md)-c public -v1 -t 10 $ip \[$mib\_value]
* [Snmp-check](toolbox/network/snmp-check.md)

[https://github.com/danielmiessler/SecLists/tree/master/Discovery/SNMP](https://github.com/danielmiessler/SecLists/tree/master/Discovery/SNMP)

## Web

#### Technology Stack

* Programming language & framework
* Web server software
* Database software
* Server operating system

#### Manual

* Check source code
* Check response headers
* Check robots.txt & sitemap.xml
* Locate admin consoles
  * /manager/html (Tomcat)
  * /phpmyadmin

#### Reconnaissance

* [Dirb](https://tools.kali.org/web-applications/dirb) / Dirbuster / [gobuster](toolbox/web/gobuster.md)
* [Nikto](https://tools.kali.org/information-gathering/nikto)
* [Skipfish](https://tools.kali.org/web-applications/skipfish)
* [Wpscan](https://tools.kali.org/web-applications/wpscan) (if running Wordpress)
* dotdotpwn
* davtest\cadevar
* droopscan
* joomscan
* magescan
* [FinalRecon](https://github.com/thewhiteh4t/FinalRecon)
* [Feroxbuster](https://github.com/epi052/feroxbuster)
* [wfuzz](https://github.com/xmendez/wfuzz)
* [goWAPT](https://github.com/dzonerzy/goWAPT)
* [ffuf](https://github.com/ffuf/ffuf)



* [https://github.com/danielmiessler/SecLists/tree/master/Discovery/Web-Content](https://github.com/danielmiessler/SecLists/tree/master/Discovery/Web-Content)
* [https://github.com/danielmiessler/SecLists/blob/master/Miscellaneous/wordlist-skipfish.fuzz.txt](https://github.com/danielmiessler/SecLists/blob/master/Miscellaneous/wordlist-skipfish.fuzz.txt)

## Others

* [https://github.com/nyxgeek/lyncsmash](https://github.com/nyxgeek/lyncsmash)
* [https://github.com/sensepost/SPartan](https://github.com/sensepost/SPartan)

