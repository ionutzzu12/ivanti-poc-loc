---
title: App Configuration
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Licensing for app features**](./App_Configuration.md)
- [**Configuration steps common to multiple apps**](./App_Configuration.md)
- [**Hide and Suspend Apps (Android only)**](./App_Configuration.md)
- [**Configuring Network Relay**](./App_Configuration.md)
- [**Configuring Cellular 5G Slicing**](./App_Configuration.md)
- [**Distributing Application using Web Content Filter Configuration**](./App_Configuration.md)
- [**Distributing Application using DNS Proxy**](./App_Configuration.md)

App configuration enables you to customize the installation, promotion, and distribution of each app you deploy to your users' devices. The apps can be your own in-house apps, apps from a public store, or Ivanti Neurons for MDM apps. You have the flexibility to deploy the apps to many different users and groups with unique names and configurations specifically tailored to each recipient. The number of in-house application versions is limited to 100. If that number is exceeded, the Ivanti Neurons for MDM system purges the oldest versions of the application. The status of the application upload and purge is listed and is visible from the Audit Trails page.

When you change the values for the app configuration of an app in the app catalog or in the managed app configuration profile, one or two device check-ins are necessary for the device to receive the new configuration values.

## Licensing for app features

The following features require additional licensing:

- Silent app install/uninstall: Silver license
- Per-app configuration: Gold license
- AppConnect custom configuration: Gold license

Multiple application packages require good group management as future device types could not be defined by the Windows OS. In such a case the only way of installing proper version of the app is for the admin to use the correct group to the correct application.

## Configuration steps common to multiple apps

Do these steps first and then proceed with configuration steps for each app you want to deploy. You can design multiple configurations of the same app and give each configuration a unique name. Each configuration can have its own distribution and promotion levels to fit your deployment strategy. The number of in-house application versions is limited to 100. If that number is exceeded, the Ivanti Neurons for MDM system purges the oldest versions of the application. The status of the application upload and purge is listed and is visible from the Audit Trails page. You can deploy an application to a maximum of 100 Users, Users Group, Device, or Device Group at once. You can select an app to add to the App catalog. Ivanti Neurons for MDM has an asynchronous process to Send Install/Update Request command for iOS apps. When you use the Send Install/Update Request command, the Ivanti Neurons for MDM administrative portal displays a message that the:

- process will continue to run in the background
- process is complete
- status whether the process is successful or if there are any errors

**Procedure**

1. Go to **Apps > Apps Catalog** and click **+Add**.
2. Use the pull-down menu to select either the App Store, Google Play or your In-House app store and choose an app to add to the catalog.Depending on your licensing agreement, you might also have apps available to add to your catalog.
3. Optionally, edit the Category of the app.
4. Optionally, add a brief description of the app in the **Description** field.
5. Click **Next**.
6. Choose a distribution level for this configuration of the app:\* **To everyone** - The app is added to all the user compatible devices.
   - **To no one** - The app is staged for distribution at a later date.
   - **Custom Distribution** - Select any of the following options:\* **User/User Groups** - The app is distributed to only the users or user groups you choose.Click the **Users** tab to select the user(s).Click the **User Groups** tab to select the user group(s).
     - **Device/Device Groups** - The app is distributed to only the devices or device groups you chooseClick the **Devices** tab to select the device(s).Click the **Device Groups** tab to select the device group(s).
7. Click **Next**.

### Configuring installation options

You can select the installation configuration options.

**Procedure**

1. Click **Install Application configuration settings** or click the **+** icon to add another configuration to view the **Configuration Setup** page.
2. Enter a name for the configuration in the **Name** field.
3. Optionally, enter a brief description of the installation configuration in the **Description** field.
4. Select the **Device Installation Configurations** option.
5. Select one of the following options:\* **Require installation on device**
   - **Install only once at device registration**
