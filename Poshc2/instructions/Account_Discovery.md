# [Account Discovery](https://attack.mitre.org/techniques/T1087/)

## Exploit Syntax

> **NOTE:** YOU CANNOT DETECT THESE! For a detectable version, skip to step 4

1. Instructions for local users (for domain users skip to step 3)

2. With local or domain beacon in posh instance, run:
    ```powershell
    get-userinfo
    ```
    > If you have domain admin creds when running this command you should get domain user info along with local users
3. To get domain user info, with a domain admin beacon, run these commands in posh: 


### - `Sharpview`

```powershell
sharpview Get-NetUser
```


> For more help or other commands, use this help command or this [sharpview link](https://github.com/tevora-threat/SharpView)

```powershell
searchhelp sharpview 
```
4. For local user enumeration, execute the following:
```
sharpps net user
```
5. For domain user enumeration, execute the following:
```
sharpps net user /domain
```
---

## Detection Methods

### Get-userinfo Detections 
*  Monitor `net.exe` and `net1.exe` processes

---

## Resrouces
https://github.com/tevora-threat/SharpView