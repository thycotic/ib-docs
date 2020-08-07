[title]: # (Agent Settings)
[tags]: # (panel)
[priority]: # (4)
# Agent Settings

Interface with Linux/Unix agents to manage user account locally defined on the agents.

![agent settings](../images/agent-settings.png "Agent Settings tab of the Bridge Configuration tool")

## Authentication Settings

### Allow Cached Logon

Allows Active Directory Users to access Linux\Unix hosts using the encrypted cached information stored on the host

* A user must of logged onto the Linux\Unix Host previously for a cache entry to of been created.
* Default value for Allow Cached Logon: Enabled.

### Time Sync

Updates the Linux\Unix Hosts date & time to be the same as the Domain Controller of the Active Directory.

* Synchronises date and Time upon the host joining the Domain
* Enables a service on the host to keep the time within a minute of the Domain Controller
* Default value for Time Sync: Enabled

## GID/UID Generation

### UID Generation Mode

Defines the format in which the UID and GID will be generate starting from the defined Starting ID values.

* Incremental – Will select the next ID available ID for user or group starting from the defined id
  * If a value has been previously assigned and removed it will not be added back to the available pool
* Algorithmic – Will randomly generate an available ID for user or group excluding the defined starting ID or lower

## Separator Characters

Replacement character for names with spaces
Defines how spaces in User and Group names will be displayed on the LInux\Unix hosts

* Default value Replacement character for names with spaces: ^