6. Select the **Do not require a specific app version** option to avoid downgrading an already installed app to a lower version. This option is available only for modern apps.
7. Select the following options:1) - **Silently install on Samsung Knox workspace and Zebra devices&#x20;**(Android Only)
   - **Do not show app in end user App Catalog**.
   - **Do not install app on newly enrolled devices**: Existing devices will not be impacted and will still display the app in the device app catalog.\* For any newly enrolled devices in this distribution, the app will not be listed or pushed.
     - If the admin triggers a send install/update command, the command will be sent to the device.
   - **App Update Mode** (supported for AMAPI devices as well). (Android Only)Use this option to update an app to the latest version using one of the following three modes:- **Default**: This mode is selected once you select the App Update Mode option. In this mode, the update happens within 24 hours from the time of app availability.- **Postpone for 90 days**: If you select this update mode, you can postpone the app updates for 90 days. After 90 days, the apps are updated automatically based on other settings made in Managed Google Play configuration.\* **High Priority**: If you select this update mode, and the user’s device is online, the app gets updated immediately after it is available on the Google Play Store.
   - **Set App Install Priority** - see the Configuring app priority topic for more details
8. On Android devices, the app updates are allowed using the Auto Update option even without selecting the Silent Install option. Administrator can control app updates on apps which are not mandatory or the apps which are self-installed by the user.
   You may encounter additional configuration options, depending on the chosen app. These options may include the ability to add multiple Key and Value pairs. In such cases, click **+ Add** to enter Key and Value pairs. For more information, see **Adding an app from a public store** in [**App Catalog**](./App_Catalog.md).
9. (macOS 11+) Select the options to install and configure the apps as managed apps:\* **Install as Managed App**
   - **Convert to as Managed App**In macOS 12.0+, Managed App support is available on user enrolled devices.

## Hide and Suspend Apps (Android only)

For Android devices in the following modes, **work profile**, **fully managed device**, **fully managed device with work profile**, and **work profile on company-owned device**, you can now hide or suspend apps after installation.

**Procedure**

|   | 1. | Install one or more apps on the device for which you want to apply the Hide or Suspend action. |
| - | -- | ---------------------------------------------------------------------------------------------- |

|   | 2. | Create an App Control Configuration and add the managed apps to Hide or Suspend list. |
| - | -- | ------------------------------------------------------------------------------------- |

|   | 3. | Apply the changes to the device. |
| - | -- | -------------------------------- |

If an app is present in both Hide and Suspend lists, then the app will be hidden because the Hide list will be prioritized.

### Configuring app priority

You can define the order in which apps are received on the device when it is first registered (specifically, within the first 20 minutes after registration date and time) and required apps are being pushed to install. You can prioritize downloading of specific apps before other apps. For example, prioritizing the download of Tunnel and Email apps before other non-critical apps. This feature is applicable for public and private apps. Prerequisite apps are pushed before dependent apps.

This feature is supported on iOS (except AppStation for iOS), Android (except Android for Enterprise), macOS (in-house PKG apps and Apple Apps and Books apps), and Windows devices.

This feature is available for new registration devices. By default, all apps are set to Medium priority. During this process, the user can select to manually install any app in the catalog even though that app will compete for resources to install and may queue before high priority apps.

In the case of Windows apps, the Bridge app has the highest priority than other apps.

See the previous section, "Configuring installation options" for the procedure to set the priority of an app using the **Set App Install Priority** option. You can set High, Medium, or Low priority for an app. Apps with same priority will be installed in no particular order. App priority is not used during app updates, when the user has already installed the app.

### Selecting Apple Application Management Configuration settings

These settings will apply to this app only and will override any global settings selected in the **Apps > Catalog Settings**. To select **Apple App Management** settings.

**Procedure**

1. Click **Apple Apps settings** or click the **+** icon to add another configuration to view the **Configuration Setup** page.
2. Enter a name for the configuration in the **Name** field.
3. Enter a brief description of the configuration in the **Description** field.
4. Select or deselect one or more of the following options from the **Apple Management Settings**:\* **Prevent backup to iCloud and iTunes**
   - **Remove apps on un-enrollment**
   - (iOS 14.0+) **Allow removal and offloading of this app** - You can deselect this option to prevent a user from removing and offloading a managed app.
   - (Optional) Add an **Apple Managed App Configuration**
5. Click **Update**.

### Selecting App Promotion levels

You can set the level of promotion for the app.

**Procedure**

