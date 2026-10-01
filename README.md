# Windows Privilege Escalation

Practical resources, guides, checklists, exploit research, enumeration tools, and payload references for Windows local privilege escalation.

> Use these resources only on systems you own or are explicitly authorized to test.

This repository is intended to be a **practical reference**, not a theoretical Windows security textbook.

The main focus is:

* Enumeration
* Manual validation
* Exploit research
* Privilege-escalation techniques
* Practical tooling
* Shell/payload references
* Lab and authorized penetration-testing workflows

---

## 1. Learn Windows Privilege Escalation

### Comprehensive Guides

* **FuzzySecurity - Windows Privilege Escalation Guide**
  https://www.fuzzysecurity.com/tutorials/16.html

* **PayloadsAllTheThings - Windows Privilege Escalation**
  https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Windows%20-%20Privilege%20Escalation.md

* **Absolomb - Windows Privilege Escalation Guide**
  https://www.absolomb.com/2018-01-26-Windows-Privilege-Escalation-Guide

* **Sushant 747 - Total OSCP Guide: Windows Privilege Escalation**
  https://sushant747.gitbooks.io/total-oscp-guide/content/privilege_escalation_windows.html

### Checklists & Methodologies

* **HackTricks - Windows Privilege Escalation Checklist**
  https://hacktricks.wiki/en/windows-hardening/checklist-windows-privilege-escalation.html

* **HackTricks - Windows Local Privilege Escalation**
  https://hacktricks.wiki/en/windows-hardening/windows-local-privilege-escalation/index.html

* **InternalAllTheThings - Windows Privilege Escalation**
  https://swisskyrepo.github.io/InternalAllTheThings/redteam/escalation/windows-privilege-escalation

---

## 2. Exploit Research

### Exploit Databases & Search

* **Exploit-DB**
  https://www.exploit-db.com/

* **SearchSploit**

```bash
searchsploit <software> <version>
```

Example:

```bash
searchsploit samba 2.2.1a
```

### Search Operators

Example:

```bash
firefox --search "Microsoft Edge site:exploit-db.com"
```

Use version-specific searches to identify publicly documented vulnerabilities affecting the target software or Windows component.

### Windows Kernel Exploits

* **SecWiki - Windows Kernel Exploits**
  https://github.com/SecWiki/windows-kernel-exploits

---

## 3. Automated Windows Enumeration

### Executables

* **WinPEAS**
  https://github.com/peass-ng/PEASS-ng/tree/master/winPEAS

* **Seatbelt**
  https://github.com/GhostPack/Seatbelt

* **Watson** - Deprecated
  https://github.com/rasta-mouse/Watson

* **SharpUp**
  https://github.com/GhostPack/SharpUp

### PowerShell

* **PowerUp / PowerSploit - Privesc** - Legacy / Deprecated
  https://github.com/PowerShellMafia/PowerSploit/tree/master/Privesc

* **Sherlock** - Deprecated
  https://github.com/rasta-mouse/Sherlock

* **JAWS**
  https://github.com/411Hall/JAWS

* **Nishang**
  https://github.com/samratashok/nishang

### Other Enumeration & Exploit-Suggestion Tools

* **Windows Exploit Suggester** - Deprecated
  https://github.com/AonCyberLabs/Windows-Exploit-Suggester

* **Metasploit Local Exploit Suggester**
  https://www.rapid7.com/blog/post/2015/08/11/metasploit-local-exploit-suggester-do-less-get-more/

* **Windows Privilege Escalation Checker**
  https://github.com/pentestmonkey/windows-privesc-check

* **UACME - UAC Bypass Research / Testing**
  https://github.com/hfiref0x/UACME

> Automated tools provide enumeration leads. Validate interesting findings manually before considering them confirmed vulnerabilities.

---

## 4. Reverse Shells & Payloads

### Reverse Shell References

* **InternalAllTheThings - Reverse Shell Cheat Sheet**
  https://swisskyrepo.github.io/InternalAllTheThings/cheatsheets/shell-reverse-cheatsheet

* **PentestMonkey - Reverse Shell Cheat Sheet**
  https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet

* **Kali Linux - Web Shells**

```text
/usr/share/webshells/
```

* **PHP Reverse Shell - PentestMonkey**
  https://github.com/pentestmonkey/php-reverse-shell

### PowerShell

* **HackTricks - Basic PowerShell for Pentesters**
  https://hacktricks.wiki/en/windows-hardening/basic-powershell-for-pentesters/index.html

### Meterpreter / Msfvenom

* **Msfvenom / Meterpreter Cheat Sheet**
  https://nitesculucian.github.io/2018/07/25/msfvenom-cheat-sheet/

### Reverse Shell Customization

* **RevShells**
  https://www.revshells.com/

---

## 5. Quick Reference

### Main Workflow

```text
Initial Access
      ↓
System Enumeration
      ↓
User / Group Enumeration
      ↓
Privilege Enumeration
      ↓
Service Enumeration
      ↓
Scheduled Tasks
      ↓
Registry
      ↓
File / Directory Permissions
      ↓
Credentials / Configuration
      ↓
Installed Software
      ↓
Kernel / Patch Research
      ↓
Manual Validation
      ↓
Privilege Escalation
```

### Core Enumeration Commands

```cmd
whoami /all
systeminfo
hostname
ipconfig /all
net user
net localgroup administrators
whoami /priv
tasklist /v
sc query
schtasks /query /fo LIST /v
netstat -ano
reg query HKLM\Software
reg query HKCU\Software
icacls "C:\Path"
```

### PowerShell

```powershell
Get-ComputerInfo
Get-LocalUser
Get-LocalGroupMember Administrators
Get-CimInstance Win32_Service
Get-CimInstance Win32_Process
Get-ScheduledTask
Get-NetTCPConnection
Get-ChildItem Env:
Get-Acl "C:\Path"
```

---

## Resource Status

Some older tools in this list are retained because they remain useful for **historical research, methodology, or understanding older techniques**.

| Resource                  | Category         | Status           |
| ------------------------- | ---------------- | ---------------- |
| WinPEAS                   | Enumeration      | Active           |
| Seatbelt                  | Enumeration      | Active           |
| SharpUp                   | Enumeration      | Limited updates  |
| Watson                    | Exploit research | Deprecated       |
| Sherlock                  | Exploit research | Deprecated       |
| PowerUp                   | Enumeration      | Legacy           |
| JAWS                      | Enumeration      | Limited updates  |
| Windows Exploit Suggester | Exploit research | Deprecated       |
| Windows Kernel Exploits   | Exploit research | Reference        |
| UACME                     | UAC research     | Research/testing |
| HackTricks                | Methodology      | Reference        |
| PayloadsAllTheThings      | Methodology      | Reference        |
| InternalAllTheThings      | Methodology      | Reference        |

