# Masscan

## Common Options

* \-p \<port> : port(s) to scan
* \--rate \<number> : packet transmission rate
* \-e \<id> : network interface to use
* \--router-ip \<ip> : appropriate gateway address

## Example

```
$ sudo masscan -p80 10.0.0.0/24 --rate=1000 -e eth0 --router-ip 10.0.0.1
```
