# [Credential Dumping]()

## Exploit Description: 
Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password, from the operating system and software. Credentials can then be used to perform Lateral Movement and access restricted information

## Exploit syntax:
* with a system level callback use “Invoke-mimikatz’

## Detection Technique:
* Look for any reference to mimikatz
* Look for sysmon event code 10 that is interacting with lsass.exe
* Look for sysmon event code 8 that is interacting with lsass.exe