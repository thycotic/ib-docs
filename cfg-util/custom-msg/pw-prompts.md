[title]: # (Password Prompts)
[tags]: # (panel)
[priority]: # (5)
# Password Prompts

Password message types can be customized via the Custom Text tab in the configuration utility.

Select Password Prompts from the drop-down options.

![pwp](../images/pw-prompts.png "Custom Text tab in Configuration tool with Password Prompts selected")

>**Note**: Custom Variables cannot be used in the message fields.

## Active Directory

Password prompt text displayed to Active Directory users when logging into Linux/Unix host

* Default Active Directory value: Active Directory Password

## Local System

Password prompt text displayed to locally defined Linux/Unix users when logging into Linux/Unix host.

* Default Local System value: Local Password:

## Other

Password prompt text displayed when user accessing Linux/Unix host via 3rd party remote user credential service.

* Default Other value: Other Password

## Old Active Directory Password

Displayed when Active Directory users are changing their password on the Linux/Unix host.

* Request to define users existing password
* Default Old Active Directory Password value: Current Active Directory Password

## New Active Directory Password

Displayed when Active Directory users are changing their password on the Linux/Unix host.

* Request to enter a new password
* Default New Active Directory Password value: New Active Directory Password:

## Confirm New Active Directory Password

Displayed when Active Directory users are changing their password on the Linux/Unix host.

* Request to confirm new password
* Default Confirm New Active Directory Password value: Confirm New Active Directory Password

## Password Policy Violation

Displayed when Active Directory users are changing their password and the new password does not meet the Active Directory policy requirements.

* Request to meet the AD password policy requirements
* Default: The new password entered does not meet the password policy defined in Active Directory.