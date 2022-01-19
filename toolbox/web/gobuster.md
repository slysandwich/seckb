# Gobuster

## Running Through a SOCKS Proxy

```
HTTP_PROXY="socks5://127.0.0.1:1080/" ./gobuster
```

## Examples

### Quick Directory Busting

```
gobuster -u 127.0.0.1 -w /usr/share/seclists/Discovery/Web_Content/common.txt -t 80 -a Linux
```

### Comprehensive Directory Busting

```
gobuster -s 200,204,301,302,307,403 -u 127.0.0.1 -w /usr/share/seclists/Discovery/Web_Content/big.txt -t 80 -a 'Mozilla/5.0 (X11; Linux x86_64; rv:52.0) Gecko/20100101 Firefox/52.0'
```

### Search with File Extension

```
gobuster -u 127.0.0.1 -w /usr/share/seclists/Discovery/Web_Content/common.txt -t 80 -a Linux -x .txt,.php
```
