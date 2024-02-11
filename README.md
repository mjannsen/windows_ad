# windows_ad
Training for Windows AD on Premise.

## Installing the Domain Controller

1. Use `sconfig` to:
    - Change the hostname
    - Change the IP address to a static
    - Change the DNS server

2. Install the Active Directory Windows Feature

```powershell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```
```powershell
import-Module ADDSDeployment
Install-ADDSForest
```

## Joining the Workstation to the domain

```powershell
Add-Computer -Domainname somethingsomething.de -Credential somethingsomething\Administrator -Force -Restart
```

## Disclaimer

The Repo is primarily designed for personal use, so it is subject to frequent modifications and glitches. Use it at your own risk and do not anticipate guidance for its installation on your device.
