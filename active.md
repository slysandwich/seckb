# Network Scanning

## Tools

* [AutoRecon](https://github.com/Tib3rius/AutoRecon)
* [Reconnoitre](https://github.com/codingo/Reconnoitre)

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

