[title]: # (Ubuntu)
[tags]: # (setup)
[priority]: # (6)
# Installing on Ubuntu

## Thycotic File Locations

Core installation location: `/opt/thycotic`

Other Thycotic file locations: `/lib/x86_64-linux-gnu/security`, `/lib/x86_64-linux-gnu/`, `/var/log`, `/etc`

Other locations Thycotic agent will modify system files: `/etc`, `/etc/pam.d`, `/etc/ssh`

There are 2 methods for installing packages, DPKG and APT, both methods are outlined below.

## DPKG

Performed as non root user with sudo permissions

`>> sudo dpkg -i pmagent-1.0.1-Linux.deb`

Below is the expected output of a successful installation

```
Selecting previously unselected package pmagent.
(Reading database ... 184828 files and directories currently installed.)
Preparing to unpack pmagent-1.0.1-Linux.deb ...
Unpacking pmagent (1.0.1) ...
Setting up pmagent (1.0.1) ...
Created symlink /etc/systemd/system/multi-user.target.wants/pmagent.service → /etc/systemd/system/pmagent.service.

Please start the pmagent service by running:
    /bin/systemctl start pmagent.service

You need to join an Active Directory domain to start authenticating users
using the command:
    /opt/thycotic/sbin/pmagent --join
```

## APT

Performed as non root user with sudo permissions

`>> sudo apt install /root/Thycotic/pmagent-1.0.1-Linux.deb`

Below is the expected output of a successful installation

```
Reading package lists... Done
Building dependency tree
Reading state information... Done
Note, selecting 'pmagent' instead of '/home/installer/pmagent-1.0.1-Linux.deb'
The following packages were automatically installed and are no longer required:
  linux-hwe-5.4-headers-5.4.0-42 tcpd
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed
  pmagent
0 to upgrade, 1 to newly install, 0 to remove and 92 not to upgrade.
Need to get 0 B/8,669 kB of archives.
After this operation, 28.5 MB of additional disk space will be used.
Get:1 /home/installer/pmagent-1.0.1-Linux.deb pmagent amd64 1.0.1 [8,669 kB]
Selecting previously unselected package pmagent.
(Reading database ... 184828 files and directories currently installed.)
Preparing to unpack .../pmagent-1.0.1-Linux.deb ...
Unpacking pmagent (1.0.1) ...
Setting up pmagent (1.0.1) ...
Created symlink /etc/systemd/system/multi-user.target.wants/pmagent.service → /etc/systemd/system/pmagent.service.

Please start the pmagent service by running:
    /bin/systemctl start pmagent.service

You need to join an Active Directory domain to start authenticating users
using the command:
    /opt/thycotic/sbin/pmagent --join
```

## Post Installation

By default Ubuntu does not start a newly installed package, therefore you will need to manually start the Thycotic Agent

Performed as non root user with sudo permissions

`>> sudo systemctl start pmagent.service`

The pmagent service will be started automatically following a reboot of the host system.