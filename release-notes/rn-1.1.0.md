[title]: # (1.1.0 Release)
[tags]: # (read me)
[priority]: # (30998)
# 1.1.0 Release Notes

_November 24th, 2020_:

## Enhancements

Enhancements available with the 1.1.0 release of Identity Bridge.

* The Message Tab in the Configuration Utility was split to provide friendly message setup.

## Bug Fixes

* Added libjansson for pmagent to fullfil prerequisite regarding Ubuntu 18.04 and 20.04 live server issue mentioned as a known issue [here](rn-1.0.1.md#known_issues) and as a prerequisite [here](../install/inst-agent/inst-agent-ubuntu.md#prerequisites).
* Improvements to the pmagent functionality in the event the Hosts UUID changes.
* The Agent Kerberos Ticket renewal in the event Active Directory Domain controller is unavailable at point of renewal. If the Agent is unable to contact the DC it moves to an unjoined status. With this fix it moves to a connecting status and continues to reattempt a renewal.
* Improvement to agent cache purging for users. Group cache will remain when associated with multiple users.
* Agent number reported on join is incorrect. *nix agent versions now display as short version number in ADUC, e.g. Thycotic Identity Bridge (1.0.1).
* Error resolved when loading __Server Manager | Tools | Active Directory Administrative Center__ with Identity Bridge installed on Server.
* When creating an Active Directory user's home directory on the *nix agent, it will pull the files and folders from the `/etc/skel` directory or the skeleton directory defined under `/etc/default/useradd`.
* Authenticating AD users shouldn't pass through `/etc/login.defs`. These should be AD defined.
* Show success message following a license import instead of reporting an error.
* Improved license import functionality. Errors will be better captured.
* Improved feedback to user when running an invalid custom json script for `syscfg` command.
* AD User login appears to be defaulting as Failover login.
* *nix Agents are now able to join Active Directory Domains when BASE enabled within the hosts /etc/openldap/ldap.conf file
* Changes to the Thycotic Configuration Utility > Custom Text > Friendly Messages > Account Expired filed are now being correctly applied.
