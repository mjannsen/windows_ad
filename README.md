# windows_ad
Training for Windows AD.

## Installing the Domain Controller

1. Use `sconfig` to:
    - Change the hostname
    - Change the IP address to a static
    - Change the DNS server

2. Install the Active Directory Windows Feature

```shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```

```
Get-NetIPAddress
```

## Joining the Workstation to the domain

```
Add-Computer -Domainname somethingsomething.de -Credential somethingsomething\Administrator -Force -Restart
```
