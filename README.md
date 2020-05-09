# KEST3LN05EU Lokaverkefni

Búið:
- 2
- 3
- 5


Reminder for myself:  
- laga centos
- add sentos client dhcp status
- búa til tables og setja í þau
- laga backup file-inn og láta hann keyra kl 00:00 á föstudegi
- fixa domain/host names
- default gateway
- Skoða DNS betur
- og gera allt frá 8-13


***

### 1 - Install and configure server and clients
**Host/domain name configuration**
> $ sudo nano /etc/hosts

![host/domainname](/Screenshots/host_domain_name.PNG)

***
### 2 - Static IP address
> $ sudo nano /etc/netplan/01-network-manager-all.yaml

![staticip](/Screenshots/staticip.PNG)

***
### 3 - DHCP
**DHCP Configuration**
> $ sudo nano /etc/dhcp/dhcpd.conf

![dhcpconfiguration](/Screenshots/DHCP_configuration.PNG)

**DHCP Status**
> $ sudo systemctl status isc-dhcp-server.service

![dhcpstatus](/Screenshots/DHCP_status.PNG)

**DHCP Server**
> $ ip add sh

![dhcpserver](/Screenshots/DHCP_server.PNG)

**DHCP Clients**

![dhcpclient1](/Screenshots/DHCP_client.PNG)

***
### 4 - DNS
**DNS Configuration**
> $ sudo nano /etc/netplan/01-network-manager-all.yaml

![dns](/Screenshots/DNS.png)

***
### 5 - Create users
> sudo adduser [username]

**Proof of users**
> ls /home/

![allusers](/Screenshots/users.PNG)

***
### 6 - MySQL
> $ sudo mysql -u root

***
### 7 - Scheduled backups
> $ crontab -e  
> 0 0 * * 5 (00:00 á föstudegi)

***
### 8 - NTP

***
### 9 - Syslog

***
### 10 - Postfix

***
### 11 - Shared printers

***
### 12 - SSH

***
### 13 - NMAP
