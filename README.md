# KEST3LN05EU Lokaverkefni

Búið:
- 2
- 3
- 4
- 5
- 6
- 7
- 8
- 9


Reminder for myself:  
- laga centos og add sentos client dhcp status
- Skoða DNS betur
- og gera allt frá 10-13
- postfix og roundcube

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
> $ sudo adduser [username]

**Proof of users**
> ls /home/

![allusers](/Screenshots/users.PNG)

***
### 6 - MySQL
> $ sudo mysql -u root

**Employees**

![sqlemployees](/Screenshots/sql_employees.PNG)

**Departments**

![sqldepartments](/Screenshots/sql_departments.PNG)

**Locations**

![sqllocations](/Screenshots/sql_locations.PNG)

**Jobs**

![sqljobs](/Screenshots/sql_jobs.PNG)

***
### 7 - Scheduled backups
**Schedule configuration**
> $ crontab -e  

![crontabconfig](/Screenshots/backup_crontab.PNG)

**Backup script**

![backupscript](/Screenshots/backup_script.PNG)

**Backup test**

![backupproof](/Screenshots/backup_proof.PNG)

***
### 8 - NTP
**NTP Configuration**
> $ sudo nano /etc/ntp.conf

![ntpconfig](/Screenshots/ntp_conf.PNG)

**NTP Syncronization from client**
> $ ntpq -p

![ntpsync](/Screenshots/ntp_sync.PNG)

***
### 9 - Syslog
**Rsyslog server configuration**
> $ sudo nano /etc/rsyslog.conf

![syslogconf](/Screenshots/rsyslog_conf.PNG)

**Rsyslog client configuration**
> $ sudo nano /etc/rsyslog.conf

![syslogclientconf](/Screenshots/rsyslog_conf_client.PNG)

**Rsyslog status**
> $ netstat -4altunp | grep 514

![rsyslogstatus](/Screenshots/rsyslog_listening.PNG)

**Client logs**  
![clientproof](/Screenshots/rsyslog_proof.PNG)

***
### 10 - Postfix

***
### 11 - Shared printers

***
### 12 - SSH

***
### 13 - NMAP
