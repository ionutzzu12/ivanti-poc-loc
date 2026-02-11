---
title: Managed Configurations for Android
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Using Android Enterprise Managed Configurations**](./Managed_Configurations_for_Android.md)
- [**App Restrictions and Permissions for in-house apps**](./Managed_Configurations_for_Android.md)
- [**Setting up Gmail with Android Enterprise**](./Managed_Configurations_for_Android.md)

If Ivanti Neurons for MDM is Android Enterprise enabled, then the Android Enterprise configuration is available to use per app.

## Using Android Enterprise Managed Configurations

::::WorkflowBlock
:::WorkflowBlockItem
Click **Apps**.
:::

:::WorkflowBlockItem
Click **App Catalog**.
:::

:::WorkflowBlockItem
Select an app for which to configure the Android Enterprise configuration.
:::

:::WorkflowBlockItem
Click **App Configurations**.
:::

:::WorkflowBlockItem
Click **Managed Configurations for Android**.
:::

:::WorkflowBlockItem
Provide a name for the configuration.
:::

:::WorkflowBlockItem
Optionally, provide a description.
:::

:::WorkflowBlockItem
Use the Managed Configurations fields to configure managed configurations behaviors:
:::

:::WorkflowBlockItem
| **Setting**                                      | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Blocks apps from sharing widgets across profiles | Enable to block apps from sharing widgets across profiles only if the app is not silently installed. Leave disabled to allow trusted apps deployed in the Android Enterprise profile to display widgets on the home screen so users can access information without having to log in.                                                                                                                                                                                                           |
| Blocks the user from uninstalling the app        | Enable to block the user from uninstalling the app after Ivanti Neurons for MDM silently installs the app.                                                                                                                                                                                                                                                                                                                                                                                     |
| Minimum version code                             | Set a minimum version code required for the app to override the default update behavior. If the version code of the app currently installed on the device is less than the specified minimum version code then the app is updated immediately to the latest version.                                                                                                                                                                                                                           |
| Auto-launch on install                           | Select this option if you want to launch an app automatically after installation. This functionality is available only if the app is newly installed on the device and not for a version update. In the case of Work Profile and Work Profile on Company-Owned devices, Go app should be active and in the foreground.Due to limitations on Android 10+, only one app will auto-launch if the user pushes multiple apps in the case of Work Profile and Work Profile on Company-Owned devices. |

### Managed Configurations

The administrator can control the app configuration fields which can be sent to devices or which should not be sent. In general, the default values are set when pushing the configurations to different devices. Under the Managed Configurations section, within **Push to device** setting, select **Push all settings** or **Only push settings with values defined**.

Each Android Enterprise app configuration displays Certificate-enable button for each text field and when clicked, the text field is replaced by a drop-down list of certificates. When configured, these certificates are silently applied without any user interaction.An existing certificate-enabled field can be changed to text-enabled by clicking the same button next to the field. A text-enabled field changed to certificate-enabled field can be changed back to text-enabled field by clicking on the same button. (Default drop-down fields cannot be changed back to text-enabled fields).

If there are no ID certificates configured in the tenant and when switched from text to drop-down using the Certificate-enable button, only 'None' option is shown in the drop-down list.

