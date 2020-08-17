[title]: # (Installation and Upgrades)
[tags]: # (setup)
[priority]: # (2)
# Installation and Upgrades

## Prerequisites

The agent should have a resolvable hostname set before installing the Thycotic Identity Bridge. If the agent has a default hostname of `localhost.localdomain`, the pmagent service will not function as expected.

**Note**: Updating the agent hostname post installation will require a reinitialization of the agent configuration.

## System Requirements

### *nix

| **Operating System** | **Disk Space Requirements**  | **Minimum Memory** | **Other** |
| ----- | ----- | ----- | ----- |
| CentOS 7 | 100Mb 2mb in each of /lib64 /etc/pam.d /usr/lib64/security and /etc | 2Gb | For the Identity Bridge component to function correctly **SELinux** currently needs to be disabled on the host. |

### Windows & Active Directory Requirements

* Active Directory Forest Functional Level: Greater than or equal to 2012 R2 or newer
* Windows OS: Greater than or equal to Windows 2012 R2/Windows 7 (x64 only across all versions of Windows)
* Client Prerequisites:
  * Visual Studio C++ Redistributable 2019 x64 (https://aka.ms/vs/16/release/vc_redist.x64.exe)
  * Visual Studio C++ Redistributable 2019 x86 (https://aka.ms/vs/16/release/vc_redist.x86.exe)
  * ASP.NET Core 3.1 Runtime (v3.1.5) - Windows Hosting Bundle (https://download.visualstudio.microsoft.com/download/pr/7c30d3a1-f519-4167-b850-b9c49bf2aa0e/dbfa957a76a41a1e1795f59d400d4ccd/dotnet-hosting-3.1.5-win.exe)
  * .NET 4.5.2 (https://download.microsoft.com/download/E/2/1/E21644B5-2DF2-47C2-91BD-63C560427900/NDP452-KB2901907-x86-x64-AllOS-ENU.exe)

>**Note**:
> * If installing from the bundled installer/bootstrapper (ThycoticIdentityBridge_x64_{version}.exe), the client prerequisites will automatically be installed.
> * If installing the raw msi (ADBridge.Installer_x64_{version}.msi), the user will have to manually download and install the client prerequisites.

#### Windows 7

If you install the Identity Bridge on a Windows 7 system, please refer to the following Microsoft KB: https://support.microsoft.com/en-us/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot
