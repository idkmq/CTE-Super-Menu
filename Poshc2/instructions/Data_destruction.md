# [Data Destruction]()

## Exploit Description: 
Delete files on victims machine

## Exploit syntax:
```powershell
posh-delete <path>
```

## Detection Technique:
* Use windows event codes that have to do with file manipulation/deletion
	* 4660 and 4663