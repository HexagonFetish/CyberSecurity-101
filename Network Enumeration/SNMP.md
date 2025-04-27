## What is SNMP?

**SNMP** (**S**imple **N**etwork **M**anagement **P**rotocol) is a protocol used to remotely manage and monitor network devices (routers, switches, printers, servers, etc.).

## What is SNMP Enumeration?

is the **recon** stage where you try to extract information from target devices.

If SNMP is not configured properly, you can collect critical information such as the device's:

    Operating system information
    Installed services
    Open ports
    Network interface details
    User accounts
    Routing tables
    Hardware/software versions

without a password or with a very simple password (community string).

## What to Look for in SNMP Enumeration?
#### Device Information
- Router model, firmware version, etc.
#### Network Interfaces
- IP addresses, MAC addresses
#### User Accounts
- Administrator or user account information
#### Running Processes
- Running services and applications
#### Routing Tables
- Network map extraction
#### ARP Tables
- IP/MAC information of neighboring devices

## What Tools Do You Use?
- snmpwalk → The most basic SNMP information gathering tool
- snmp-check → Gets more detailed device and user information
- onesixtyone → Community string to bruteforce (for example, tries common strings like public, private)
- snmpenum → Collects user, network, service information

### snmpwalk usage:
```snmpwalk -v2c -c public <ipaddress>```
- -v2c: SNMP version 2c
- -c public: Community string (think of it like a password)
- ```<ipaddress>```: Target IP

## Most Classic SNMP Vulnerabilities
- Leaving default community strings like "public" or "private"
- Using SNMP v1 or v2c (they work without password/data encryption)
- SNMP service being open to the internet
- OIDs with management information being open to the outside