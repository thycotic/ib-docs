[title]: # (Agent Install)
[tags]: # (setup)
[priority]: # (4)
# Installing Thycotic Agent

The following information will guide you through the process on how to install your Identity Bridge agent on CentOS.

Once you have downloaded the latest version of Thycotic's __pmagent__ installer you will need to securely copy it onto you host. You will need to perform the installation as root or a user with root sudo permissions.

## Thycotic File Locations

Core installation location: `/opt/thycotic`

Other Thycotic file locations: `/lib64 /usr/lib64/security /var/log /etc`

Other locations Thycotic agent will modify system files: `/etc`, `/etc/pam.d`, `/etc/ssh`

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
