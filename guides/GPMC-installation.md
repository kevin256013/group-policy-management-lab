# Installing GPMC (Group Policy Management) on Windows Server VM

1. Click on Manage(Top Right) and Select Add Roles and Features
2. In Server Roles, select AD Domain Services, Remote Access, and DNS
3. In Features, select Group Policy Management
4. Proceed with default setup and click install

![GPMC Install](../../ad-windows-server-lab/docs/screenshots/active-directory-install-1.png)
![GPMC Install](../../ad-windows-server-lab/docs/screenshots/active-directory-install-2.png)

# Configure Windows Server 

## Configure server with static IP address on Windows Server VM

1. In Search tool, open Command Line Prompt (CMD)
![Windows Configuration](../docs/screenshots/windows-config-2.png)

2. Type "ipconfig" and copy IP Address credentials
![Windows Configuration](../docs/screenshots/windows-config-3.png)

3. Navigate to Network & Internet Settings -> Advanced Network Settings
![Windows Configuration](../docs/screenshots/windows-config.png)

3. Select the "Change Adapter Option" and click on "Ethernet0"
![Windows Configuration](../docs/screenshots/windows-config-4.png)

4. Select Properties -> Internet Version Protocol 4 (TCP/IPV4), select "Use The Following IP Address", fill in IP address credentials and Alternative DNS Server (Ex: Google Server -> 8.8.8.8), click "OK"
![Windows Configuration](../docs/screenshots/windows-config-5.png)

5. To confirm configuration, type "ipconfig /all" in CMD, results should be similar to the example
![Windows Configuration](../docs/screenshots/windows-config-6.png)

# Configure Client Server 

## Configure Client Server on Windows Enterprise VM

1. Static IP Address not neccessary for Client servers
2. Navigate to Network & Internet Settings -> Advanced Network Settings -> "Change Adapter Option" -> "Ethernet0" -> Select Properties -> Internet Version Protocol 4 (TCP/IPV4)
![Client Configuration](../docs/screenshots/client-config.png)

3. In TCP/IPv4 Properties, select "Use the following DNS server addresses" and fill in IPv4 address from Windows Server as "Preferred DNS server" and Google Server(8.8.8.8) as "Alternative DNS Server", click OK
![Client Configuration](../docs/screenshots/client-config-2.png)

4. To Test Domain Controller Connection, proceed to type in CMD "nslookup Domain Name", which should have an IP Address assigned to the Domain like the Example below.
![Client Configuration](../docs/screenshots/client-config-3.png)

## Add Computer to the Domain

1. Navigate to File Explorer -> Right-click on "This PC" -> Properties -> "Rename this PC (advanced)" 
![Add Computer To Domain](../docs/screenshots/add-comp-to-domain.png)

2. In System Properties, type your Domain name and click OK
![Add Computer To Domain](../docs/screenshots/add-comp-to-domain-2.png)

3. Confirm Domain changes by filling credentials
![Add Computer To Domain](../docs/screenshots/add-comp-to-domain-3.png)

4. Succefully Added Computer to the Domain! and sysem will restart
![Add Computer To Domain](../docs/screenshots/add-comp-to-domain-4.png)

5. Once System is restarted, in "Other User", login with one of the user credential created in Windows Server VM.
![Add Computer To Domain](../docs/screenshots/add-comp-to-domain-5.png)
![Add Computer To Domain](../docs/screenshots/add-comp-to-domain-6.png)