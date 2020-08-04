[title]: # (ADUC Extensions)
[tags]: # (panel)
[priority]: # (3)
# ADUC Extension

The Thycotic Identity Bridge Extension provides Thycotic Panels in Active Directory Users and Computers (ADUC) MMC for a number of container types.

The Thycotic extension panel can accept settings from the ID Bridge Configuration Utility allowing certain fields to be pre-populated, although there is no dependency between the Utility and the Extension.

From the Thycotic panel you can manage fields independently as well as generate UID and GID values for users and groups respectively.

## Users - Thycotic User Data Panel

* Panel that allows you to manage the ID Bridge values on an individual user basis.
* This includes UID Number, primary group membership and additional Linux/Unix user attributes.

## Users - Thycotic User Mapping Panel

Panel that allows creation of an alternate username (logon alias) which can be used when accessing the Unix/Unix host.

## Groups - Thycotic Group Data Panel

* Panel that allows you to manage the ID Bridge values on an individual group basis.
* This includes GID Number, Description and additional Linux\Unix group attributes.

## OU's - Thycotic Overrides Panel

Allows override of some global POSIX user fields at the OU level.

## Computers - Thycotic Identity Bridge Panel

Displays a list of all the Active Directory users that can access this computer and their associated user mapping name (username alias).