1. Click **Promotion distribution configuration settings** or click the **+** icon to add another configuration to view the **Promotion configuration** page.
2. Click **Edit**.
3. Enter a name for promotion distribution configuration settings in the **Name** field.
4. Optionally, enter a brief description of the configuration in the **Description** field.
5. Select the level of promotion you want the app to receive, **Not Featured**, **Featured List**, or use **Feature Banner**. If **Not Featured** is selected the app will not be listed.
6. If you select Featured Banner specify the following details:1) **Title** - Specify the application title
   2\) **Description** - Specify the application detail
   3\) **Banner style** - Select a banner color
7. Click **+ Add Description** to enter a brief description of the configuration.
8. Optionally, change the distribution of the configuration.
9. Click **Done** to save the app configuration.

### Configuring AppTunnel traffic rules

Use the AppTunnel configuration to define traffic rules to allow access to services using Sentry.

For information about adding an AppTunnel configuration, see "Adding an AppTunnel configuration" in the *AppConnect Guide for Ivanti Neurons for MDM*.

### Configuring Managed app

**Procedure**

1. Click the **+** icon to open the configuration page.
2. Click **+ Add Description** to enter a brief description of the configuration.
3. Click **+ Add** to enter a Key and Value.
4. Choose a distribution level.
5. Click **Next**.

### Configuring a VPN for each app using Per App VPN

**Procedure**

1. Click the **+** icon to open the configuration page.
2. Enter a name for the VPN for this app in the **Name** field.
3. Click **+ Add Description** to enter a brief description of the configuration.
4. Click the **Enable Per-App VPN for this app** option and select an available Per-App VPN configuration.
5. (Optional) For macOS apps, enter **Designated Requirement** string in the format, identifier "\\%s\\". For example, identifier "com.google.Chrome". Use this field to enable a multiple package macOS app to use a Per-App VPN like Tunnel.
6. Choose how to **Distribute this App Config**.
7. Click **Next**.

### Using Apple Managed App Configuration

Using the Apple Managed App Configuration, specific settings can be configured for the installed managed app. An application might have some configuration parameters implemented or restricted by the developer. For applications with such restrictions your configuration options might be limited. You can configure Apple managed apps.

**Procedure**

1. Go to **Apps > App Catalog**.
2. Select an app.
3. Click the **App Configurations** tab.
4. Click **Apple Managed App Configuration** or click the **+** button.In the Apple Managed App Configuration there are some default configuration settings in place.
5. Click **Add** to add another configuration, if needed. Optionally, click name of the configuration to edit the configuration.
6. Under **Configuration Source** select any of the **Source Type** options\* **AppConfig Community** - This option is available only for those apps that have an app configuration specification available in the community repository. If this option is available, it is selected by default.
   - **Use .xml\*\*\*\*spec** - Select this option to upload the schema for the app to push a particular version of app configuration. Click **Choose File** to upload the .xml file. Ensure that the .xml file contains the bundle ID and the version. An error message will be displayed if the bundle ID in the file does not match with the bundle ID of the app.
   - **None** - Select this option if you do not want to apply any schema for the app. This option is selected by default if the **AppConfig Community** option is not available.The uploaded .xml file is displayed in the **Configuration Source** section. Click the Delete icon to delete the uploaded .xml file.
7. In the **Apple Managed App Settings**, you can set the configuration options to enter key value pairs.- Click **Add** to add the key value pairs to the managed app configuration to retrieve the registration name identity by Go client during iReg or Apple Device Enrollment.You can select the data types (String, Integer, Boolean, Long Float, Double, Date, String Array, Integer Array, Double Array, Float Array, Long Array) for the key value pairs.Add the following key value pairs to the managed app configuration to retrieve the registration name identity by Go client during iReg or Apple Device Enrollment:

