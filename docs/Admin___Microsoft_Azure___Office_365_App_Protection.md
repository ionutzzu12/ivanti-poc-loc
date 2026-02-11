---
title: Admin > Microsoft Azure > Office 365 App Protection
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

**License: Gold**

You can set up Office 365 App Protection policies to help protect your company's data. The policies enforce Data Loss Prevention (DLP) controls for Microsoft Office 365 apps using Microsoft Graph APIs. Some of these Graph APIs allow administrators to enforce app protection for native iOS and Android apps that leverage the Graph SDK.

Use this feature to enforce policies such as:

- Prevent users printing from Office 365 apps.
- Preventing outbound data sharing from Office 365 apps.
- Enforce PIN for Office 365 apps.
- Disable Contacts sync from Office 365 apps.

## Prerequisites for using Office 365 App Protection

Before you can use Office 365 App Protection, you must have:

- A valid MobileIron license.
- Office 365 App Protection Feature enabled in Ivanti Neurons for MDM
- Intune subscription or an Microsoft EMS subscription that includes Intune.\* Each use to which the policy is applied to requires a license, however to enable and test the integration requires only a single license.
- A valid Office Enterprise or Business subscription with access to Office 365 apps on a mobile device.
- One or more Office 365 apps.
- Synced your Active Directory users to your Entra ID.
- One Drive for Business installed on devices to protect data on Word, Excel, and PowerPoint. This is not mandatory.
- Access to Microsoft Azure portal ([**https://portal.azure.com/**](https://portal.azure.com/)) to configure intune app protection policies.
- Intune Company Portal app installed on Android devices.Device users are not required to sign in, but this app must be installed on the device to protect data on device. Protection will be applicable when the user signs in to the app.

## Registering MobileIron as an Azure app

This topic describes how to register and store your Azure tenant credentials with Ivanti Neurons for MDM software and to remotely manage app protection policies in the Microsoft Azure cloud for Android and iOS Office 365 apps. Though not necessary, you may open two browsers to perform the steps in the following procedures. Use the first browser to log into the Microsoft Azure portal. Use the second browser to log into the Ivanti Neurons for MDM Admin portal.

### Procedure for Microsoft Azure Portal

Microsoft may change the Azure portal user interface from time to time. These instructions assume that you are familiar with the Microsoft Azure Portal and can make necessary adjustments as you register MobileIron as an Azure app.

::::WorkflowBlock
:::WorkflowBlockItem
Open the first browser and log into the Microsoft Azure portal ([**https://portal.azure.com/**](https://portal.azure.com/)).
:::

:::WorkflowBlockItem
Click **App registrations** on the left pane.
:::

:::WorkflowBlockItem
Click **+New application registration**.
:::

:::WorkflowBlockItem
Enter the following information to register MobileIron as an Azure app.
:::

:::WorkflowBlockItem
- **Name:** Enter a name for the MobileIron app. (This field is required with a minimum of 4 characters.)
- **Application Type:** Select Web app / API.
- **Sign-on URL:** Enter the URL device users access to sign into MobileIron (required).
  Click **Create** on the bottom of the pane to add the app and return to the Azure home page.
:::

:::WorkflowBlockItem
Click the newly created MobileIron app in the Azure home page.
:::

:::WorkflowBlockItem
Return to the Azure home page to assign permissions to the MobileIron Azure app.
:::

:::WorkflowBlockItem
To set required API permissions for the newly created MobileIron app, click the app name under App Registrations.
:::

:::WorkflowBlockItem
Click **API permissions** > **Add a permission**.
:::

:::WorkflowBlockItem
In the **Microsoft Graph > Delegated Permissions > Device Management Apps** section, select the **DeviceManagementApps.Read.All** permission and click **Save**. By default, the user.Read permission is enabled for the app.
:::

:::WorkflowBlockItem
To grant access, click **Grant admin consent for MobileIron**.
:::

:::WorkflowBlockItem
Perform the following procedure for Ivanti Neurons for MDM admin portal.
:::
::::

### Procedure for Ivanti Neurons for MDM Admin Portal

::::WorkflowBlock
:::WorkflowBlockItem
Open the second browser and log into the Ivanti Neurons for MDM admin portal.
:::

:::WorkflowBlockItem
Go to **Admin > Microsoft Azure > Office 365 App Protection**.
:::

:::WorkflowBlockItem
Paste **Application ID** in the Ivanti Neurons for MDM admin portal.
:::

:::WorkflowBlockItem
**Procedure**

1. Go to the Azure portal.
2. Select the MobileIron app > **Properties**.
3. Copy the **Application ID**.
4. Return to **Admin > Microsoft Azure > Office 365 App Protection** on the Admin Portal.
5. Paste it into the **Application ID** field.
   Paste the **Application Secret** (Client Secret) in the Ivanti Neurons for MDM admin portal.
:::

:::WorkflowBlockItem
**Procedure**

1. Go to the Azure portal.
2. Select the MobileIron app.
3. Click **Keys** and enter a name in **Key description** and select an expiration time-period in **Duration**.
4. Click **Save** and copy the **Key** value.
5. Return to **Admin > Microsoft Azure > Office 365 App Protection** on the Admin Portal.
6. Paste it into the **Application Secret** (Client Secret) field.
   Paste the **Tenant ID** in the Ivanti Neurons for MDM admin portal.
:::

:::WorkflowBlockItem
**Procedure**

1. Go to the Azure portal.
2. Click Entra ID in the left pane then click Properties.
3. Copy the Directory ID.
4. Return to **Admin > Microsoft Azure > Office 365 App Protection** on the Admin Portal.
5. Paste it into the **Tenant ID** field.
   Enter your Intune admin **Username** and **Password**.
:::

:::WorkflowBlockItem
- The Azure account should have either global admin rights or limited admin + Intune service administration rights.
- Ivanti recommends creating a local Azure account with just the Intune service administration rights. User accounts that are federated to an identity provider are not supported by Microsoft for authentication with the Graph API's.
  Click **Authenticate and Save**.

If the date submitted is incorrect, an error message is displayed.
:::
::::

## Policies for Office 365 App Protection

After configuring Microsoft Graph credentials, go to **Apps > Office 365 App Protection** to add new Office 365 App Protection policies for iOS or Android devices for different user groups.

The policies are listed on the **Apps > Office 365 App Protection** page, under the **App Policies** tab. This list of policies provides tabular details such as the updated time stamp, platform, apps assigned, and user groups deployed.

### Adding an Office 365 App Protection policy for iOS devices

Procedure

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Apps > Office 365 App Protection**.
:::

:::WorkflowBlockItem
Click **App Policies > + Add**.
:::

:::WorkflowBlockItem
Enter a **Name** and an optional **Description** for the policy.
:::

:::WorkflowBlockItem
Under Choose OS, click **iOS**.
:::

:::WorkflowBlockItem
Under **Data Relocation**, select from the following settings and options:\* Prevent iTunes and iCloud backups

- Allow app to transfer data to other apps - All apps (default), Policy managed apps, None
- Allow app to receive data from other apps - All apps (default), Policy managed apps, None
- Prevent "Save As"
- Restrict cut, copy and paste with other apps - Any app (default), Blocked, Policy managed apps, Policy managed with paste in
- Restrict web content to display in the Managed Browser
- Encrypt app data - When device is locked (default), When device is locked and there are open files, After device restart, Use device settings
- Disable contact sync
- Disable printing
:::

:::WorkflowBlockItem
Under **Access**, select from the following settings and options:
:::

:::WorkflowBlockItem
- Require PIN for access
- Number of attempts before PIN resets (default 5)
- Allow simple PIN
- PIN length (default 4)
- Allow Fingerprint instead of PIN (iOS 8+)
- Disable app PIN when device PIN is managed
- Require corporate credentials for access
- Block managed apps from running on jailbroken or rooted devices
- Recheck access requirements after (Minutes)
  - Timeout - Must be a value between 1 and 65535 (default 30)
  - Offline - grace period Must be a value between 1 and 65535 (default 720)
  - Offline interval (days) before app data is wiped - Must be a value between 1 and 65535 (default 90)
    Require minimum iOS operating system
- Require minimum iOS operating system (Warning only)
- Require minimum app version
- Require minimum app version (Warning only)
- Require minimum Intune app protection policy SDK version
  Click **Next**.
:::

:::WorkflowBlockItem
Select and assign apps that this policy will apply to.
:::

:::WorkflowBlockItem
Click **Next**.
:::

:::WorkflowBlockItem
Select user groups that this policy will apply to.
:::

:::WorkflowBlockItem
Click **Done**.
:::
::::

### Adding an Office 365 App Protection policy for Android devices

**Procedure**

1. Go to **Apps > Office 365 App Protection**.
2. Click **App Policies > + Add**.
3. Enter a **Name** and an optional **Description** for the policy.
4. Under Choose OS, click **Android**.
5. Under **Data Relocation**, select from the following settings and options:\* Prevent Android backups
   - Allow app to transfer data to other apps - All apps (default), Policy managed apps, None
   - Allow app to receive data from other apps - All apps (default), Policy managed apps, None
   - Prevent "Save As"
   - Restrict cut, copy and paste with other apps - Any app (default), Blocked, Policy managed apps, Policy managed with paste in
   - Restrict web content to display in the Managed Browser
   - Encrypt app data
   - Disable app encryption when device encryption is enabled
   - Disable contact sync
   - Disable printing
6. Under **Access**, select from the following settings and options:\* Require PIN for access
   - Number of attempts before PIN resets (default 5)
   - Allow simple PIN
   - PIN length (default 4)
   - Allow Fingerprint instead of PIN (Android 6+)
   - Disable app PIN when device PIN is managed
   - Require corporate credentials for access
   - Block managed apps from running on jailbroken or rooted devices
   - Recheck access requirements after (Minutes)\* Timeout - Must be a value between 1 and 65535 (default 30)
     - Offline - grace period Must be a value between 1 and 65535 (default 720)
     - Offline interval (days) before app data is wiped - Must be a value between 1 and 65535 (default 90)
   - Block screen capture and Android assistant
   - Require minimum Android operating system
   - Require minimum Android operating system (Warning only)
   - Require minimum app version
   - Require minimum app version (Warning only)
   - Require minimum Intune app protection policy SDK version
7. Click **Next**.
8. Select the apps that this policy will apply to.
9. Click **Next**.
10. Select the user groups that this policy will apply to.
11. Click **Done**.

### Modifying an Office 365 App Protection policy

Procedure

1. Go to **Apps > Office 365 App Protection**.
2. Click **App Policies**.
3. Click the name of the policy you want to modify.
4. On the policy details page, click **Edit**.
5. Modify the policy configuration settings.
6. Click **Next**.
7. Modify the list of apps that this policy will apply to.
8. Click **Next**.
9. Modify the user groups that this policy will apply to.
10. Click **Done**.

### Deleting an Office 365 App Protection policy

Procedure

1. Go to **Apps > Office 365 App Protection**.
2. Click **App Policies**.
3. Under the **Actions** column, click the remove icon against the policy name you want to delete.
4. Click **Yes** to confirm.

## Office 365 App Configurations

Go to the **Apps > Office 365 App Protection** page, under the **App Configuration** tab to add, modify, or delete Office 365 App Configurations for different user groups. In these app configurations, administrators can add a list of key-value pairs. and assign the configurations to one or more Office 365 apps. The App Configuration tab lists configurations with tabular details such as the updated time stamp, apps assigned, and deployment status.

### Adding an Office 365 App Configuration

Procedure

1. Go to **Apps > Office 365 App Protection**.
2. Click **App Configuration > + Add**.
3. Enter a **Name** and an optional **Description** for the configuration.
4. Enter the key-value pairs.
5. Click **Next**.
6. Select the apps that this configuration will apply to.
7. Click **Next**.
8. Select the user groups that this configuration will apply to.
9. Click **Done**.

### Modifying an Office 365 App Configuration

Procedure

1. Go to **Apps > Office 365 App Protection**.
2. Click **App Configuration**.
3. Click the name of the configuration you want to modify.
4. On the configuration details page, click **Edit.**
5. Alternatively, click either **App Distribution** or **User Group Distribution** tabs. Click **Edit** to modify only those settings and click **Save**.
6. Modify the configuration settings.
7. Click **Next**.
8. Modify the list of apps that this configuration will apply to.
9. Click **Next**.
10. Modify the user groups that this configuration will apply to.
11. Click **Done**.

### Deleting an Office 365 App Configuration

Procedure

1. Go to **Apps > Office 365 App Protection**.
2. Click **App Configuration**.
3. Under the **Actions** column, click the remove icon against the configuration name you want to delete.
4. Click **Yes** to confirm.

## Out of compliance users with Office 365 apps

Administrators can review the list of users and their devices due to non-compliance. Use this page to wipe any Office 365 apps on such flagged devices.

### Wiping Office 365 apps

Procedure

1. Go to **Apps > Office 365 App Protection**.
2. Click **Out of Compliance Users**.
3. Perform one of the following actions:\* Select the users from the list and click **Wipe Office 365 Apps**.
   - Click the name of the user to display the list of devices that have out of compliance apps. Under the **Action** column, click **Wipe Office 365 Apps** icon against a specific device.
   - Click the name of the user to display the list of devices that have out of compliance apps. Click the name of a specific device to view the apps listed with bundle IDs / package names and the flagged reasons. Click **Wipe Office 365 Apps**.
4. Click **Yes** to confirm the action.

Alternatively, perform the following steps:

1. Go to **Users**.
2. Click the name of the user to display the user details page.
3. Click **Action >&#x20;****Wipe Office 365 Apps**.
4. Select the devices from which the Office 365 apps need to be wiped.
5. Click **OK** to confirm the action.

### Canceling wipe requests of Office 365 apps

Procedure

1. Go to **Users**.
2. Click the name of the user to display the user details page.
3. Click the **Office 365 Protection** tab.
4. From the **Select Report Type** drop-down box, select the **Wipe Requests** report to display the corresponding information.
5. Select the devices from which the wipe requests need to be canceled. Only devices with the Wipe Pending status can be selected.
6. Click **Cancel Wipe**.
7. Click **OK** to confirm the action.

## App reports for users with Office 365 App Protection

Administrators can select one of the following reports to review the list of users with Office 365 App Protection and related information:

- App Policy Report
- App Configuration Report
- Wipe Requests

Information in the App Reports includes Bundle ID / Package Name, Device Name, Device Type, Policies or Configurations (deployed to the device), Status (Synced, Synced but out of date, or Not Synced), and the time of Last Check-in. Information from the App Reports can be exported to a CSV file for later reference or analysis.

Information in the Wipe Requests report includes Display Name, User Name, Device Name, Device Type, and Wipe Status (Wipe Pending or Wipe Complete).

Perform the following steps to view one of the reports:

1. Go to **Users**.
2. Click the name of the user to display the user details page.
3. Click the **Office 365 Protection** tab.
4. From the **Select Report Type** drop-down box, select one of the reports to display the corresponding information.
5. (Optional) From the Wipe Requests report page, select the devices from which the wipe requests need to be canceled and click **Cancel Wipe**. Only devices with the Wipe Pending status can be selected.
6. (Optional) Click **Export to CSV** to download the report contents in a CSV file for later reference or analysis.
