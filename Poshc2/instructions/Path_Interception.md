# [Path Interception](https://attack.mitre.org/techniques/T1574/007/)

## Exploit syntax:
```sh 
sharpps cmd.exe /c 'set PATH="%PATH%;C:\tmp"' 
#current path for that command line

#can use setx to change the system eniviroment but command is funky 
```
## Detection Technique:
* Investigate all instances of any process attempting to manipulate the ‘PATH’ variable inside a windows environment.
* Check the Value of the Path Variable for both User and system level
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Environment
HKEY_CURRENT_USER\Environment.
* Kibana:
    * process.name: cmd.exe
    * process.command_line: \*PATH\*
