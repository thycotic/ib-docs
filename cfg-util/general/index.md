[title]: # (General)
[tags]: # (panel)
[priority]: # (5)
# The General Panel

Default settings of values for User and Group attributes, including starting ID’s, default home and shell parameters.

![general](../images/general.png "General tab of the Bridge Configuration tool")

## Default User Settings

### Starting UID

The starting UID that will be taken as starting point for all uid assignments.

* Default: value should be 1000000
* Only positive numeric characters can be set
* A maximum of 9 numeric characters can be used

### Default Home Directory

The Home Directory Path that be used for users when logging into the Linux/Unix host.

* Default: [systemhome]/[domain]/[username]

### Default Login Shell

The Shell that will be assigned to the user when logging into the Linux/Unix host.

* Default: /bin/bash 

### Check All Domains

This setting forces searches to halt if a domain being searched is offline. If this setting is disabled, such domains will be ignored and the search will continue on available domains.

* Check All Domains unchecked by Default

### POSIX Data for Users

Defines if User POSIX data to be defined by Active Directory before Users are able to login into the Linux/Unix Hosts.

* Default: Automatic
* Automatic - If there is no POSIX data on the user in Active Directory (i.e. No UID/Shell/Home Dir), then generate POSIX data for the user during authentication.
* Manual - POSIX data will need to be specified for each User in ADUC before being able to authenticate to Linux/Unix Hosts
* Always - Always generate POSIX data during authentication, even if POSIX data has been set on user  object

### Duplicate User Processing

Defines how Identity Bridge will process Duplicate Active Directory usernames when user logs into the Linux/Unix Hosts.

* Default: Automatic
* Never - Ignore Duplicate users
* Automatic - Generates a unique user name by adding or appending the domain information to the user for all domains except for the joined domain.
* Only Duplicates - Generates a unique user name by adding or appending the domain information to the user when a duplicate name is detected.
* Always - Generates a unique user name by adding or appending the domain information to the user for all domains.

### Duplicate User Format

Defines the format for the Active Directory username displayed on the Linux/Unix Host when the Active Directory username is duplicated due to a multi-active Domain environment.

* Default: Domain/User
* Domain/User - Example: demo/user1
* User_Domain - Example: user1_demo
* User@Domain - Example: user1@demo

## Default Group Settings

### Starting GID

The starting GID that will be taken as starting point for all GID assignments.

* Initial Starting GID: value should be 1000000
* Only positive numeric characters can be set
* A maximum of 9 numeric characters can be used

### POSIX Data for Groups

Defines if Group POSIX data to be defined by Active Directory before Users are able to login into the Linux/Unix Hosts

* Default: Automatic
* Automatic - If there is no POSIX data on the group in Active Directory (i.e. No GID), then generate POSIX data for the group during authentication.
* Manual - POSIX data will need to be specified for each Group in ADUC before being able to authenticate to Linux/Unix Hosts.
* Primary Group Only - Generate GID for users primary group if Primary Group does not have an existing GID.
* Always - Always generate POSIX data during authentication, even if POSIX data has been set on group object.

### Duplicate Group Processing

Defines how Identity Bridge will process Duplicate Active Directory groups with
users logging into the Linux/Unix Hosts

* Default: Automatic
* Never - Ignore Duplicate groups
* Automatic - Generates a unique group name by adding or appending the domain information to the group for all domains except for the joined domain.
* Only Duplicates - Generates a unique group name by adding or appending the domain information to the group when a duplicate name is detected.
* Always - Generates a unique group name by adding or appending the domain information to the group for all domains.

### Duplicate Group Format

Defines the format in which the Active Directory group will be displayed on the Linux/Unix Host when the Active Directory username is duplicated due to a multi-active Domain environment.

* Default: Domain/Group
* Domain/Group - Example: [demo](http://demo.com)/group1
* Group_Domain - Example: group1_demo

## Default Computer Settings

### Default Computer Container

Defines the default OU container for Linux/Unix Hosts joining the Active Domain.

* Default: CN=Computers
