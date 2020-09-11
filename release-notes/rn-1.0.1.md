[title]: # (1.0.1 Release)
[tags]: # (read me)
[priority]: # (30999)
# 1.0.1 Release Notes

_September 29th, 2020_:

## Bug Fixes

* Improvements to the pmagent functionality in the event the Hosts UUID changes.
* The Agent Kerberos Ticket renewal in the event Active Directory Domain controller is unavailable at point of renewal. If the Agent is unable to contact the DC it moves to an unjoined status. With this fix it moves to a connecting status and continues to reattempt a renewal.