| **Key**                                                                                                                                                                           | **Value**                                                 | **Type**          |                                                                                                                                                                                                                                                                                |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| registration.username                                                                                                                                                             | $\{userEmailAddress}                                      | STRING            |                                                                                                                                                                                                                                                                                |
| registration.token                                                                                                                                                                | $\{zeroTouchClientRegistrationNonce}                      | STRING            |                                                                                                                                                                                                                                                                                |
| registration.token.expirationSeconds                                                                                                                                              | $\{zeroTouchClientRegistrationNonceExpiresAtSeconds}      | STRING            |                                                                                                                                                                                                                                                                                |
| registration.url                                                                                                                                                                  | $\{clientRegistrationUrl}                                 | STRING            |                                                                                                                                                                                                                                                                                |
| Add the following key value pairs to the managed app configuration to retrieve the registration name identity by mac agent (Mobile\@Work) during iReg or Apple Device Enrollment: |                                                           |                   |                                                                                                                                                                                                                                                                                |
| **Key**                                                                                                                                                                           | **Value**                                                 | **Type**          |                                                                                                                                                                                                                                                                                |
| ---------------------                                                                                                                                                             | --------------------------------------------------------- | --------          |                                                                                                                                                                                                                                                                                |
| ClientRegistrationUrl                                                                                                                                                             | $\{clientRegistrationUrl}                                 | STRING            |                                                                                                                                                                                                                                                                                |
| Token                                                                                                                                                                             | $\{zeroTouchMacOSClientRegistrationNonce}                 | STRING            |                                                                                                                                                                                                                                                                                |
| TokenExpiresAt                                                                                                                                                                    | $\{zeroTouchMacOSClientRegistrationNonceExpiresAtSeconds} | STRING            |                                                                                                                                                                                                                                                                                |
| If the end user terminates the Ivanti Go application, click **Edit** to set the application to do one of the following:                                                           |                                                           |                   |                                                                                                                                                                                                                                                                                |
| Key                                                                                                                                                                               | Value                                                     | Type              |                                                                                                                                                                                                                                                                                |
| ----------------------------------------------------------                                                                                                                        | -------------------                                       | ----------------- |                                                                                                                                                                                                                                                                                |
| To display default notification use the following values:                                                                                                                         |                                                           |                   |                                                                                                                                                                                                                                                                                |
| enableAppTerminationNotification                                                                                                                                                  | True/False OR 1/0                                         | Boolean OR String |                                                                                                                                                                                                                                                                                |
| To Display a custom notification use the following values:                                                                                                                        |                                                           |                   |                                                                                                                                                                                                                                                                                |
| appTerminationNotificationMessage                                                                                                                                                 | Custom notification                                       | String            |                                                                                                                                                                                                                                                                                |
| enableAppTerminationNotification                                                                                                                                                  | True/False OR 1/0                                         | Boolean OR String | \* **Use .plist** - .plist files contain multiple key value pairs to be uploaded in bulk. Click **Choose File** to upload the .plist file. The validated plist data will be displayed in the **Apple Managed App Settings** table.plists with nested dictionaries are invalid. |

8. Click **Update** to save your entries.

## Configuring Network Relay

To make your app's network traffic more private and secure without connecting to VPN. For more information see, [**Network Relay Configuration**](./Network_Relay_Configuration.md).

1. Click the **Network Relay + icon** to open the configuration page.
2. Enter a name for the **Network Relay** for this app in the Name field.
3. Click + **Add Description** to enter a brief description of the configuration.
4. Click the **Enable Network Relay** for this app option and select an available **Network Relay configuration**.
5. Choose how to **Distribute** this App Config.
6. Click **Next**.

## Configuring Cellular 5G Slicing

Cellular 5G network slicing support allows individual managed apps (for all iOS apps) to be assigned to a network slice which may provide specific network capabilities and characteristics to optimize the app experience. The assignment is done using the new **CellularSliceUUID** app attribute in either the MDM app installation command or declarative app configuration. The string value of the network slice to put into the key needs to be provided by the supporting carrier.

5G network slicing will not be used if either the specific app or the entire device is configured to use a VPN.

ProcedureProcedure

1. Go to **Apps > Apps Catalog > App Configurations >****Cellular 5G Slicing** and click **Add**.
2. Under the **Configuration Setup** section, update the following fields:\* Name
   - Select the **Enable 5G network Slicing** option
   - Choose the **DNN** or **App Category** (as per the network provider)
3. Choose a distribution level for this configuration of the app:
4. Click **Save**.

## Distributing Application using Web Content Filter Configuration

You can use the Web Content Filter configuration to distribute an application instead of a DNS proxy server. After you create the Web Content Filter configuration, you can add the configuration to an application for distribution. For more information about Web Content Filter configuration, see [**Web Content Filter**](./Web_Content_Filter.md).

