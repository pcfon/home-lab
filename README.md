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

1. Install bind packages on system and service 
```
[root@bastion ~]# yum install bind bind-utils -y
[root@bastion ~]# systemctl start named
[root@bastion ~]# systemctl enable named

```

