# Tcpdump

## Common Options

* \-i : interface to listen on
* \-r : read capture file
* \-n : skip DNS resolution
* \-X : print packet data in both hex and ascii format
* \-A : print each packet

## Filters

### TCP Flags

```
sudo tcpdump -A -n 'tcp[tcpflags] & tcp-ack != 0'
```

