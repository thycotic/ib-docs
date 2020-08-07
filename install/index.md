[title]: # (Installation and Upgrades)
[tags]: # (setup)
[priority]: # (2)
# Installation and Upgrades

## Prerequisites

The agent should have a resolvable hostname set before installing the Thycotic Identity Bridge. If the agent has a default hostname of `localhost.localdomain`, the pmagent service will not function as expected.

**Note**: Updating the agent hostname post installation will require a reinitialization of the agent configuration.

## System Requirements

| **Operating System** | **Disk Space Requirements**  | **Minimum Memory** | **Other** |
| ----- | ----- | ----- | ----- |
| CentOS 7 | 100Mb 2mb in each of /lib64 /etc/pam.d /usr/lib64/security and /etc | 2Gb | For the Identity Bridge component to function correctly **SELinux** currently needs to be disabled on the host. |
