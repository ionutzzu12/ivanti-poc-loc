---
title: Managing Windows Applications
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

Users can manage (Import, Configure, Schedule, Distribute, Update, and Remove) the complete app life cycle for Windows applications. The app distribution and app update processes are supported through the MDM console. For more details on managing Windows apps and other applications, see [**App Configuration**](./App_Configuration.md), [**App Insights**](./App_Insights.md), and [**App Catalog**](./App_Catalog.md).

### Supported app types

- In-house (Check options in **Adding an In-house app** from the section [**App Catalog**](./App_Catalog.md))
- MSB (Microsoft Store for Business integration)
- Public store (via native Microsoft Store Integration) Microsoft Store Region can be set in Apps > Catalog Settings. For more information, see **Adding an app from a public store** from the section [**App Catalog**](./App_Catalog.md).

### Supported app extensions

- MSI
- MSIX
- APPX
- APPX bundles
- EXE (via [**Ivanti Bridge**](./Ivanti_Bridge.md))

### App Control

The App Control configuration controls the app installation per device. For more information, see [**App Control Configuration: Control Which Apps Are Installed Per Device**](./App_Control_Configuration__Control_Which_Apps_Are_Installed_Per_Device.md).

### Packages and Dependencies

The following different features are available: 

1. Windows apps can be set as prerequisites for all types of applications. For information on how to set app prerequisites, see [**Deploying app dependencies**](./Deploying_app_dependencies.md).
2. The APPX and APPX bundles App Dependencies and Other Packages dependencies. On the [**Viewing App Details**](./Viewing_App_Details.md) page, review the **App Dependencies and Other Packages** section.
3. Win32 apps support the selection of the correct product code (MSIs) and command lines and variables. A list of common command line options can be found [**here**](https://learn.microsoft.com/en-us/windows/win32/msi/command-line-options).

### Scripts

Scripts are supported via Ivanti Bridge Client. For information on setting up the Scripts, see the [**Ivanti Bridge**](./Ivanti_Bridge.md)

Once Ivanti Bridge is installed on the devices, the scripts can be distributed as follows:

- At device level with the Scripts and Actions via Ivanti Bridge Action
- Via the Ivanti Bridge Configuration (go to Configurations > Bridge)

### Pre-install and post-install scripts and files

**For .exe files and .MSI files**

You can configure pre and post-PowerShell install scripts, registry scripts, and Windows executable (.exe) files and download other types of files for Windows apps at the App Details level.

When adding a new pre or post install script or file, the Ivanti Bridge screen appears. You can attach the script or file, add script argument and also provide a target location for the files. The pre-install script must be executed successfully on the device before sending the app installation command to the device. The pre and post install scripts and files will be executed / installed in the same order in which they were uploaded to the console. If the pre-install script download or installation fails, the app installation cannot proceed further.

If the post-install script fails, you can view the errors in the Device details page under the Device logs section. Also, you cannot revert the pre-install scripts / downloaded files and installed .exe files in case the post-install actions fail.

You can reorder the pre-install or post-install scripts and files using the Prioritize Scripts and Files option. This option will be available only if there are at least two or more scripts or files available. Using this option, you can drag and drop the files or scripts within their respective pre or post sections, and not from one section to another.

### Installation behavior and configurations

Windows applications support the following features:

- Silent installations
- [**Windows app scheduling**](./Windows_app_scheduling.md)
- Reboot options

For more details on installation behavior options, see [**App Configuration**](./App_Configuration.md)

MSI apps and EXE apps (installed using Bridge) support installations with user-less MDM sessions.

For example, in the following scenarios:

- The device was restarted, and no user is logged-in yet
- The user logged out from the Windows session
- The device was enrolled in Autopilot user-less (Self-deploying or Pre-provisioning) mode
- Applications are installed at the device level

It allows installing the MSI apps in more efficient ways, for example, during Auto-pilot enrollment or during the night when nobody works on the Windows device. When simple repacking is used for EXEs in MSI, it can be installed, but not upgraded or deleted. The real MSI package has a connection with CSP. Other Application types will be installed after the user logs in.

### Tunnel for Windows (Per-App VPN)

Tunnel is a stand-alone native Windows application. It is currently available in the Microsoft Store for distribution to devices. Creates a Per-App VPN Configuration. Sentry deployment is required. To configure the Tunnel app, go to **Configurations** > **+Add** > Search for Tunnel (choose the Configurations that support Windows devices). Select the Sentry profile and configure settings to start tunneling the app data via Sentry. To set up a Sentry Server, go to **Admin** > **Infrastructure** > **Sentry**.

### App Inventory

Application and Software Inventory installed in your Windows Device fleet can be tracked at two levels:

- To check applications installed across your devices, go to **Devices** > **App Inventory**
- To check inventory at the device level, go to Devices > choose a device > click on Installed Apps

Administrators can set Windows application inventory collection intervals. Go to Admin > Windows > App Inventory Intervals The intervals are used when privacy configuration is set to collect all apps from the device. To configure the Privacy Configuration, go to Configurations > +Add > search for Privacy > Choose Collect apps Inventory For all apps on the device. Select app types to be collected.

### Corporate App Catalog (Apps\@Work)