**Procedure**

1. Go to **Apps** > **App Catalog**.
2. Select an app.
3. Click **Next**.
4. Select the delegation option and click **Next**.
5. Select the distribution options and click **Next**.
6. Select **Web Content Filter configuration** and click the **+** icon.
7. Specify the **Name**.
8. Select the **Enable Web Content Filter for this app** checkbox.
9. Select the Web Content Filter from the drop-down menu.
10. Choose a distribution level for this configuration of the app:1) **To everyone** - The app is added to all the user compatible devices.
    2\) **To no one** - The app is staged for distribution at a later date.
    3\) **Custom Distribution** - Select any of the following options:\* **User/User Groups** - The app is distributed to only the users or user groups you choose.Click the **Users** tab to select the user(s).Click the **User Groups** tab to select the user group(s).
    - **Device/Device Groups** - The app is distributed to only the devices or device groups you choose.Click the **Devices** tab to select the device(s).Click the **Device Groups** tab to select the device group(s).
11. Click **Next**.
12. Click **Done**. The selected app is distributed to the specific users through the Web Content Filter configuration.

## Distributing Application using DNS Proxy

You can use the DNS Proxy configuration to distribute an application. After you create the DNS Proxy configuration, you can add the configuration to an application for distribution. For more information about DNS Proxy Configuration, see [**Creating DNS Proxy Configuration**](./Creating_DNS_Proxy_Configuration.md).

**Procedure**

1. Go to **Apps** > **App Catalog**.
2. Select an app.
3. Click **Next**.
4. Select the delegation option and click **Next**.
5. Select the distribution options and click **Next**.
6. Select **DNS Proxy Configuration** and click the **+** icon.
7. Specify the **Name**.
8. Select the **Enable DNS Proxy for this app** checkbox.
9. Select the DNS proxy from the drop-down menu.
10. Choose a distribution level for this configuration of the app:1) **To everyone** - The app is added to all the user compatible devices.
    2\) **To no one** - The app is staged for distribution at a later date.
    3\) **Custom Distribution** - Select any of the following options:\* **User/User Groups** - The app is distributed to only the users or user groups you choose.Click the **Users** tab to select the user(s).Click the **User Groups** tab to select the user group(s).
    - **Device/Device Groups** - The app is distributed to only the devices or device groups you choose.Click the **Devices** tab to select the device(s).Click the **Device Groups** tab to select the device group(s).
11. Click **Next**.
12. Click **Done**. The selected app is distributed to the specific users through the DNS Proxy configuration.

### Cloning App Configuration Settings

You can clone the Configuration Settings of a Managed app so that the same settings can be applied on other devices. You can even rename and make some changes to the cloned settings.

**Android**

You can clone Configuration Settings on Android devices.

**Procedure**

1. Go to **Apps > App Catalog**.
2. Select an app from which you want to clone the configuration settings.
3. Click **App Configurations**.
4. Under the **App Configurations Summary** section, you will find the list of configurations (**Managed Configurations for Android**, **Install on Device**, **Promotion**, **Delegated Device Permissions**, and **Google Play Release**) available for Android devices.
5. Click on any of the available configurations.
6. Under **Actions**, click **Clone** to begin the cloning process.
7. By default, the cloned configuration name will be \<Copy of the Cloned Configuration name>. However, you can modify the name by entering a name of your choice in the **Name** box.
8. (Optional) Enter some text about the cloned setting in the **Description** box.
9. Click **Continue**.

A confirmation window appears indicating that cloning the app configuration settings is complete. You can view the cloned version under the App Configurations Summary and within the cloned app.

**iOS**

You can clone Managed app Configuration Settings on iOS devices.

**Procedure**

