[title]: # (1.0.0 Initial Release)
[tags]: # (read me)
[priority]: # (31000)
# 1.0.0 Initial Release

_August 12th, 2020_:

With this release, Thycotic is rolling out the __Identity Bridge__ (ID Bridge) for CentOS 7 Active Directory integration support.

Thycotic Identity Bridge provides centralized authentication and authorization for Unix and Linux systems. This enables organizations to validate that someone is who they say they are, so they can be granted access to the resources they need to perform their job. This software utilizes the organization’s existing directory service (e.g. Active Directory) to achieve consistency in identities across the enterprise regardless of platform and operating system. The ID Bridge simplifies access as users have one username and one password to remember. It also streamlines identity management as administrators have a single place to manage users, groups, and the systems they have access to.

## Initial Feature Set

* Joins a non-windows host (CentOS 7) to Active Directory, creating a computer object in Active Directory and a Kerberos trust between the CentOS 7 and Active Directory.
* Allows User and Group POSIX data (UID/GID/Home Dir/Shell/GECOS) to be set directly in Active Directory without the need for any schema extension.
* Provides Kerberos Authentication against Active Directory.
* Allows User and Group POSIX data (UID/GID/Home Dir/Shell/GECOS) to be generated on the fly when a user logs on.
* Stores all agent data centrally without the need for an external database or schema extension.
* Honors password and account policies when authenticating from non-windows systems (CentOS 7).
* Allows for users to be locked and/or de-provisioned in the central directory and take immediate effect on all CentOS 7 endpoints.
* Allows for a user to authenticate using their Active Directory username and password on Unix & Linux systems that have been joined to Active Directory.
* Allows for a user to authenticate using their Active Directory username and password on Unix & Linux systems that have been joined to Active Directory even when disconnected from Active Directory, so long as they have authenticated within the last 30 days.
* Allows Access Control Lists (ACLs) (users and hosts) to be defined using native Active Directory groups. Provide selective access to target hosts based on group membership.
* Automatic Time Sync with Active Director.
* Identity Bridge Configuration Tool for Centralized Configuration Management.
* \*Nix Command Line Tools:
  * Domain Join/Leave
  * System Configure/Unconfigure
  * ACL Reporting
  * User Testing
  * Cache Management
  * Agent Stats

## Limitations

* If you are running the Thycotic Identity Bridge Configuration Utility on a Domain Controller, while being logged in as an account that is not the primary administrator for the Domain Controller, you will have to perform one of the following actions so that the Thycotic Identity Bridge Configuration Utility has the appropriate permissions to write configuration settings to Active Directory:

  1. Use a specific user when attempting to connect to Active Directory in the Thycotic Identity Bridge Configuration Utility.
  1. Log into the Domain Controller with the primary administrator account.
  1. Run the Thycotic Identity Bridge Configuration Utility as Administrator.
  1. Grant the user you are attempting to connect with explicit read/write permissions to the Configuration Partition of your domain.

  This is due to a security feature implemented by Windows on Domain Controllers to enhance security."
* Root will always have SU access to user accounts.
* Standard ftp (vsftp) doesn’t display the Windows Messages.
* Root will not have permission to change Active Directory users passwords via the `passwd` command.
* When AD Accounts disabled, telnet and su display an additional message stating “User account has expired”. Unfortunately Thycotic is unable to control these additional messages.
* If a an Active Directory Username or Alias matches a Local Agent Username, the login will be blocked, with the exception of of root SU.
* If an Active Directory users UID Number matches a Local Agents users UID, the Active Directory user will be blocked. The Local Agents user will be granted access.
* If the agent has a default hostname of `localhost.localdomain`, the pmagent service will not function as expected and will return an error. Updating the agent hostname post installation will require a re-initialization of the agent configuration using the `pmagent --init` command.
* VNC and Remote Desktop will not be supported authentication methods for version 1 of Thycotic Identity Bridge. We recommend that these methods are disabled.

## Known Issues

* A reboot will be required after the Agent joining the Domain to allow AD users to login via Gnome desktop.
* Logging into an Agent with cached credentials can only accept the case of the username as defined in Active Directory.
* SSH logins drop-back to a local login attempt following 3 failed Active Directory attempts.
* Chsh command is not currently supported for Active Directory users, if you are required to change the shell for an Active Directory user, please use the Thycotic User Data panel in ADUC.
