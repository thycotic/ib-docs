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

### POSIX Data for Users

Defines if User POSIX data to be defined by Active Directory before Users are able to login into the Linux/Unix Hosts.

* Default: Automatic
* Automatic - If there is no POSIX data on the user in Active Directory (i.e. No UID/Shell/Home Dir), then generate POSIX data for the user during authentication.
* Manual - POSIX data will need to be specified for each User in ADUC before being able to authenticate to Linux/Unix Hosts
* Always - Always generate POSIX data during authentication, even if POSIX data has been set on user  object

## Default Group Settings

### Starting GID

The starting GID that will be taken as starting point for all GID assignments.

* Initial Starting GID: value should be 1000000
* Only positive numeric characters can be set
* A maximum of 9 numeric characters can be used

### POSIX Data for Groups

Defines if Group POSIX data to be defined by Active Directory before Users are able to login into the Linux/Unix Hosts.

* Default: Automatic
* Automatic - If there is no POSIX data on the group in Active Directory (i.e. No GID), then generate POSIX data for the group during authentication.
* Manual - POSIX data will need to be specified for each Group in ADUC before being able to authenticate to Linux/Unix Hosts.
* Primary Group Only - Generate GID for users primary group if Primary Group does not have an existing GID.
* Always - Always generate POSIX data during authentication, even if POSIX data has been set on group object.

## Default Computer Settings

### Default Computer Container

Defines the default OU container for Linux/Unix Hosts joining the Active Domain.

* Default: CN=Computers
