---
title: Android Management API
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Android Management API (AMAPI) is the Cloud Platform API from Google that integrates Google Android UEM functions to Ivanti Neurons for MDM. In the Android Enterprise setup, you can enable the Android Management API framework to manage Android Enterprise devices without the need to have a client app to be installed on the devices for device management. Currently, Go app is not supported to be pushed to the device for other features such as MTD, etc.

When you have an Android Enterprise account configured in your setup, you will be able to enable and use the Android Management API framework. After enabling, you can:

- Add an enrollment profile to use the QR code for device enrollment.
- Create a dedicated devices configuration (corporate-owned single-use, or COSU) for the enrolled device to serve a specific purpose.

Android Management API is currently supported only on devices running on Android version 9 or above that has Google Play installed and provisioned in Dedicated mode. The Corporate Dedicated mode is also referred to as Corporate Owned Single Use (COSU) mode and is a flavor of the device owner mode. This feature also supports the following device actions:

- Lock
- Reboot
- Sync to server
- Wipe

Device check ins are scheduled at regular intervals (hourly). But for immediate action, use the device action 'Sync to server' in the device details page. AMAPI devices do not send mandatory check-ins to Ivanti Neurons for MDM. Inventory updates are performed as and when there is an activity on the device.

## Enabling Android Management API

To enable the Android Management API, go to **Admin > Android Enterprise > Authorize Google (needs a valid Google address) > Android Enterprise Enabled**.

The status of the enabled Android Management API feature (**Yes** for enabled and **No** for disabled) is also shown in the Device details page.

GSuite accounts are currently not supported with COSU.

## Adding an Enrollment Profile

Enrollment profile is required to be created for enrolling Android device using the QR code scan or the alphanumeric string of the token. Enrollment Profiles can only be created when the Android Management API is enabled. You can also create custom device attributes to be associated with the enrollment profile.

::::WorkflowBlock
:::WorkflowBlockItem
Select **Admin > Android Enterprise> Enrollment Profiles**.
:::

:::WorkflowBlockItem
Configure the following settings in the **Enrollment Profile - Corporate Owned Dedicated Device** window.
:::

:::WorkflowBlockItem
| Setting                      | Description                                                                                                                                                                                                                                                                                                                                                |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                     | Enter a name that identifies this enrollment profile.                                                                                                                                                                                                                                                                                                      |
| **Description**              | Enter a description that clarifies the purpose of this enrollment profile.                                                                                                                                                                                                                                                                                 |
| **Username**                 | Enter the first few letters of a valid user name and select the one from the matching results that are displayed.A valid user name could be from a local user or an LDAP user.Enrollment profiles tag the devices enrolled using the QR code in the profile to be displayed as a device belonging to the user for whom the enrollment profile was created. |
| **Token Validity**           | Enter the number of days for the validity of the authentication token QR code scan. The number entered should be between 1 - 30. Device resets if you use the token or enrollment profile post the expiry period.                                                                                                                                          |
| **Custom Device Attributes** | In the Actions column click **+Add New** to add custom device attributes to be associated with the enrollment profile.1) Select the custom device attribute from the drop-down list in the **Attribute name** column.                                                                                                                                      |

2. In the **Value** column, enter the value of the custom attribute.
3. Click **Save**. The added custom device attribute is displayed in the table. To delete, click **Delete** options in the Actions column.The custom attributes can only be added to an enrollment profile during profile creation. The attributes fields cannot be edited after the profile creation. |
   Click **Save**. The **Profile Summary** window shows the following token details:

- Name
- Description
- Username
- Token creation date
- Token expiry date
- Token value
- QR Code
- Custom Device Attributes.
:::
::::

Devices are reset if proper configuration for the device fails to be acquired within the time interval of 10 minutes post registration. In such cases, you should re-register using the enrollment token/QR code

When an enrollment profile is created, it is listed in the **Enrollment Profiles** page. You can perform any of the following actions on the **Actions** column.

- Click on the View icon to view the details of the enrollment profile in the Profile Summary window. The QR code is also displayed in this window.
- Click on the Edit icon to edit the details of the enrollment profile.
- You can edit only the token validity. Other attributes cannot be edited.
  Click the Delete icon to delete the enrollment profile.

## Creating the COSU configuration

Administrators can configure dedicated devices that can be used for a specific purpose using Android enterprise using the Dedicated devices (corporate-owned single-use, or COSU) configuration .The COSU configuration is distributed to Work Managed Devices (Device Owner mode) to provide only one app available to users in Kiosk mode. Devices that are in Work Profile on Company Owned Device are not supported.

Using this configuration, the admin can configure the devices to have the app pinned to the screen so that the Kiosk mode user cannot unpin this app and navigate away from the app to other screens of the device or use any other app on the device.

Other apps can also be force-installed on the AMA device by selecting the "Install on device" option under Advanced Options & App Configuration, but you will not be able to interact with them while the Kiosk app is pinned to the screen via the configuration. For multi-app Kiosk, it is recommended to use the Kiosk functionality of Work Managed Device (device owner mode). This gives more control on apps and device settings and can also be extended to a multi-user mode.

Admins can make configuration changes such as allowing system navigation and the ability to use other apps pushed to the device for the end-user via the Google DPC by reviewing the various options based on the needs.

COSU configurations are determined by the priority assigned to them. The highest priority configuration is used in pushing the policy configuration to Google. COSU configurations are applied to devices within the defined space. It can be delegated to other spaces, if defined in default space.

To configure:

