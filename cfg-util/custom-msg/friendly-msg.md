[title]: # (Friendly Messages)
[tags]: # (panel)
[priority]: # (6)
# Friendly Messages

Friendly Message message types can be customized via the Custom Text tab in the configuration utility.

Select Friendly Messages from the drop-down options.

![friendly](../images/friendly-msg.png "Custom Text tab in Configuration tool with Friendly Messages selected")

## Welcome Message

Message displayed to all Active Directory users as they login to the Linux/Unix Hosts

* Supports customer variables in the message field, such as [username] and [hostname]
* Default Welcome Message: Welcome [username] to the Thycotic Identity Bridge on [hostname]

## Authentication Messages

Messages displayed to all Active Directory users when various Active Directory states are discovered upon logging into Linux/Unix hosts.

* Supports customer variables in the message field, such as [username] and [hostname]

### Show Friendly Messages

Option to enable/disable all Authentication messages.

* With trial license in place, option will be defaulted to enabled.
* With a perpetual is license applied, option will be defaulted to disabled, but it can be enabled.

### Account Disabled

Displayed when Active Directory user has been disabled within ADUC.

* Default Account Disabled value: User account [username] is disabled in Active Directory

### Account Locked

Displayed when Active Directory user account has become locked through to many invalid password attempts.

* Default Account Locked value: User account [username] is locked in Active Directory

### Access Control Deny

Displayed when the Active Directory user does not have a valid Access Control list entry within the Thycotic Configuration Utility.

* Default Access Control Deny value: No valid Access Control List (ACL) found for user [username] on [hostname]

### Account Expired

Displayed when Active Directory user account has passed defined Account expiry value in ADUC.

* Default Account Expired value: User account [username] has expired in Active Directory.

### Invalid Password

Displayed when Active Directory user enters an invalid password.

* Default Invalid Password value: Invalid Active Directory Password

### User Not Found

Displayed when username entered can not be found within Active Directory.

* Default User Not Found value: User account [username] not found in Active Directory
