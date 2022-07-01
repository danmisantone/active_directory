# Steps taken to join XYZ domain

1. Clone Base Win 11 VM into `WS01`.
    - Suspend Base Machine and copy its contents into a new folder.
    - Use "Open a Virtual Machine" Option within VMWare Workstation 16 Player.
    - Use the `.vmx` within copied folder to launch new VM.

2. Connect `WS01` to DNS.
    - Find out what DNS Server `WS01` is connected to.
    ```
    Get-DNSClientServerAddress
    ```
    - Using the Interface Index found in the previous step, connect to the DNS address of the server.
    ```
    Set-DNSClientServerAddress -InterfaceIndex 7 -ServerAddress 192.168.138.130
    ```

3. Connect `WS01` to Domain
    - Connect to the Domain.
    ```
    Add-Computer -DomainName xyz.com -Credential xyz\Administrator -Force -Restart
    ```
