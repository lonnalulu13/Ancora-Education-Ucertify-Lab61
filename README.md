# Ancora-Education-Ucertify-Lab61
# Managing Log Files


## Objective of the Lab
In this lab, you will learn to manage log files. File used: Log files Log files are files that contain messages about the system, including the kernel, services, and applications running on it. 
## Instructions
### STEP 1 
From the desktop, open the Terminal window. 
### STEP 2 
Execute the following command to open the /etc/rsyslog.conf file:
```bash
nano /etc/rsyslog.conf
```
### STEP 3 
Edit the file /etc/rsyslog.conf by adding the following entries, press CTRL+X, then press y, and then Enter to save the changes:
```bash
cron.=debug         /var/log/cron.debug
```
```bash
local3.*             root
```
### STEP 4
 Execute the following command to restart rsyslog:
```bash
systemctl restart rsyslog
```
### STEP 5
Execute the following commands to test the changes to the rsyslog.conf file: 
### Caution
* The second command should produce a message to the root terminal window.
```bash
logger -p cron.debug "test"
```
```bash
logger -p local3.warn "test"
```
### STEP 6
Execute the following command to view the contents of /var/log/cron.debug and verify that the logger entry was made and press CTRL+X, press y, and then press Enter to exit:
```bash
nano /var/log/cron.debug
```
## Disclaimer

This repository is for **educational and personal learning purposes only**.  

The original lab content belongs to **uCertify / Ancora Education** and remains their copyrighted material.  
This repository is not affiliated with, endorsed by, or sponsored by uCertify or Ancora Education.  

No copyright infringement is intended.  
Use of any tools or techniques mentioned here should only be performed in authorized, legal environments.
