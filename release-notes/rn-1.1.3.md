[title]: # (1.1.3 Release)
[tags]: # (read me)
[priority]: # (30995)
# 1.1.3 Release Notes

_February 24th, 2021_:

## Bug Fixes

* When using "User Name Formatting" configurations from the Thycotic Configuration Utility ensure that Active Directory Users are able to update their passwords regardless of the username format they are assigned.
* When Active Directory updates the Computer Object Password, this is now correctly updated on the Agent to ensure continued Kerberos Ticket renewal between Active Directory and the Agent.

## Known Issues

* Updating the CentOS, Redhat Enterprise and Oracle Linux agents requires a change to the upgrade command and a pmagent service restart.
  * For RPM you will need to perform the following upgrade command:

    `rpm -U --force ./pmagent_x86_64_v1.1.3.xx_<platform>.rpm`
  * For YUM you will need to run the following downgrade command:

    `yum downgrade ./pmagent_x86_64_v1.1.3.xx_<platform>.rpm`
