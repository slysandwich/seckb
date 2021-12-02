# Medusa

## Documentation

* [http://foofus.net/goons/jmk/medusa/medusa.html](http://foofus.net/goons/jmk/medusa/medusa.html)

## Common Options

* \-h : target host
* \-m : URI
* \-u : user
* \-P \<filename> : passwords list file
* \-M \<method> : authentication scheme

## Examples

### Show Modules

```
medusa -d
```

### Htaccess Attack

```
medusa -h 10.0.0.1 -u admin -P /usr/share/wordlists/rockyou.txt -M http -m DIR:/admin
```

