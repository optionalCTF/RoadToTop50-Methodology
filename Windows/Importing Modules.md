## Importing PowerShell Modules
When importing modules to PowerShell you have to have them in one of the following directories
```
$Env:HomeDrive$Env:HOMEPATH\Documents\WindowsPowerShell\Modules" The default 

computer-level module path is: "$Env:windir\System32\WindowsPowerShell\v1.0\Modules"
```

If the `$env:HomeDrive;$Env:HOMEPATH\Documents\WindowsPowerShell\Modules` does not exist. You can easily create it and it *should* override the computer-level path.


Also screw powershell