Click **Manage Permissions** to select and configure runtime permissions for applications targeting API 23 or higher and Android 6.0+.Only the dangerous permissions that are applicable to the specific application are listed for selection. The complete list of dangerous permissions (such as read your contacts, find accounts on the device, write call log, and so on) are listed at [**https://developer.android.com/guide/topics/permissions/requesting.html#perm-groups.**](https://developer.android.com/guide/topics/permissions/requesting.html#perm-groups)
:::

:::WorkflowBlockItem
- The permissions are applied only when the application requests permissions.
- The permissions are not applied if the users have previously accepted or denied permissions.
  The rights you can assign to each permission include:
- Auto grant
- Auto deny. Use this setting with caution.
- Default/Global
  Configure the distribution options, selecting from **Everyone with App**, **No One**, or **Custom**.
:::

:::WorkflowBlockItem
Click **Save**.
:::
::::

### New Configuration Settings

When an app version is updated and if there are any changes to existing configurations, the **Update to Latest Features** button appears after editing the Configuration Details page.

1. Click **Update to Latest Features**.A warning message appears on the screen indicating that moving to the latest features will prevent users from accessing the older versions of the application. The warning message recommends steps to integrate the latest version of the application seamlessly.
2. Click **Next**.
3. The **New Configurations Settings** window appears on the screen.
4. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/6S6Z98e3O3q9o_oVNEhdZ_newconfigurationsettings.png" alt caption}
   The **New Configuration Settings** window lists different settings that were existing with the configuration, and the status of each setting after the update. The New Configuration Settings window lists all the restrictions from the database, and the Google schema will list the following status:
   •Added
   •Removed
   •Modified
   Select the check box and click **Accept** to proceed with the update.
   A confirmation message appears on the screen that the configuration has been updated successfully with the latest features. You can now distribute and save the configurations for changes to take effect.

## App Restrictions and Permissions for in-house apps

The administrator can set some app restrictions and restrict or grant permissions for In-house apps. This functionality was available only for Public apps. But this functionality has been extended to the In-house apps now.

The administrator must re-upload the In-house apps to have the **App Restrictions** and **Permissions** features available on their apps. It is recommended to delete the existing app before uploading a new version.

**Procedure**

1. Go to **Apps** > **App Catalog**.
2. Select an **In-house** app from the list.
3. Click **App Configurations**.
4. Click **Manged Configurations for Android**.
5. Click **Add**.
6. The **App Restrictions** section appears on the screen.
   Enter the required values for the available restrictions.
7. Select **Manage Permissions**.
8. The **Select Permissions** window appears on the screen.
   Select the required permissions from the list and then click **Select**.
9. Under the **Runtime Permissions** section, set the values for the selected permissions.
10. Under the **Distribute this App Config** section, choose one of the following **App Distribution** options:\* **Everyone with App**
    - **No One**
    - **Custom**
11. Click **Save**.
    The selected restrictions and permissions will be applied on the In-house apps.

## Setting up Gmail with Android Enterprise

You can deploy Gmail to Android Enterprise devices if you have set up Ivanti Neurons for MDM for Android Enterprise. To setup Gmail with Android Enterprise

1. Go to **Apps > App Catalog**.
2. Select Gmail app for which to configure the Android Enterprise configuration. The Configuration Setup section is displayed.
3. Provide a name for the configuration.
4. Optionally, provide a description.
5. Use the **Managed Configurations** fields to configure managed configurations behaviors:

The **Expand all** and **Collapse all** options are available for nested or hierarchical restrictions only.

| Setting                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Push to device**           | Push all settings - Select this option to enable all toggles, including those with no valuesOnly push settings with values defined - Select this option to enable all toggles with defined values and disable the toggles for settings without valuesIn many cases, the default settings are already available. However, the admin can select the required app config settings or edit the variables that must be sent to the devices. |
| **Email address**            | Enter substitution variables to define the email address. Typically, you enter $emailaddress$. UEMs can use this field to pull user credentials from Active Directory.                                                                                                                                                                                                                                                                 |
| **Hostname or host**         | Enter the host name for the Active Sync server, such as hostname.company.com:443/path.                                                                                                                                                                                                                                                                                                                                                 |
| **Username**                 | Use the variable for the user's Active Directory username that can be specified as a direct username (janedoe) or templated value ($username$).                                                                                                                                                                                                                                                                                        |
| **Authentication types**     | Select the list of strings containing the permitted authentications types.                                                                                                                                                                                                                                                                                                                                                             |
| **SSL required**             | When selected, enables and requires SSL on port numbers used with hostname.                                                                                                                                                                                                                                                                                                                                                            |
| **Trust All certificates**   | Select only if you want the app to automatically accept untrusted certificates. Use this option only for debugging or development when working in a test environment.                                                                                                                                                                                                                                                                  |
| **Login certificate alias**  | Enter the alias for the login certificate used for authenticating to the ActiveSync servers.                                                                                                                                                                                                                                                                                                                                           |
| **Allow unmanaged accounts** | Select this option to allow users to add or remove any Exchange account other than the account specified in this managed configuration.                                                                                                                                                                                                                                                                                                |
| **Default email signature**  | Enter the string comprising the default email signature to be appended to the bottom of all outbound email message text.                                                                                                                                                                                                                                                                                                               |
| **Default sync window**      | Enter the value from 0-5 that represents the time window for syncing with EAS (Exchange Active Sync).                                                                                                                                                                                                                                                                                                                                  |
| Click **Next**.              |                                                                                                                                                                                                                                                                                                                                                                                                                                        |

7. Configure the distribution options, selecting from **Everyone with App**, **No One**, or **Custom**.
8. Click **Save**.
