# Snmp-check

## Common Options

* \-c \<string> : community string. Default is public
* \-p \<port> : SNMP port. Default is 161
* \-v \<version> : SNMP version. Default is 1
* \-w : detect write access
* \-t \<seconds> : timeout in seconds. Default is 5

## Example

```
$ snmp-check -t 10 <IP>
```
