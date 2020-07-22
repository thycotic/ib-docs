[title]: # (Password Prompts)
[tags]: # (panel)
[priority]: # (5)
# Installation and Upgrades

The prompt that will be displayed to the user on the Linux/Unix host during login.

![pwp](../images/pwp.png "Messages tab in Configuration tool")

## Local

Password prompt message displayed to users logging onto a Linux/Unix host with a locally defined account only

* Default value should be: Local Password:
* Field can be modified
* Currently no character limit on any field. This is subject to change.
* Only Unicode characters can be set
* Should be displayed to user when logging into Linux/Unix

## Active Directory

Password prompt message displayed to users logging onto a Linux/Unix host when Active Directory authentication is being used.

* Default value should be: Local Password:
* Field can be modified
* Currently no character limit on any field. This is subject to change.
* Only Unicode characters can be set
* Should be displayed to user when logging into Linux/Unix

## Other

In the event of the Linux/Unix agent using an alternative authentication method defined in the nsswitch configuration this message will be displayed at the password prompt.

* Default value should be: Local Password:
* Field can be modified
* Currently no character limit on any field. This is subject to change.
* Only Unicode characters can be set
* Should be displayed to user when logging into Linux/Unix
