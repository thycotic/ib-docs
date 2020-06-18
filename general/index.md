[title]: # (General)
[tags]: # (panel)
[priority]: # (3)
# The General Panel

## Default User Settings

### Starting UID

The base UID that should be taken as starting point for all uid assignments

* Initial Starting UID: value should be 0
* Only positive numeric characters can be set
* A maximum of 9 numeric characters can be used
* ADUC → User Properties → Thycotic  
  * Generate button Should create a unique UID to the entire forest and higher than the Starting UID.
  * Generate button should not create a UID of an existing UID
  * Generate button should not create a UID lower than the Starting UID
  * Generate button with Algorithmic selected
    * Should generate a random number above the Starting UID value
  * Generate button with Incremental selected
    * Should generate a UID 1 higher than the previous one used

### Default Home Directory

Setting of the path that should be used for users when logging into the Linux\Unix host

* Initial Default Home Directory should be set to: `[systemhome]/[domain]/[username]`
* ADUC → User Properties → Thycotic
  * Default value should be displayed as: `{target home root}*\<domain\>**\<username\>*`
* Any Change made in Utility should be reflected in ADUC → User Properties → Thycotic
* Help message should be present make sense

### Default Login Shell

Define the shell you would like assigned to the user when logging into the Linux\Unix host

* Initial Default Login Shell should be set to: /bin/bash
* ADUC → User Properties → Thycotic:
  * Default value should be displayed as: /bin/bash
* Any Change made in Utility should be reflected in ADUC → User Properties → Thycotic
* Help message should be present make sense 

## Default Group Settings

### Starting GID

The base GID that should be taken as starting point for all gid assignments

* Initial Starting GID: value should be 0
* Only positive numeric characters can be set
* A maximum of 9 numeric characters can be used
* ADUC → User Properties → Thycotic:
  * Select the Assign Group button → Search and Select a group that doesn’t have a Thycotic GID assigned, should now be prompted to Set a GID for Group
    * Set GID button Should create a unique GID to the entire forest and higher than the Starting GID
    * Set GID button should not create a GID of an existing GID
    * Set GID button should not create a GID lower than the Starting GID
    * Set GID button with Algorithmic selected
      * Should generate a random number above the Starting GID value
    * Set GID button with Incremental selected
      * Should generate a GID 1 higher than the previous one used
  * Group name and GID should then be displayed.
* ADUC → Group Properties → Thycotic: 
  * Generate button Should create a GID Number higher than the Starting GID
  * Generate button should not create a GID of an existing GID
  * Generate button should not create a GID lower than the Starting GID
  * Generate button with Algorithmic selected
    * Should generate a random number above the Starting GID value
  * Generate button with Incremental selected
    * Should generate a GID 1 higher than the previous one used

### Primary Group name

Used to assign an existing AD group as the users primary group as Linux Account

* Select the assign group button
* Search and Select a group that does not have a Thycotic GID assigned, should now be prompted to Set a GID for Group
  * Set GID button Should create a GID Number higher than the Starting GID
  * Set GID button should not create a GID of an existing GID
  * Set GID button should not create a GID lower than the Starting GID
  * Set GID button with Algorithmic selected
    * Should generate a random number above the Starting GID value
  * Set GID button with Incremental selected
    * Should generate a GID 1 higher than the previous one used
* Group name and GID should then be displayed.
* Pick another – allows you to pick another group
* If a Group has a GID already assigned, group should be picked and be returned to Utility
* Should not be able to assign more than one group as Primary Group name

## UID Generation Mode

Defines the format in which the UID and GID will be generate starting from the defined Starting ID values

* Incremental – Will select the next ID available ID for user or group starting from the defined id
  * If a value has been previously assigned and removed it will not be added back to the available pool
* Algorithmic – Will randomly generate an available ID for user or group excluding the defined starting ID or lower
  * If a value has been previously assigned and removed it will not be added back to the available pool
* Utility → Primary Group Name → Assign group with no id – will open the assign GID modal
* ADUC → Group Properties → Thycotic – Drop down should be present and can be changed
* ADUC → User Properties → Thycotic – Drop down should be present and can be changed

## Lock Generator Mode

Stops users from being able to change the Generation mode in ADUC.

* ADUC → Group Properties → Thycotic – Drop down should be present
* ADUC → User Properties → Thycotic – Drop down should be present
