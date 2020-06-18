[title]: # (Access Control List)
[tags]: # (panel)
[priority]: # (12)
# Access Control List

Assign Active directory groups at a Global level to allow or deny login access to your Linux/Unix hosts.

If the Access Control List is empty All users are granted allow permissions.

For best practice a group should contain both user and computer objects, to create an effective Access Control List.

## Accounts

### Add Groups

Opens the Active Directory Select Group modal and you can search and select
groups to be added to the ACL List.

* Only 1 group can be added at a time
* A Group can only be added to the list once

### Accounts Grid

* Account - Displays the Groups assigned to ACL
* State - Allowed/Denied
  * Allowed - Users within the assigned group will be allowed to login to the Linux/Unix agents running the Thycotic Universal Bridge
  * Denied - Users within the assigned group will be denied login access to the Linux/Unix agents running the Thycotic Universal Bridge
  * Denied will override when user assigned to multiple groups
* Remove - Option to remove group from the ACL list

### Pre-Cache User Login Credentials

* Waiting on clarification
* May be delayed until V2

### Display Error Message if Logon denied due to ACL

* If checked when users attempted to login with a denied group membership the defined message will be displayed
* __Message field__
  * Default value is blank
  * Field can be modified
  * Currently no character limit on any field. This is subject to change.
  * Only Unicode characters can be set
  * Should be displayed to user when access denied to Linux/Unix
