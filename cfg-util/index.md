[title]: # (Configuration Utility)
[tags]: # (introduction)
[priority]: # (4)
# Identity Bridge Configuration Utility

The ID Bridge Configuration Utility allows the setting of values used in the Thycotic panels under Active Directory User and Computers and User and Group Properties.

These values are used to enable the ID Bridge to manage the user authentication from Linux/Unix hosts to Active directory.

The ID Bridge Configuration Utility will allow Global setting of all values and selected values at an OU level.Below are all panels that appear under the ID Bridge Configuration Utility, each page outlines the functionality of the Panel

## [General](general/index.md)

Default settings of values for User, Group, and OU attributes, including starting Id’s, default home and shell parameters.

## [ACL (Access Control List)](acl/index.md)

Assign Active directory groups at a global level to allow or deny login access to your Linux/Unix hosts.

## [Agent Settings](agent-settings/index.md)

Defaults for setting agent specific values, including Cached Logins, time sync, home directory permissions, and character separators.

## [Attribute Mapping](attr-map/index.md)

Allow Active directory values to be mapped to Thycotic ID Bridge fields. For example based on AD terms, Display Name is mapped to Unix Username.

## [Cache Settings](cache-set/index.md)

Sets the amount of time the local Linux/Unix agent will store a copy of the users password within the agent's encrypted database. This is required in the event the Agent is unable to contact AD to verify the users credentials.

## [Customer Variables](cust-var/index.md)

Allows the ID Bridge user to configure the custom attribute macros for use within the Default User & Group Settings.

## [Excluded Users](excl-users/index.md)

Provide a list of local user accounts that will automatically bypass the Identity Bridge portion of the authentication stack.

## [License](license/index.md)

Licensing panel to view, add, and remove Thycotic ID Bridge licenses.

## [Logging](logging/index.md)

Allows the Linux/Unix host to utilize SysLog functionality, either logging the agent information locally or to a defined remote SysLog server.

## [Custom Text](custom-msg/index.md)

Allows custom messages to be defined. The messages are displayed to user when accessing the Linux/Unix hosts.

## [OU Override](ou-override/index.md)

Shows an overview of where all Thycotic Identity Bridge configuration objects are stored in Active Directory.

## [File Menu](file-menu/index.md)

The [File Menu](file-menu/index.md) of the configuration utility offers options like:

* Location: Opens the location selector.
* Refresh: Refreshes configuration utility data.
* Restore all Defaults: Restores the utilities data to default values.
* Export Changes to File: Audit feature, only exports the changed values in the application.
* Go to Global Configuration: If user is not already in the global configuration selecting this option navigates to it.
* [Export Backup](file-menu/index.md#export_backup)
* [Import Backup](file-menu/index.md#import_backup)
