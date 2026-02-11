---
title: Mobile@Work for macOS
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Mobile@Work for macOS configuration and scripts execution workflow**](./Mobile@Work_for_macOS.md)
- [**Creating a Mobile@Work for macOS configuration**](./Mobile@Work_for_macOS.md)
- [**Enabling User Onboarding for macOS devices**](./Mobile@Work_for_macOS.md)
- [**Creating a Mobile@Work for macOS Script configuration**](./Mobile@Work_for_macOS.md)
- [**Perform a clean uninstall of Mobile@Work for macOS**](./Mobile@Work_for_macOS.md)

Ivanti Neurons for MDM allows you to create your own macOS shell scripts, which you can then upload to Ivanti Neurons for MDM and run on managed macOS devices. For information about creating, uploading, and managing the scripts repository, see [**All Scripts**](./All_Scripts.md).

A macOS device user can initiate the device to be retired using Mobile\@Work for macOS 1.1 or later. The retire option is available when you click **Uninstall** from the About Mobile\@Work screen. In Ivanti Neurons for MDM, you can verify the status of the device in the **Devices** page and on the device details page.

Mobile\@Work for macOS 1.5 or later opens Apps\@Work immediately after registration without waiting for the MDM registration to complete.

In Mobile\@Work for macOS, click on an application tile to display the App Details page for that application. The page includes app description, screen shots, ratings, and reviews.

Mobile\@Work for macOS notifies the Ivanti Neurons for MDM server if the Packager in-house macOS apps are installed or not installed in the inventory report.

**Prerequisites**

In the [**App Catalog**](./App_Catalog.md), the Mobile\@Work for macOS client is available as a business app. Before you can run shell scripts on macOS devices, instruct the users to register their devices with Ivanti Neurons for MDM using Mobile\@Work for macOS.

**Procedure**

1. Download the Mobile\@Work for macOS application. It is available as a PKG file at [**https://support.mobileiron.com/support/CDL.html**](https://support.mobileiron.com/support/CDL.html). See [**this Ivanti customer forums article**](https://forums.ivanti.com/s/article/MobileIron-Downloads-credential-information) for information on getting credentials for the download site.
2. Upload the PKG file for Mobile\@Work for macOS to a secure server. This server must be accessible to device users.
3. Share the URL of the installation file for Mobile\@Work for macOS with the device users via an e-mail or a message.
4. Instruct the users to:1) Download and install Mobile\@Work for macOS on their device.
   2\) Register the devices with Ivanti Neurons for MDM using Mobile\@Work for macOS.

## Mobile\@Work for macOS configuration and scripts execution workflow

**Procedure**

1. Set up and distribute a Mobile\@Work for macOS configuration.
2. Set up and distribute a Mobile\@Work for macOS Script configuration to upload the script to Ivanti Neurons for MDM. The scripts are encrypted and signed using a signed certificate, which is unique per tenant. The key to decrypt the script is sent to the device along with download URL to the script, which is encrypted and signed.
3. Ivanti Neurons for MDM executes the scripts on macOS devices using Mobile\@Work for macOS. Mobile\@Work for macOS polls Ivanti Neurons for MDM periodically to check whether there are any scripts awaiting execution. If there are scripts in the queue, Mobile\@Work downloads and runs the scripts on macOS devices according to settings you define on Ivanti Neurons for MDM.
4. Mobile\@Work for macOS returns the script execution results to Ivanti Neurons for MDM, which are shown in the device logs. You can check the device logs from the device details page of the macOS device, in the **Logs** tab.

## Creating a Mobile\@Work for macOS configuration

A default system configuration for the Mobile\@Work for macOS configuration is available. However, it is not distributed to any devices by default.

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **work** in the search field, and then click the **Mobile\@Work for macOS** configuration.
4. Name and describe the configuration.
5. Enter **Max Run Time** in seconds to specify how long a script can run. The default value is 60 seconds.
6. Enter **Max Response Size** in kilobytes (KB) to specify the maximum response size limit of the output of the script that is returned to Ivanti Neurons for MDM. This is the stdout or stderr data that is returned when running the script. The default value is 1 KB.
7. Enter **Check-in Frequency** in minutes to specify how often the Mobile\@Work for macOS app must check-in with Ivanti Neurons for MDM. The default value is 15 minutes.
8. (Optional) You can enable user onboarding for macOS devices using the [**Enabling User Onboarding for macOS devices**](./Mobile@Work_for_macOS.md) section.
9. Click **Next** to configure the distribution settings.1) Choose a distribution level:
   2\) **To everyone** - The app is added to all the user compatible devices.
   3\) **To no one** - The app is staged for distribution at a later date.
   4\) **Custom Distribution** - Select any of the following options:\* **User/User Groups** - The app is distributed to only the users or user groups you choose.Click the **Users** tab to select the user(s).Click the **User Groups** tab to select the user group(s).
   - **Device/Device Groups** - The app is distributed to only the devices or device groups you chooseClick the **Devices** tab to select the device(s).Click the **Device Groups** tab to select the device group(s).
10. Click **Done**.

## Enabling User Onboarding for macOS devices

You can enable user onboarding for macOS devices during the automated Device Enrollment process as follows:

