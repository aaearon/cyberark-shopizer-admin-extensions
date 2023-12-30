# cyberark-shopizer-admin-extensions

CyberArk PSM connector and CPM plugin for the Shopizer Administrator portal. These extensions were created as part of a [blog series](https://timschindler.blog/series/shopizer-admin-ext) that can be found at [https://timschindler.blog](https://timschindler.blog).


# CyberArk PSM connection component

Developed as part of the article [Creating a CyberArk Privileged Session Manager connection component for a web application](https://timschindler.blog/creating-a-cyberark-privileged-session-manager-connection-component-for-a-web-application).

The PSM connector is found in the `psm` folder. It contains the following file:

* `CC-PSM-ShopizerAdministrator.xml` - The xml representation of the PSM connection component.

`CC-PSM-ShopizerAdministrator.xml` can be used to create a PSM connection component package and the package be imported via the PVWA. `New-PASConnectionComponentPackage` as part of [`New-PASExtensions`](https://github.com/aaearon/New-PASExtensions) can be used to easily create a platform package from these files.


## CyberArk CPM plugin

Developed as part of the article [Creating a CyberArk Central Policy Manager plugin for a web application]().

The CPM plugin is found in the `cpm` folder. It contains the following files:

* `Policy-TimSchindlerShopizerAdministratorAccounts.ini` - Contains the Automatic Password Management part of a platform that can be used to manage Shopizer Administrator accounts.
* `Policy-TimSchindlerShopizerAdministratorAccounts.xml` - Contains the General and UI & Workflows parts of a platform that can be used to manage Shopizer Administrator accounts.
* `ShopizerAdministrator.ini` - The WebFormFieldsFile that contains the commands for each of the three CPM operations (Verify, Change, Reconcile).
* `shopizeruser.ini` - A file that contains parameters to be used when [testing the CPM plugin](https://docs.cyberark.com/PAS/Latest/en/Content/Plugins/CPM_WebApplication.htm#Step3Testtheplugin).

`Policy-TimSchindlerShopizerAdministratorAccounts.ini`, `Policy-TimSchindlerShopizerAdministratorAccounts.xml`, and `ShopizerAdministrator.ini` can be combined into a platform package and imported via the PVWA. `New-PASPlatformPackage` as part of [`New-PASExtensions`](https://github.com/aaearon/New-PASExtensions) can be used to easily create a platform package from these files.