1. Go to **Apps > App Catalog**.
2. Select an app from which you want to clone the configuration settings.
3. Click **App Configurations**.
4. Under the **App Configurations Summary** section, you will find the list of configurations (**Install on Device**, **Apple App Settings**, **Promotion**, **AppConnect Custom Configuration**, **App Tunnel**, **Apple Managed App Configuration**,and **Per App VPN**) available for iOS devices.
5. Click on the required configuration that you want to clone.
6. Under **Actions**, click **Clone** to begin the cloning process.
7. By default, the cloned configuration name will be \<Copy of the Cloned Configuration name>. However, you can modify the name by entering a name of your choice in the **Name** box.
8. (Optional) Enter some text about the cloned setting in the **Description** box.
9. Select a configuration source from the **Source Type** list.
10. Under the **Apple Managed App Settings** section, enter **Key**, **Value**, and select **Type** from the list.For information about the **Key**, **Value**, and **Type**, see **Using Apple Managed App Configuration**.
11. Click **Continue**.A confirmation window appears indicating that cloning the app configuration settings is complete. You can view the cloned version in the **Apple Managed App Configuration** section.

**Windows**

You can clone App Configuration Settings on Windows devices: 

**Procedure**

1. Go to **Apps > App Catalog**.
2. Select an app from which you want to clone the configuration settings.
3. Click **App Configurations**.
4. Under the **App Configurations Summary** section, you will find the **Install on Device** and **Promotion** configurations.
5. Click on the required configuration that you want to clone.
6. Under **Actions**, click **Clone** to begin the cloning process.
7. By default, the cloned configuration name will be \<Copy of the Cloned Configuration name>. However, you can modify the name by entering a name of your choice in the **Name** box.
8. (Optional) Enter some text about the cloned setting in the **Description** box.
9. Click **Continue**.

A confirmation window appears indicating that cloning the app configuration settings is complete. You can view the cloned version under the App Configurations Summary and within the cloned app.

### Choosing Windows 10 apps for your in-house catalog

Choose the apps to add to your in-house app catalog. The in-house, Microsoft Store, and Microsoft for Business apps are supported for Windows 10. Windows 10 enforces compliance directly on the device based on the apps you choose to allow or disallow.

The Windows 10 check-in interval is once every 60 minutes by default. You may want to perform a forced device check-in to get an update of the device and app status.

These actions are supported:

- Uploading new apps
- Silent installation
- Installing manually from Apps\@Work
- Adding a new version of the app
- Deleting an app

These formats are supported:

- APPX
- APPXBUNDLE
- MSI wrapped Win32 - pre-bundled Win32 app
- MSIX (supported on RS5 and above Windows 10 devices)
- .EXE (using bridge)

The **Ivanti Neurons Agent** app is available on the **App Catalog** for **Windows** devices. The admin can deploy the **Ivanti Neurons Agent** app as an in-house app and this app can be distributed accordingly on the Windows devices.

### Configure Windows 10 apps

**Procedure**

1. Click **Devices** on the main navigation bar.
2. Select a Windows 10 device that you have enrolled in Ivanti Neurons for MDM.
3. Click **Apps > App Catalog**.
4. Select an app.
5. Use the **Actions** pulldown menu to add the app or delete the app from your catalog.Optionally add a new version of the app.\* Click the **Actions** pulldown menu.
   - Select **Add New Version**.
   - Go to the catalog and select a new version of the app.
   - Click **Update and Save** to view the App information screen.
6. Use the **Version** pulldown menu to choose which version to use.
7. Click **Edit** to begin making changes to the details.\* Edit the **Category** if needed.
   - Enter a **Description** if needed.
   - Add screenshots if needed.
8. Click **Save**.
9. Click the **Distribution** tab and click **Edit** to begin making changes to the distribution level.
10. Click **Save**.
11. Click the **App Configurations** tab to view a summary of the current configuration.
12. Enter a description of the app if needed.
13. Click **Install on Device** in the App Configurations summary page.Silent installation is the default and cannot be changed.
14. Click **Promotion** in the left navigation pane then click **Promotion distribution configuration settings** to change the promotion level.\* Click **Edit** to make changes to the promotion level settings.
    - Enter a name for the configuration.
    - Enter a description for the configuration.
    - Select a promotion level.
    - Click **Update** to save your changes.
15. Click the **Reviews** tab to view information on reviews.Export the review data to a spreadsheet if needed.

### Editing Windows 10 app configuration settings

**Procedure**

1. Click **Policies > Configuration**.
2. Click **+Add**.
3. Select **Windows App Control** to view the **Create Windows App Control Configuration** screen.
4. Enter a **Name** and **Description** for the configuration.
5. Define the app type as:\* Allowed (Allowlisted) - Only these apps are allowed. These apps are installed silently if not already present on the device.
   - Disallowed (Blockedlisted) - If present on the device,these apps will be blocked if launched.
