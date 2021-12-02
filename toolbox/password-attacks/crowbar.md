---
description: Suitable for SSH with private key, RDP, VNC with key, OpenVPN
---

# Crowbar

## Documentation

* [https://github.com/galkan/crowbar](https://github.com/galkan/crowbar)

## Common Options

* \-b : protocol
* \-s : target server
* \-u : username
* \-C : wordlist
* \-n :  number of threads

## Examples

### RDP

```
crowbar -b rdp -s 10.0.0.1/32 -u admin -C /usr/share/wordlists/rockyou.txt -n 1
```
