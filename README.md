# Virtual-Machine-Manager-Web-App
**THIS SHOULD NOT BE EXPOSED TO THE WEB, ONLY USE AS INTERNAL SERVICE**

Aims to imitate Virtual Machine Manager as a webapp using flask

![Pic](Progress.png?raw=true "Demo")

## Inital Setup

Guacamole Install (Optional)
```
...
```
NOVNC Install (Optional)
```
sudo snap install novnc
```

## Setup (if this is not running on the same server as vms)

Setup ssh keys
https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/virtualization_deployment_and_administration_guide/sect-remote_management_of_guests-remote_management_with_ssh

Setting up vms to work with vnc...

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
ssh_host = 192.168.1.1                          # SSH HOST for libvirt, vnc, and spice
ssh_port = 22                                   # SSH PORT for libvirt, vnc, and spice
ssh_usr = xxxx                                  # SSH USER
```
## Usage

Run
```
./main.py
```
Go to site http://0.0.0.0:5000/

## Thanks

Thanks to all those who made this possible with simple to use python packages.  If I missed any license or credits, please let me know and I'll add them here.

https://github.com/novnc/noVNC

https://github.com/muicss/mui
