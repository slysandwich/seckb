# Table of contents

* [Home](README.md)

## General

* [External References & Links](general/awesome-links.md)
* [Trainings](general/trainings/README.md)
  * [OSCP](general/trainings/oscp.md)
* [To Read](general/to-read/README.md)
  * [Reconnaissance](general/to-read/reconnaissance.md)
  * [Buffer Overflow](general/to-read/buffer-overflow.md)

## Toolbox

* [Network](toolbox/network/README.md)
  * [Snmp-check](toolbox/network/snmp-check.md)
  * [Snmpwalk](toolbox/network/snmpwalk.md)
  * [Onesixtyone](toolbox/network/onesixtyone.md)
  * [Enum4linux](toolbox/network/enum4linux.md)
  * [Nbtscan](toolbox/network/nbtscan.md)
  * [Nmap](toolbox/network/nmap.md)
  * [Masscan](toolbox/network/masscan.md)
  * [DNSenum](toolbox/network/dnsenum.md)
  * [DNSrecon](toolbox/network/dnsrecon.md)
  * [Netcat](toolbox/network/netcat.md)
  * [Socat](toolbox/network/socat.md)
  * [Tcpdump](toolbox/network/tcpdump.md)
* [Reconnaissance](toolbox/reconnaissance/README.md)
  * [Recon-ng](toolbox/reconnaissance/recon-ng.md)
  * [TheHarvester](toolbox/reconnaissance/theharvester.md)
* [Linux](toolbox/linux/README.md)
  * [Awk](toolbox/linux/awk.md)
  * [Cut](toolbox/linux/cut.md)
  * [Grep](toolbox/linux/grep.md)
  * [Sed](toolbox/linux/sed.md)
  * [Xxd](toolbox/linux/xxd.md)
* [Windows](toolbox/windows/README.md)
  * [Rpcclient](toolbox/windows/rpcclient.md)
  * [SNMP /Windows](toolbox/windows/snmp-windows.md)
  * [Powercat](toolbox/windows/powercat.md)
* [Web](toolbox/web/README.md)
  * [Gobuster](toolbox/web/gobuster.md)
  * [WPScan](toolbox/web/wpscan.md)
  * [SQLmap](toolbox/web/sqlmap.md)
* [Exploitation Frameworks](toolbox/exploitation-frameworks/README.md)
  * [Metasploit](toolbox/exploitation-frameworks/metasploit.md)
  * [Powershell Empire](toolbox/exploitation-frameworks/powershell-empire.md)
* [Password Attacks](toolbox/password-attacks/README.md)
  * [CredMaster](toolbox/password-attacks/credmaster.md)
  * [Go365](toolbox/password-attacks/go365.md)
  * [Hashcat](toolbox/password-attacks/hashcat.md)
  * [fgdump](toolbox/password-attacks/fgdump.md)
  * [pwdump](toolbox/password-attacks/pwdump.md)
  * [John The Ripper](toolbox/password-attacks/john-the-ripper.md)
  * [Medusa](toolbox/password-attacks/medusa.md)
  * [Crowbar](toolbox/password-attacks/crowbar.md)
  * [Hydra](toolbox/password-attacks/hydra.md)
  * [Mimikatz](toolbox/password-attacks/mimikatz.md)
  * [Pth-toolkit](toolbox/password-attacks/pth-toolkit.md)

## Reconnaissance

***

* [OSINT](passive.md)
* [Network Scanning](active.md)

## Exploitation <a href="#binary-exploitation" id="binary-exploitation"></a>

* [Services](binary-exploitation/services/README.md)
  * [21 - FTP](binary-exploitation/services/21-ftp.md)
  * [25 - SMTP](binary-exploitation/services/25-smtp.md)
  * [53 - DNS](binary-exploitation/services/53-dns.md)
  * [111 - NFS](binary-exploitation/services/111-nfs.md)
  * [139, 445 - SMB](binary-exploitation/services/139-445-smb.md)
  * [161 - SNMP](binary-exploitation/services/161-snmp.md)
  * [1433 - MSSQL](binary-exploitation/services/1433-mssql.md)
  * [3306 - MySQL / MariaDB](binary-exploitation/services/3306-mysql-mariadb.md)
  * [5800, 5900 - VNC](binary-exploitation/services/5800-5900-vnc.md)
* [Applications](binary-exploitation/applications/README.md)
  * [Exchange](binary-exploitation/applications/exchange.md)
* [Binary](binary-exploitation/services-1/README.md)
  * [Buffer Overflow](binary-exploitation/services-1/windows-buffer-overflow.md)
  * [Fuzzing](binary-exploitation/services-1/fuzzing.md)
* [Client-Side](binary-exploitation/client-side.md)
* [Public Exploits](binary-exploitation/public-exploits.md)
* [Reverse Shell](binary-exploitation/reverse-shell.md)
* [Web](binary-exploitation/web-1/README.md)
  * [Launching HTTP Server](binary-exploitation/web-1/launching-http-server.md)
  * [Techniques](binary-exploitation/web-1/techniques/README.md)
    * [Code Injection - Python](binary-exploitation/web-1/techniques/code-injection-python.md)
    * [Content-Security Bypass](binary-exploitation/web-1/techniques/content-security-bypass.md)
    * [File Inclusion](binary-exploitation/web-1/techniques/file-inclusion.md)
    * [PHP Wrappers](binary-exploitation/web-1/techniques/php-wrappers.md)
    * [SQL Injection](binary-exploitation/web-1/techniques/sql-injection.md)
    * [XSS - Cross-Site Scripting](binary-exploitation/web-1/techniques/xss-cross-site-scripting.md)
    * [XXE - XML External Entity Injection](binary-exploitation/web-1/techniques/xml-external-entity-xxe-injection.md)
  * [Webshell](binary-exploitation/web-1/webshell.md)
  * [Wordpress](binary-exploitation/web-1/wordpress.md)

## Post-Exploitation

* [Linux](post-exploitation/linux/README.md)
  * [Privilege Escalation](post-exploitation/linux/privilege-escalation.md)
  * [Port Forwarding & Tunneling](post-exploitation/linux/port-forwarding-and-tunneling.md)
* [Windows](post-exploitation/windows/README.md)
  * [Active Directory](post-exploitation/windows/active-directory.md)
  * [Privilege Escalation](post-exploitation/windows/privilege-escalation.md)
  * [Powershell](post-exploitation/windows/powershell.md)
  * [File Transfers](post-exploitation/windows/file-transfers.md)
  * [Antivirus Evasion](post-exploitation/windows/antivirus-evasion.md)
  * [UAC Bypass](post-exploitation/windows/uac-bypass.md)
  * [Lateral Movement](post-exploitation/windows/lateral-movement.md)
  * [Port Forwarding & Tunneling](post-exploitation/windows/port-forwarding-and-tunneling.md)
* [Pivoting](post-exploitation/pivoting.md)
* [Loot, Booty & Plunder](post-exploitation/loot-booty-and-plunder.md)

## Password Attacks

* [Default Credentials](password-attacks/default-credentials.md)
* [Wordlists](password-attacks/wordlists.md)
* [Pass-The-Hash](password-attacks/pass-the-hash.md)

## Crypto

* [External Links](crypto/external-links.md)

## Physical Pentest

* [TMP](physical-pentest/tmp.md)
* [Physical Pentest](physical-pentest/physical-pentest.md)

## Social-Engineering

* [TMP](social-engineering/tmp.md)

***

* [Kali Customisation](kali-customisation.md)
* [CTFs](ctfs.md)
* [Mobile Pentest](mobile-pentest.md)
