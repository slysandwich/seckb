# Snmpwalk

## Common Options

* \-c : community string
* \-t \<seconds> : timeout period
* \-v\<int> : SNMP version

## Example

```
$ snmpwalk -c public -v1 -t 10 <IP> [MIB_VALUE]
```

## MIB Values

{% content-ref url="../windows/snmp-windows.md" %}
[snmp-windows.md](../windows/snmp-windows.md)
{% endcontent-ref %}

