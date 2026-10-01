# Windows-Privilege-Escalation

### Learn Windows Priv Esc
- Fuzzy Security Guide - https://www.fuzzysecurity.com/tutorials/16.html
- PayloadsAllTheThings Guide - https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Windows%20-%20Privilege%20Escalation.md
- Absolomb Windows Privilege Escalation Guide - https://www.absolomb.com/2018-01-26-Windows-Privilege-Escalation-Guide
- Sushant 747's Guide (Country dependant - may need VPN) - https://sushant747.gitbooks.io/total-oscp-guide/content/privilege_escalation_windows.html
- Windows PrivEsc Checklist - https://hacktricks.wiki/en/windows-hardening/checklist-windows-privilege-escalation.html
- Windows Privilege Escalation - https://hacktricks.wiki/en/windows-hardening/windows-local-privilege-escalation/index.html
-  InternalAllTheThings - https://swisskyrepo.github.io/InternalAllTheThings/redteam/escalation/windows-privilege-escalation
- Windows Kernel Exploits - https://github.com/SecWiki/windows-kernel-exploits


### Search for Exploits
- Google Search Operators
```
firefox --search "Microsoft Edge site:exploit-db.com"
```

- OffSec Exploit Database - https://www.exploit-db.com/

- Linux Local Search 
```
searchsploit samba 2.2.1a 
```

### Search for a Reverse Shell:
 - InternalAllTheThings - https://swisskyrepo.github.io/InternalAllTheThings/cheatsheets/shell-reverse-cheatsheet
- Kali Local Path - /usr/share/webshells/
- meterpreter payload cheat sheet - https://nitesculucian.github.io/2018/07/25/msfvenom-cheat-sheet/
- Basic PowerShell for Pentesters - https://hacktricks.wiki/en/windows-hardening/basic-powershell-for-pentesters/index.html#download--execute
- PHP Reverse Shell - https://github.com/pentestmonkey/php-reverse-shell/blob/master/php-reverse-shell.php
- Reverse Shell Cheat Sheet - https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet


### Customize a Reverse Shell
- https://www.revshells.com/


### Windows Automated Tools:
Executables:**
- WinPEAS.exe & LinPEAS.exe - https://github.com/peass-ng/PEASS-ng/tree/master/winPEAS          (Best)
- Seatbelt.exe - https://github.com/GhostPack/Seatbelt
- Watson.exe - https://github.com/rasta-mouse/Watson          (Deprecated)
- SharpUp.exe - https://github.com/GhostPack/SharpUp          (Not Updated)

**PowerShell:**
- Sherlock.ps1 - https://github.com/rasta-mouse/Sherlock          (Deprecated)
- PowerUp.ps1/Powersploit/privesc - https://github.com/PowerShellMafia/PowerSploit/tree/master/Privesc          (Deprecated)
- JAWS.ps1 - https://github.com/411Hall/JAWS          (Not Updated)
- https://github.com/samratashok/nishang

**Others:**
- Local Windows Exploit Suggester.py - https://github.com/AonCyberLabs/Windows-Exploit-Suggester          (Deprecated)
- Metasploit Local Exploit Suggester - https://www.rapid7.com/blog/post/2015/08/11/metasploit-local-exploit-suggester-do-less-get-more/
- Windows_privesc_check.py - https://github.com/pentestmonkey/windows-privesc-check
- Defeating Windows User Account Control - https://github.com/hfiref0x/UACME
