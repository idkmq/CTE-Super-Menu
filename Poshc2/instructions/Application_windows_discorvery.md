# [Application Window Discovery]()

## Exploit Description: 
Obtain a listing of open application windows.

---
## Exploit syntax:

  
### List processes
```powershell
getprocesslist
```

```powershell 
ps 
```
### Get a process
```powershell 
getprocess <explore>
```

```powershell 
sharpps get-process 
```
---

## Detection Technique:
* Look for any process enumeration (ls / get-process

## Resources