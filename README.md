
# Guide for store passwords with KeePass
This is guide and testground for storing passwords with KeePass password manager.

  https://keepass.info/

  https://keepass.info/download.html


## Installing in Windows

Quick version:
Download 'KeePass-X.XX-Setup.exe' and install it.

  https://keepass.info/download.html

  https://sourceforge.net/projects/keepass/files/latest/download


Here is batch script for downloading and installing Resilio Sync.

```bat
C:

cd "%HOMEDRIVE%%HOMEPATH%\Downloads"

PowerShell -Command "& {$client = new-object System.Net.WebClient; $client.DownloadFile('https://downloads.sourceforge.net/project/keepass/KeePass%202.x/2.50/KeePass-2.50-Setup.exe','.\KeePass-2.50-Setup.exe')}"

::KeePass-2.50-Setup.exe /SAVEINF=todo.inf
::KeePass-2.50-Setup.exe /SILENT /LOG=KeePass_install.log /LOADINF=todo.inf
```