- As soon as the Device Enrollment is completed, Mobile\@Work for macOS (version 1.68 or later is required) is pushed to the device along with the profiles, configurations, and apps.
- The Mobile\@Work for macOS client and other apps are pushed to the devices only if:\* The apps are either in-house PKG apps or Apple Apps and Books public apps.
  - The silent installation setting for the apps is set to true. The setting is available from the **Apps** > [**app details**](./App_Configuration.md) > **App Configuration** > **Install on device** page.
  - The [**priority for the apps**](./App_Configuration.md) is set to High. By default, the priority of the Mobile\@Work for macOS client app is set to high (and it cannot be modified), **without which the user onboarding process may fail**.
  - The apps are configured to be distributed to the devices, user groups, or device groups.
- After Mobile\@Work for macOS is installed and registered, the macOS device enters the kiosk mode (user has no control of the device) until the remaining profiles, configurations, and apps are configured and installed. The progress is displayed in steps.

For Mobile\@Work for macOS 1.73 or later versions as supported by Ivanti Neurons for MDM, the following additional features are supported:

- The user onboarding process is completed soon after the Device Enrollment is completed for a device. The user onboarding process does not start after the time window to trigger user onboarding is expired (typically 20 minutes after device registration) even if an administrator enables user onboarding in the Mobile\@Work configuration. This prevents a device from entering the user onboarding kiosk mode when the device is in regular usage.
- The user onboarding process is displayed in steps in the Mobile\@Work for macOS client. Configurations will be installed as part of the first step.
- High-priority apps will be installed initially. Each high-priority app will be counted as one step. Packager apps are not counted as part of the steps.
- Remaining apps will continue to be installed in the background even after user onboarding is complete. Applications are marked as installed after the installation is initialized on a device or after the application is actually installed on the device.
- After user onboarding, you can go to the device details page to verify the configurations and apps pushed to each device. More information is available in the logs.

**Procedure**

1. Create a Mobile\@Work for macOS configuration using [**Creating a Mobile@Work for macOS configuration**](./Mobile@Work_for_macOS.md).
2. Select the **Enable User Onboarding** option.
3. Enter the following details:\* **User Onboarding Timeout Value** - Enter the approximate time that the device will take to install the app and configurations during the initial device setup. By default, the user onboarding process on a macOS device times out in 120 seconds, which you can modify as required.
   - **User Landing Page URL&#x20;**- Provide a landing page URL to be displayed to the user after onboarding is completed.
4. Click **Next** to configure the distribution settings.
5. Click **Done**.

## Creating a Mobile\@Work for macOS Script configuration

You can create and distribute multiple Mobile\@Work for macOS Script configurations to the devices. Using this configuration, you can select a script from the repository (**Admin >&#x20;**[**All Scripts**](./All_Scripts.md)) to distribute to Mobile\@Work for macOS.

You can schedule script executions on devices with Mobile\@Work for macOS 1.66 or later versions. If you schedule a script execution to run on devices with Mobile\@Work for macOS client versions earlier than 1.66, then the script is executed only once. If the Mobile\@Work for macOS client is upgraded from 1.4 to 1.66, then all the macOS client configurations will be redistributed to the devices.

**Prerequisites**

- Go to **Admin >&#x20;**[**All Scripts**](./All_Scripts.md) to upload and manage scripts that can be used in this configuration and distributed to devices.
- Configure and distribute the Mobile\@Work for macOS configuration on devices. Otherwise, the Mobile\@Work for macOS Script configuration will be in the Error state.

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **work** in the search field, and then click the **Mobile\@Work for macOS Script** configuration.
4. Name and describe the configuration.
5. In the **Select Script** field, enter the name of the script to find and select the script from the drop-down list.
6. In the Script Input section, the script input labels and script variables associated with the script are displayed. If you need to override them, enter alternate script variables (for example, \{$userWorkEmailAddress}) and their alternate default values (for example, [**john.doe@company.com**](mailto\:john.doe@company.com)).
7. In the Script Execution section, select one of the following scheduling options:\* Execute Once On Deployment
   - Recurring Execution
8. If you choose Recurring Execution, specify the following details:\* Timezone to use - Select Device's Local Time or UTC Time. The script will be executed at the time selected in this field.
   - Execution Starts on - Select the start date.
   - Execution Ends on - Select the end date (greater than or equal to the start date).
   - Execute Script - Select Daily or Weekly and enter the hours (in 24 hours format), minutes, and days as applicable.
9. Click **Next** to configure the distribution settings.
10. Click **Done**.

## Perform a clean uninstall of Mobile\@Work for macOS

If you have enabled the option **Remove apps on un-enrollment**&#xNAN;**(Applicable to managed apps only)** during installation of Mobile\@Work for macOS and if you initiate the device to be retired from the Ivanti Neurons for MDM administrator portal, then the Mobile\@Work for macOS application and the uninstall script is just deleted from the device. To avoid the processes and scripts from running in the back end, ensure that during device registration of new users or retirement of existing users, you deselect the following option from the Ivanti Neurons for MDM administrator portal to ensure that the uninstall script runs and deletes the associated processes and scripts from the back end.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrator portal.
2. Go to **Apps** > **Mobile\@Work** > **App Configurations** > **App Configurations Summary list** > **Apple App Settings** > **Apple Application Management configuration settings**.
3. From the **Configuration Setup** page deselect the following option:\* **Remove apps on un-enrollment (Applicable to managed apps only)**.

**Related topics:**

- [**Admin > All Scripts**](./All_Scripts.md)
