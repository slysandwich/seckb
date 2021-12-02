# Nmap

## Common Options

* \-sS : SYN scan
* \-sT : CONNECT scan
* \-sU : UDP scan
* \-sn : network sweep
* \-p \<port(s)> : port(s) to scan
* \-iL \<file> : targets input file
* \-oG \<file> : save results in greppable format
* \-O : OS fingerprinting
* \-sV : service banners
* \-sC : default scripts set
* \-A : OS fingerprinting, script scanning and traceroute
* \--script \<name> : load NSE script(s)

## Static Binary

* [https://github.com/ZephrFish/static-tools/blob/master/nmap/nmap](https://github.com/ZephrFish/static-tools/blob/master/nmap/nmap)

## All ports TCP Scan

```
sudo nmap -sS -T4 -p- <IPs>
```

## UDP Scan

```
nmap -sU -T4 --open <IPs>
```

## SMB Scanning

```
# Discover listening SMB servers
$ nmap -v -p 139,445 -oG smb.txt 10.0.0.1-254

# Run all SMB plugins on target host
$ nmap -p 139,445 --script smb* 10.0.0.1

# Run MS08-067 plugin on target host
$ nmap -v -p 139,445 --script=smb-vuln-ms08-067 --script-args=unsafe=1 10.0.0.1
```

## Extensive Host Scanning

```
nmap -Pn -sT -A -p- --reason --script=vuln --script-args=unsafe <IP>
nmap -sU --top-ports=1000 <IP>
```
