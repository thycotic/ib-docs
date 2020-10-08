[title]: # (1.0.1 Release)
[tags]: # (read me)
[priority]: # (30999)
# 1.0.1 Release Notes

_October 8th, 2020_:

## Bug Fixes

* Improvements to the pmagent functionality in the event the Hosts UUID changes.
* The Agent Kerberos Ticket renewal in the event Active Directory Domain controller is unavailable at point of renewal. If the Agent is unable to contact the DC it moves to an unjoined status. With this fix it moves to a connecting status and continues to reattempt a renewal.
* Improvement to agent cache purging for users. Group cache will remain when associated with multiple users.
* Agent number reported on join is incorrect. *nix agent versions now display as short version number in ADUC, e.g. Thycotic Identity Bridge (1.0.1).
* Error resolved when loading Server Manager | Tools | Active Directory Administrative Center with Identity Bridge installed on Server.
* When creating an Active Directory user's home directory on the *nix agent, it will pull the files and folders from the `/etc/skel` directory or the skeleton directory defined under `/etc/default/useradd`.
* Authenticating AD users shouldn't pass through `/etc/login.defs`. These should be AD defined.
* Show success message following a license import instead of reporting an error.
* Improved license import functionality. Errors will be better captured.
* Improved feedback to user when running an invalid custom json script for `syscfg` command.
* AD User login appears to be defaulting as Failover login.
* *nix Agents are now able to join Active Directory Domains when BASE enabled within the hosts /etc/openldap/ldap.conf file
