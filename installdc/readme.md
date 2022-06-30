# Installing the Domain Controller


1. Use `sconfig` to:
    - Change the hostname
    - Change the IP addr to static
    - Change the DNS Server to our IP

2. Install the Active Directory Windows Feature

```
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```