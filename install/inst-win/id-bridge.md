[title]: # (.exe Install)
[tags]: # (setup)
[priority]: # (4)
# Installing the Thycotic Identity Bridge for Windows .exe file

The executable for the Identity Bride installation on Windows systems, checks for prerequisites and installed those before entering the actual product installation.

1. Double-click the downloaded Identity Bridge for Windows install executable.
1. The Thycotic Identity Bridge Bundle installer opens, click __Install__.

   ![id 1](images/id-1.png "Bundle info page")
1. The installer shows the progress of the prerequisites verification and installation.

   ![id 2](images/id-2.png "Setup progress")

   Once the prerequisites are applied the Installation wizard opens, click __Next__.

   ![id 3](images/id-3.png "Welcome dialog")
1. The install wizard shows the installed Prerequisites, click __Next__.

   ![id 4](images/id-4.png "Prerequisites installed dialog")
1. When Active Directory is detected, the Configure Active Directory dialog opens to the following:

   ![id 5](images/id-5.png "Configure Active Directory dialog")

   * Check the Install Thycotic Identity Bridge Property Sheets checkbox.
   * If you are logged in as the default user (Administrator), ignore the specific user detail setup.
   * Click __Configure AD__.
1. A successful AD Configuration is confirmed:

   ![id 6](images/id-6.png "Successful configuration confirmation dialog")

   Click __Next__.
1. Confirm or change the default Destination Folder path:

   ![id 7](images/id-7.png "Destination Folder dialog")

   Click __Next__.
1. Click __Finish__ once the setup completes.

   ![id 8](images/id-8.png "Finish dialog")
1. On the Setup Successful dialog, click __Close__.

   ![id 9](images/id-9.png "Close dialog")

You are now ready to open the Identity Bridge application, it will open to the Thycotic Identity Bridge Connect dialog.

![connect](images/connect.png "Connect dialog")

If you are the default user, you only need to click __Connect__. The Domain should have been automatically entered and the Mode drop-down is on the Current User option.

Refer to [Identity Bridge Configuration Utility](../../cfg-util/index.md) for details about the features of the configuration utility.
