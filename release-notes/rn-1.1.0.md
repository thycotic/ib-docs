[title]: # (1.1.0 Release)
[tags]: # (read me)
[priority]: # (30998)
# 1.1.0 Release Notes

_November 24th, 2020_:

## Enhancements

Enhancements available with the 1.1.0 release of Identity Bridge.

* The [Message Tab](../cfg-util/custom-msg/index.md) in the Configuration Utility was split to provide friendly message setup.
* Overhaul and renaming of the Excluded Users tab now called [Exclusions](../cfg-util/excl-users/index.md).
* Full Configuration Utility backup support via ex- and imports options on the [File Menu](../cfg-util/file-menu/index.md).
* Added [DC Selector](../cfg-util/dc-selector.md) option to Configuration Utility.
* [User/Group support](../cfg-util/general/index.md) for multi-domain environments.
* The Primary Group configuration option was removed from the Configuration Utility and MMC extension.

## Bug Fixes

* Added libjansson for pmagent to fullfil prerequisite regarding Ubuntu 18.04 and 20.04 live server issue mentioned as a known issue [here](rn-1.0.1.md#known_issues) and as a prerequisite [here](../install/inst-agent/inst-agent-ubuntu.md#prerequisites).
* Changes to the Thycotic Configuration Utility > Custom Text > Friendly Messages > Account Expired filed are now being correctly applied.
* User Properties - Thycotic User Data Panel - Auto population of fields corrected when using Automatic POSIX data generation.
* Reduced number of PreAuth calls made to Active Directory when users authenticating against locally cached information.