1. Go to **Configuration > +Add**.
2. In the **Lockdown & Kiosk: Android enterprise Configuration**, click **Dedicated devices (corporate-owned single-use, or COSU)**.
3. Enter a name for the configuration.
4. Enter a description.
5. You can configure the following settings by clicking the relevant tabs:\* **App settings**
   - **General lockdowns**
   - **Kiosk customization**
   - **System Settings**The following table provides the details of the configurable fields:| Setting                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
     \| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
     \| **App Setting**                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
     \| **App Name**                    | Select the app to be pinned on the device by typing the name of the app by typing the initial letter of the app name until you see the desired app in the drop-down. If you do not see the desired app in the drop-down, ensure that the app you wish to deploy is a Public/Private app available in the Play Store and is added to the app catalog.This field is mandatory. You will not be allowed to create the configuration if you do not select an app to be added in this field. You can add only public and private apps. In-house apps and Web Apps (Private) cannot be added .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
     \| **General Lockdowns**           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
     \| **Keep Display On**             | Configure the battery plugged in modes for which the device stays on. Select any of the following options :\* **AC** - Power source is an AC charger
   - **Wireless**
   - **USB** - Power source is a USB port
   - **Any** - Power source is from either AC charger or USB port or a wireless charger.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
     \| **Kiosk Customization**         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
     \| **Customize Status Bar**        | Select any of the following options for customizing the status bar on the target devices:\* **Notification and system info enabled** - To show system info and notifications on the status bar.
   - **Only System info enabled**- To show only system info on the status bar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
     \| **Customize System Navigation** | Select any of the following options to specify the access to navigation features (Home, and Overview buttons) in kiosk mode.:\* **Enabled** - Enables Home and Overview buttons navigation. Users can navigate out of the specified app if this option is selected.
   - **Disabled** - Disables Home and Overview buttons navigation.
   - **Home button only** - Enables only the home button navigation.Back button is available with all these options.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
     \| **Enable Global Actions**       | Select to enable global actions in kiosk mode. Restart and shut down functionality associated with the power buttons is controlled via this option.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
     \| **Enable System Error Dialogs** | Select to enable error dialogs for crashed or unresponsive apps in kiosk mode.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
     \| **System Settings**             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
     \| **System Updates Settings**     | Configure the following settings to manage system updates:- **System Update** - Select the type of system update required.
     - **Automatic** - Install automatically as soon as an update is available.
     - **Postpone** - Postpone automatic install up to a maximum of 30 days.
     - **Windowed** - Install automatically within a daily maintenance window. Set the start and the end hours for the maintenance window period.
       The updates installed on devices might vary based on the supported feature set, Android version, and the Google DPC version installed on the device.\* **Freeze Period** - When a device is set within the freeze period, all the incoming system updates are blocked and not installed. Click **Add Freeze Period** to set the **Start Date** and the **End Date** of the freeze period.

:::Paragraph{indent="2"}
When a device is outside the freeze period, normal update behavior is applied. If the end date is before the start date, then the freeze period extends between the current and the successive year.
The freeze period can be set to a maximum of 90 days. Two consecutive freeze periods must be separated by a minimum of 60 days. |
:::

6. Click **Next**.
7. Select one of the following distribution options:\* **All Devices**
   - **No Devices** (default)
   - **Custom**
8. Click **Done**.

### Managing apps on AMAPI devices

When the COSU configuration is distributed to devices, the apps are pushed and pinned to the screen on the AMA device. Irrespective of the COSU configuration being pushed to the device, apps that are installed on the AMA device can still be managed. The following are the details on the app management on these devices:

- Only public, private apps are supported; in-house apps and web-clips are not supported.
- Apps are pushed only if the installation settings have the "Install on Device" or "Silent Install" options are enabled. Apps that are assigned to the user/device without any of these options enabled will not be seen on the device or on the device's Play Store for any user action.
- The supported app configurations are Managed Google Play, and Work Managed Device (Android for Work) Settings. Managed configurations for apps are supported, including support for managed configuration for OEMConfig apps.
  The time for the completion of the installation and un-installation of configurations might vary based on the notifications from Google (messaging service) on whether the desired action is performed.
- The Go app will now be installed by default as part of the AMA device registration. During the registration process, the app will be pinned to the screen and once the setup is complete, will run in the background.
  Policies except for the device registration requirement enforcement based on manufacturer, OS version and security patch level are not supported. Device Allowlisting that allows only the Allowlisted devices to register with Ivanti Neurons for MDM is supported.

### Managing apps feedback support on AMAPI devices

The app feedback support can be managed on AMAPI (COSU) devices. When a device is registered in AMAPI (COSU) mode, the managed app configuration will be pushed to Ivanti Neurons for MDM directly from Google without any intervention from the Go app. The Managed App Feedback information can be viewed at the device level from **Device details > Installed apps > View feedback**, or can be viewed at the individual app level by navigating to the specific Android app in App catalog under the "App Config Feedback" tab for the overall report across all devices. For information on app feedback mechanism, see [**Synchronizing and fetching app feedback**](./Synchronizing_and_fetching_app_feedback.md).

### AMAPI Limitations

Currently, AMAPI has the following limitation:

- Only dedicated devices (COSU mode) are supported.

### Supported Configurations

The following configurations are supported for AMAPI:

- App Distribution (single or multiple apps)
- Managed App Config for apps pushed to the device
- Wi-Fi configuration
- Android Enterprise Lockdown-Dedicated (COSU) configuration
- Always-on VPN Configuration
