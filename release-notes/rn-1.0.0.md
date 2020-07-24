[title]: # (1.0.0 Initial Release)
[tags]: # (read me)
[priority]: # (31000)
# 1.0.0 Initial Release

_August 12th, 2020_:

With this release, Thycotic is rolling out the __Identity Bride__ (Id Bridge) for CentOS 7 Active Directory integration support.

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

## Known Issues

* A reboot will be required after the Agent joining the Domain to allow AD users to login via Gnome desktop.
* Logging into an Agent with cached credentials can only accept the case of the username as defined in Active Directory.
* SSH logins drop-back to a local login attempt following 3 failed Active Directory attempts.