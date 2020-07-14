[title]: # (1.0.0 Initial Release)
[tags]: # (read me)
[priority]: # (31000)
# 1.0.0 Initial Release

_August 12th, 2020_:

With this release, Thycotic is rolling out the __Identity Bride__ (Id Bridge) for full Unix/Linux Active Directory integration support.

## Initial Feature Set

* Joins a non-windows host (Unix/Linux) to Active Directory, creating a computer object in Active Directory and a Kerberos trust between the Unix/Linux and Active Directory.
* Allows User and Group POSIX data (UID/GID/Home Dir/Shell/GECOS) to be set directly in Active Directory without the need for any schema extension.
* Allows User and Group POSIX data (UID/GID/Home Dir/Shell/GECOS) to generated on the fly when a user logs on.
* Stores all agent data centrally without the need for an external database or schema extension.
* Honors password and account policies when authenticating from non-windows systems (Unix/Linux).
* Allows for users to be locked and/or de-provisioned in the central directory and take immediate effecting on all Unix/Linux endpoints.
* Allows for a user to authenticate using their Active Directory username and password on Unix & Linux systems that have been joined to Active Directory.
* Allows for a user to authenticate using their Active Directory username and password on Unix & Linux systems that have been joined to Active Directory even when disconnected from Active Directory, so long as they have authenticated within in the last 30 days.
* Allows Access Control Lists (ACLs) (users and hosts) to be defined using native Active Directory groups.  Provide selective access to target hosts based on group membership.