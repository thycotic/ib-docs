[title]: # (Logging)
[tags]: # (panel)
[priority]: # (6)
# Logging

Allows the Linux/Unix host to utilize SysLog functionality, either logging the agent information locally or to a defined remote SysLog server.

![logging](../images/logging.png "Logging tab of the Bridge Configuration tool")

>**Note**: Making changes to the syslog settings in the Configuration Utility, will also require a restart of the *nix Agent for the updated settings to take effect.

## Logging

### Turn on SysLog

Defines if Agent logging also sent to SysLog as well as existing agent pmlog.

* Default: Disabled

### Log Successful/Failed Authentications

Sends Active Directory Authentication outcomes to the syslog.

* Default: Disabled

### Log Send Friendly Messages

Send Friendly Messages displayed to users to syslog.

* Default: Disabled

### Log Send Warning Messages

Send Warning Messages displayed to users to syslog.

* Default: Disabled

### Protocol

The communication protocol used to send Linux/Unix host information to SysLog.

* Default: TCP

### Facility

Defines the Linux\Unix host process component that will be sent to the SysLog.

* Default: Auth

### Type

Defines if Linux\Unix host will use a local or remote SysLog server.

* Default: Local
* If remote selected the Remote SysLog server and Remote SysLog port fields will become enabled.

### Remote SysLog Server

Defines the address of the remote SysLog server to which the Linux/Unix hosts send their defined SysLog information.

* Default: Blank
* When enabled defined by the resolvable host name or IP address.

### Remote SysLog Port

Defines the port SysLog uses for communication.

* Default: 0