6. Specify the Rule definitions for the App Type and App Identifier.
7. Click **Lookup Apps** to view the **Search Windows 10 Apps** screen.
8. Enter the name of the app to search the Windows Store.
9. Select the app from the choices displayed to add it to the App Identifier.
10. Optionally use the App Type pulldown menu to set a path define in the App Identifier to allow or disallow apps using the specified path or block all apps installed in that path.App Type **Publisher/PFN Equals** applies to Windows 10+ devices and supports PFN. **EXE/Win32 Equals**.
11. Click **Next**.
12. Select a distribution level.\* **All Devices**.
    - **No Devices**.
    - **Custom** - to enter the users or groups to receive the app.
13. Click **Done**.
14. You can edit the Rule definitions to select an App Type and specify an App Identifier.\* Click the **Actions** pulldown menu.
    - Select **Add New Version**.
    - Select a new version of the app.
    - Click **Update and Save** to view the **App information** screen.

### Configuring Reboot device after install option for Windows

You can configure a device to reboot after an app installation using the **Reboot device after install** option.

**Procedure**

1. Go to **Apps > App Catalog**.
2. Select any Windows-specific app from the list.
3. Go to **App Configurations > Install on device > Install Application configuration setting**.
4. Click **Edit** and set the **Reboot device after install** option to ON.
5. Select one of the following schedule options at which you want to reboot the device:| **Setting**                         | **What To Do**                                                                                                              |
   \| ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
   \| **Right after Installation**        | Select this option to reboot the device soon after you install the application.                                             |
   \| **At specific time during the day** | Select this option to reboot the device at a specific time of the day after you install the application.                    |
   \| **After few mins**                  | Select this option to reboot the device after **15**, **30**, **60**, or **120** minutes after you install the application. |
6. Click **Update**.The device will be rebooted at the scheduled time.

In the case of public apps and Microsoft Store for Business (MSB) apps, you need to set the **Silently install on Windows devices** setting to ON from the **App Configurations** section.

### Installing apps using Apps\@Work

To install an app using Apps\@Work:

1. Click the **Apps\@Work** app.Your administrator email address and server URL are pre-filled in the Apps\@Work login dialog.
2. Enter your password and click Sign In to display the apps page.
3. Select an app to install. You will not be able to install apps with dependencies on prerequisite apps if those prerequisite apps are not already installed on the client.For Apps\@Work for iOS devices, you can optionally click the **Install All** button to install all apps. This option is available in **New Releases**, **Featured Apps** and **Categories** screens.Apps and Books apps will not be installed if the Apps and Books app license is not previously accepted.
4. Click **Update and Save** to view the **App information** screen.

### App Installation and Updates for Android Enterprise Devices

Administrators can publish an app to the catalog for general access and simultaneously deploy it to a specific device for immediate use. This allows users to receive the app directly, while it also stays available in the catalog for others to install as needed.

To install apps and updates

1. Navigate to **Apps> Apps Catalog**.
2. Choose the app you want.
3. Click **Actions** on the **Details** screen. The **Send Install/Updates Request** is displayed.
4. Click Send Install/Updates Request. The **Send Install/Updates Request** dialog box is displayed.
5. Perform the following under **Send Install & update notifications to devices for this application**:\* Select **Send request for new application (applies to devices that don’t yet have the app installed)** checkbox to install the new application.
   - Select **Send request for updates (applies to devices that have the app installed but an update is available)** checkbox to update an installed application.
6. Perform the following under **Select Users to Send Request**:\* Click **Everyone** to distribute the configuration to all compatible users. The app appears in their App Catalog.
   - Click **Custom** to define the user group or user who sees the application in the App Catalog.The **Send Install /Update Request** distribution is part of the app distribution process. The settings you choose on the **Distribution** screen decide which devices will receive the app.

A confirmation window appears indicating that installation of the app is complete.

Changes from new installs or updates are shown in **Dashboard** > **Audit Trails**.

For Public and Private apps **Send request for updates (applies to devices that have the app installed but an update is available)** is disabled. Only **Send request for new application** requests are allowed.

**Related topics:**
