[title]: # (Identity Bridge)
[tags]: # (introduction)
[priority]: # (1)
# Thycotic Identity Bridge

Thycotic's __Identity Bridge__ (ID Bridge) is a utility that allows the setting of values to be used in the Thycotic panels under Active Directory User and Computers, User and Group Properties. These values are used to enable the ID Bridge to manage the user authentication from Linux\Unix hosts to Active directory.

The ID Bridge Configuration Utility allows to globally set all values and selected values at an organizational unit (OU) level.

Below are all panels that appear under the ID Bridge Configuration Utility, each page outlines the functionality of the Panel

## General

Default settings of values for User and Group attributes, including starting Id’s, default home and shell parameters.

## Authentication

Defines ACL and User attribute requirements for authenticating against the Active Directory. Setting of Home directory permissions and syncing of local Linux\Unix passwords with Active Directory.

## Password Prompts

Defines the Password prompt text the user will see for different access types on the Linux\Unix host.

## Attribute Mapping

Allow Active directory values to be mapped to Thycotic ID Bridge fields. For example based on AD terms, Display Name is mapped to Unix Username.

## Cache Settings

Sets the amount of time the local Linux\Unix agent will store a copy of the users password within the agent. This is required in the event the Agent is unable to contact AD to verify the users credentials.

<!--
## Logging (Not implemented)

Allow Thycotic actions to be logged under the Servers syslog functionality

## License (Not implemented)

Licensing Thycotic ID Bridge functionality - to be defined

## *nix Hosts (Not implemented)

Allows the definition of locally defined Linux\Unix accounts that will be allowed to bypass the ID Bridge authentication protocol. These might be users such as root
-->

## Customer Variables

Allows the ID Bridge to use attributes from AD (and in the future results of scripts and Linux\Unix variables) in items that happen on the Linux\Unix host.

## ACL (Access Control List)

Assign Active directory groups at a global level to allow or deny login access to your Linux\Unix hosts.
