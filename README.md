# HOME-LAB WORKING PROGRESS
This project will ultiately be broken down into multiple projects 

# HOME-LAB

This document are procedures steps in setting up multiple components in my home lab.
For my home lab I choose to use a INTEL NUC10i7FNK for the purposes of energy efficient. 
Thought I would have it for a while so used it as big investmenet to advance my career. 
You can find great cheap and older versions of the NUC with customization of memory and storage. 


# Virtualization

To have the ability install multiple VMS on my box I choose the route of installing VMWare on my NUC. 
At this point I downloaded VmWare Vsphere from the website and bought a unlimited code from ebay that allows me to have no restriction. 
For the NUC you will have to install VMware(Esxi) on a bootable usb and boot NUC off of your USB. 


# Setting Up AD Servers. 

Setting up AD I choose the route of using Microsoft Server 2016. I choose this becuase it will allow me to intergrate with a lot of different applications the right way. Instructions comming soon 

```
This is an example of using code block format 

```

# Setting Up DHCP Server w/ PXE BOOT

# Install DNS

export DNS_MASTER_IP=192.168.1.10    (Use your IP address that you are setting up DNS on)
export FWD_FILE_NAME=fwd.fon         (name of the file you, your choice) 
export REV_FILE_NAME=rev.fon         (name of the file you, your choice) 

REV_FILE_NAME

Some variables need to be set to make our day easier 
sed -i "s|--MANIFEST_URL--|${FWD_FILE_NAME}|g" named.conf
sed -i "s|--MANIFEST_URL--|${REV_FILE_NAME}|g" named.conf

Documentation at this location 
https://www.unixmen.com/setting-dns-server-centos-7/

1. Install bind packages on system and service 
```
[root@bastion ~]# yum install bind bind-utils -y
[root@bastion ~]# systemctl start named
[root@bastion ~]# systemctl enable named

2. Get these files and add to the project and use the sed command to simply some stuff
Need set variables, inport these files and replace . 
1. /etc/named.conf
2. /var/named/fwd.fon
3. /var/named/rev.fon
4. add fire
firewall-cmd --permanent --add-port=53/tcp
firewall-cmd --permanent --add-port=53/udp
firewall-cmd --reload
```






# Install PXE Boot Server 

```
yum install dhcp tftp tftp-server syslinux vsftpd xinetd -y

```




