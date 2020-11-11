[title]: # (Excluded Users)
[tags]: # (panel)
[priority]: # (4)
# Excluded Users

Allows to provide a list of local and domain user accounts that will automatically bypass the Identity Bridge portion of the authentication stack. This excludes the domain the configuration utility is connected to.

Groups are masked from the list. It's possible to define individual or ranges of UIDs and GIDs to be excluded.

![excluded users](../images/excl-users.png "Excluded Users tab of the Bridge Configuration tool")

## User and/or Group Exclusions

### Add

Open a text based modal where the Linux/Unix username can be defined and added to the list of excluded user.

### Filter

Allows the defined excluded user list to be filtered.

## Exclusions Panel

The panel shows the applied exclusions types, the values assigned and an option to remove.

### User(s)

Users will automatically bypass the Identity Bridge portion of the authentication stack on the *nix agents.

* Users can be defined singular or by a comma separated list
* Both Local and Active Directory users can be defined
* Default: root
  * By default the root user will always bypass the Identity Bridge portion of the authentication stack on the *nix agents.

### UID(s) Number

UID value/range will be excluded as an applicable value as UID Number in the Thycotic User Data extension of ADUC.

* UID numbers can be defined as a single value, comma separated list or range of values
* Default: 0 - 500

### GID(s) Number

GID value/range will be excluded as an applicable value as UID Number in the Thycotic User Data, Thycotic Group Data and Thycotic Overrides extensions of ADUC.

* GID numbers can be defined as a single value, comma separated list or range of values
* Default: 0 - 500

### Domain

Users defined within the domain will automatically bypass the Identity Bridge portion of the authentication stack on the *nix agents.

* The domain is required to be defined in full FQDN format, for example: child.demo.com.
* Exclusion will not apply to the root domain the Configuration Utility is connected to.

### Group(s)

Defined Groups will be masked from the Active Directory users group list on the *nix agent.

* Groups can be defined singular or by a comma separated list.