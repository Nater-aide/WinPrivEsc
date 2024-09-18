#  Initial Enumeration
https://github.com/TCM-Course-Resources/Windows-Privilege-Escalation-Resources

## System Enumeration
First get a shell from Meterpreter
- ```systeminfo``` -- this will give system information
- ```systeminfo | findstr /B /C: 'OS Name" /C: "OS Version" /C:"System Type"``` -- quick way to grab info
- ```wmic qfe``` -- windows management instrumentation. QFE- quick fix engineering.
- ```wmic qfe get Caption,Description,HotFixID,InstalledOn``` -- cleaner look
- ```wmic logicaldisk``` -- lists out drivers
- ```wmic logicaldisk get caption,description,providername``` -- cleaner look

## User Enumeration
- ```whoami```
- ```whoami /priv``` -- privileges for user
- ```whoami /groups``` -- what groups were involved in
- ```net user``` -- shows us user on the machine
- ```net user (username)``` -- gives information about user
- ```net localgroup``` -- this will tell you who is in different groups

## Network Enumeration
- ```ipconfig```
- ```ipconfig /all```
- ```arp -a``` -- bigger in lab environment compare to CTFs
- ```netstat -ano``` - shows what we are communicating with

## Password hunting
- ```findstr /si password *.txt``` -- find string in a directory
- ```findstr /si password *.txt *.ini *.config``` -- hunt multiple file types

## AC Enumeration
- ```sc query windefend``` -- info about windows defender
- ```sc queryex type= service``` tells us all of the services running on the machine
- ```netsh advfirewall fireall dump```
- ```netsh firewall show state``` -- state of firewall
- ```netshe firewall show configuration``` -- look for ports or things open
