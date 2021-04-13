# Virtual-Machine-Manager-Web-App
Aims to imitate Virtual Machine Manager as a webapp
Outputs to novnc, or guacamole

## Setup

Guacamole Install (Optional)
```
...
```
NOVNC Install (Optional)
```
sudo snap install novnc
```
Setup ssh keys (if this is not running on the same server as vms)
https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/virtualization_deployment_and_administration_guide/sect-remote_management_of_guests-remote_management_with_ssh

## Config

settings.config
```
[Console]
vnc_type = novnc                               # novnc, guac

[Guac]
guac_url = http://192.168.1.2:8080/guacamole   # Guacamole URL for REST API
guac_usr = xxxx                                # Guacamole user with admin privileges 
guac_pwd = xxxx                                # Guacamole password for user

[Libvirt]
hostIp = 192.168.1.1                           # VM HOST IP (FOR VNC and SPICE)
host = username@192.168.1.1:22                 # SSH HOST
```
## Usage

Run
```
./main.py
```
## Thanks

Thanks to all those who made this possible with simple to use python packages.  If I missed any license or credits, please let me know and I'll add them here.

https://github.com/novnc/noVNC
https://github.com/muicss/mui
