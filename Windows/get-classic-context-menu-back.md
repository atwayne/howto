## Description
Get the classic context menu back in Windows 11

## Steps

1. Import the following registry key
```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32]
@=""
```
Or add it via command
```
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
```
2. Restart Windows Explorer

## Tags
- windows 11
- context menu
