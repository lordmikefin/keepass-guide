
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

:: Create install configuration file
::KeePass-2.50-Setup.exe /SAVEINF=KeePass-install.inf
(
echo [Setup]
echo Lang=en
echo Dir=C:\Program Files\KeePass Password Safe 2
echo Group=KeePass Password Safe 2
echo NoIcons=0
echo SetupType=full
echo Components=core,userdoc,keepasslibc,xsl,ngen,preload
echo Tasks=fileassoc,desktopicon
) > KeePass-install.inf

KeePass-2.50-Setup.exe /SILENT /LOG=KeePass_install.log /LOADINF=KeePass-install.inf
```

## Password storage/database

File 'keepass-pass-store.kdbx' in my Resilio Sync share is for testing purposes.
Install Resilio Sync by using my [guide](https://github.com/lordmikefin/resilio-sync-guide).
And sync 'c:\resilio-sync-test' directory by using my [read only key](https://github.com/lordmikefin/resilio-sync-guide/blob/main/sync/with-key.md).


## Open storage/database

TODO: key file

### Master password
```
DO_NOT_SHARE_MASTER_KEY_PUBLICLY
```


