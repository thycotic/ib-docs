[title]: # (CentOS/RedHat/Oracle)
[tags]: # (setup)
[priority]: # (5)
# Installing on CentOS/RedHat/Oracle Linux

## Thycotic File Locations

Core installation location: `/opt/thycotic`

Other Thycotic file locations: `/lib64`, `/usr/lib64/security`, `/var/log`, `/etc`

Other locations Thycotic agent will modify system files: `/etc`, `/etc/pam.d`, `/etc/ssh`, `/etc/authselect/`

## Disable Security-Enhanced Linux (SELinux)

Currently for the Thycotic Identity Bridge agent to correctly authenticate against Active Directory Thycotic requires that the SELinux functionality of the host machine is disabled.

The agent installer will detect if SELinux is set to Enforcing or Permissive and provide the following message at the end of the installation.

```
========================================================================
Please disable SELinux to allow the Identity Bridge to function properly
========================================================================
```

To disable the SELinux functionality you will need to perform the following:

1. Edit the /etc/selinux/config file
1. Set the SELINUX line to: disabled
   * Example: SELINUX=disabled
1. Reboot your host

If SElinux is disabled the message will not be displayed.

For CentOS, RedHat, and Oracle there are 2 methods for installing packages, rpm and yum, both methods are outlined below.

## RPM

Performed as non root user with sudo permissions:

`>> sudo rpm -i /root/Thycotic/pmagent_x86_64_vn.n.n.rpm`

Where, pmagent_x86_64_vn.n.n.rpm is replaced with the actual software package and version that is being installed.

Below is the expected output of a successful installation

```
Created symlink from /etc/systemd/system/multi-user.target.wants/pmagent.service to /etc/systemd/system/pmagent.service.

Please start the pmagent service by running:

/bin/systemctl start pmagent.service

You need to join an Active Directory domain to start authenticating users using the command:

/opt/thycotic/sbin/pmagent --join

Please disable SELinux to allow the Identity Bridge to function properly
```

## YUM

Performed as non root user with sudo permissions:

`>> sudo yum install /root/Thycotic/pmagent_x86_64_vn.n.n.rpm`

Where, pmagent_x86_64_vn.n.n.rpm is replaced with the actual software package and version that is being installed.

```
Below is the expected output of a successful installation
Loaded plugins: fastestmirror, langpacks
Examining pmagent_x86_64_v1.1.2.rpm:  pmagent_x86_64_1.1.26
Marking pmagent_x86_64_v1.1.2.rpm to be installed
Resolving Dependencies
--> Running transaction check
---> Package pmagent.x86_64 0:1.1.26 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

==============================================================================

Package         Arch         Version         Repository                  Size

==============================================================================
Installing:

pmagent         x86_64        1.1.26        /pmagent_x86_64_v1.1.2       50 M

Transaction Summary
==============================================================================
Install 1 Package
Total size: 50 M
Installed size: 50 M
Is this ok [y/d/N]: y
Downloading packages:
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Installing : pmagent_x86_64_1.1.26 1/1
Created symlink from /etc/systemd/system/multi-user.target.wants/pmagent.service to /etc/systemd/system/pmagent.service.

Please start the pmagent service by running:
  /bin/systemctl start pmagent.service

You need to join an Active Directory domain to start authenticating users using the command:
  /opt/thycotic/sbin/pmagent --join

Verifying : pmagent_x86_64_1.1.26 1/1

Installed:
pmagent_x86_64_1.1.26
Complete!
```

## Post Installation

By default CentOS, RedHat, and Oracle do not start a newly installed package, therefore you will need to manually start the Thycotic Agent.

Performed as non root user with sudo permissions:

`>> sudo systemctl start pmagent.service`

The pmagent service will be started automatically following a reboot of the host system.
