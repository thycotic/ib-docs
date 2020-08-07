[title]: # (Installation/Upgrades)
[tags]: # (setup)
[priority]: # (1)
# Installation and Upgrades

## Prerequisites

The agent should have a resolvable hostname set before installing the Thycotic Identity Bridge. If the agent has a default hostname of `localhost.localdomain`, the pmagent service will not function as expected.

**Note**: Updating the agent hostname post installation will require a reinitialization of the agent configuration.

## System Requirements

| **Operating System** | **Disk Space Requirements**  | **Minimum Memory** | **Other** |
| ----- | ----- | ----- | ----- |
| CentOS 7 | 100Mb 2mb in each of /lib64 /etc/pam.d /usr/lib64/security and /etc | 2Gb | For the Identity Bridge component to function correctly **SELinux** currently needs to be disabled on the host. |

## Installing Thycotic Agent on CentOS Hosts

The following information will guide you through the process on how to install your Identity Bridge agent on CentOS.

Once you have downloaded the latest version of Thycotic's __pmagent__ installer you will need to securely copy it onto you CentOS host. You will need to perform the installation as root or a user with root sudo permissions.

With CentOS there are 2 methods for installing packages, rpm and yum, both methods are outlined below.

### Thycotic File Locations

Core installation location: `/opt/thycotic`

Other Thycotic file locations: `/lib64 /usr/lib64/security /var/log /etc`

Other locations Thycotic agent will modify system files: /etc, /etc/pam.d, /etc/ssh

### Security-Enhanced Linux (SELinux)

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

### RPM

Performed as non root user with sudo permissions:

`>> sudo rpm -i /root/Thycotic/pmagent-1.0.0.x86_64.rpm`

Below is the expected output of a successful installation

```bash
Created symlink from /etc/systemd/system/multi-user.target.wants/pmagent.service to /etc/systemd/system/pmagent.service.

Please start the pmagent service by running:

/bin/systemctl start pmagent.service

You need to join an Active Directory domain to start authenticating users using the command:

/opt/thycotic/sbin/pmagent --join

Please disable SELinux to allow the Identity Bridge to function properly
```

### YUM

Performed as non root user with sudo permissions:

`>> sudo yum install /root/Thycotic/pmagent-1.0.0.x86_64.rpm`

```bash
Below is the expected output of a successful installation
Loaded plugins: fastestmirror, langpacks
Examining pmagent-1.0.0.x86_64.rpm: pmagent-1.0.0-1.x86_64
Marking pmagent-1.0.0.x86_64.rpm to be installed
Resolving Dependencies
--> Running transaction check
---> Package pmagent.x86_64 0:1.0.0-1 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

==============================================================================

Package         Arch         Version         Repository                  Size

==============================================================================
Installing:

pmagent         x86_64        1.0.0-1        /pmagent-1.0.0.x86_64       50 M

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
  Installing : pmagent-1.0.0-1.x86_64 1/1
Created symlink from /etc/systemd/system/multi-user.target.wants/pmagent.service to /etc/systemd/system/pmagent.service.

Please start the pmagent service by running:
  /bin/systemctl start pmagent.service

You need to join an Active Directory domain to start authenticating users using the command:
  /opt/thycotic/sbin/pmagent --join

Verifying : pmagent-1.0.0-1.x86_64 1/1

Installed:
pmagent.x86_64 0:1.0.0-1
Complete!
```

## Post installation

By default CentOS does not start a newly installed package, therefore you will need to manually start the Thycotic Agent.

Performed as non root user with sudo permissions:

`>> sudo systemctl start pmagent.service`

The pmagent service will be started automatically following a reboot of the host system.
