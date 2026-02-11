---
title: Monitoring and Controlling Allowed Apps
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

**License:** Silver

To control which apps are installed on devices, you create an Allowed Apps policy. This policy also supports MobileIron Packager (MIP) in-house macOS apps. The policy contains the following information:

- Allowlist apps
- Blockedlist apps
- required apps
- compliance actions

If an app is both required and Blockedlisted, then the evaluation of the app against the required list takes precedence. For example, if an app A1 is present in both in the required list and the Blockedlist, then the apps policy evaluation for this device behaves as follows:

- Device will be compliant if A1 is installed on the device.
- Device will be non-compliant if A1 is not installed on the device.

## Supported Devices

- Android 4.2 or supported newer versions
- iOS 8.0  or supported newer versions
- macOS 10.12 or supported newer versions
- Windows 10 or supported newer versions

**Prerequisites**

- The [**privacy configuration**](./Privacy_Configuration.md) assigned to a device must allow collection of app information in order for an Allowed Apps policy to work correctly. Check the privacy configurations assigned to the devices to which you will apply the Allowed Apps policy.

If you are not sure which configurations are affected:

1. Go to **Policies**.

::Image[]{src="r44allowedapps001.png" signedSrc="r44allowedapps001.png" size="36" caption alt isUploading="false" sha initialPath="r44allowedapps001.png" githubPath="r44allowedapps001.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
Click **Allowed Apps**.
:::

::Image[]{src="allowed_app_privacy001.png" signedSrc="allowed_app_privacy001.png" size="37" caption alt isUploading="false" sha initialPath="allowed_app_privacy001.png" githubPath="allowed_app_privacy001.png" position="flex-start" indent="2"}

3. Under **Privacy Configurations**, note the configurations that need to be edited.
4. Go to **Configurations**.
5. For each privacy configuration you noted:1) Select the configuration.
   2\) Click **Edit**.
   3\) Under **Collect App Inventory,** select **For All Apps on the Device**.
   4\) Click **Done**.

## Creating an Allowed Apps policy

**Prerequisites**

- Enable Android Enterprise to access Google Play Store and to add new applications to allowed apps policy.

Procedure

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Policies** and click **+ Add**.

::Image[]{src="r44allowedapps001.png" signedSrc="r44allowedapps001.png" size="36" caption alt isUploading="false" sha initialPath="r44allowedapps001.png" githubPath="r44allowedapps001.png" position="flex-start"}
:::

:::WorkflowBlockItem
Click **Allowed Apps**.

::Image[]{src="r44allowedapps001a.png" signedSrc="r44allowedapps001a.png" size="46" caption alt isUploading="false" sha initialPath="r44allowedapps001a.png" githubPath="r44allowedapps001a.png" position="flex-start"}
:::

:::WorkflowBlockItem
In the **Name** field, type a name for this policy.
:::

:::WorkflowBlockItem
In the **Description** field, type optional text that explains the purpose of the policy.
:::

:::WorkflowBlockItem
Choose the apps to Allowlist or Blockedlist by clicking one or both of the following tabs:

- Click Add by Lookup to search for and choose apps from the App Store or App Catalog.Ensure to enable Android Enterprise to access Google Play Store.

::Image[]{src="Resources/Images/AllowedApps_EnablingAndroidEnterprise.png" signedSrc="Resources/Images/AllowedApps_EnablingAndroidEnterprise.png" size="29" caption alt isUploading="false" sha initialPath="Resources/Images/AllowedApps_EnablingAndroidEnterprise.png" githubPath="Resources/Images/AllowedApps_EnablingAndroidEnterprise.png" position="flex-start" indent="2"}

- Click **Add Manually** to choose apps by entering the bundle ID for Android, Windows, iOS or macOS system apps.
  Select the **Add App Lists** tab and then select the desired required apps lists.
:::

:::WorkflowBlockItem
Use the resultant fields to select the required apps or apps lists.
:::

:::WorkflowBlockItem
Click the **View Required List** tab for a list of apps you have selected so far.

Click **Next**
:::

:::WorkflowBlockItem
:inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/FE-hnabSQMF6rqr_nozZ4_r44allowedapps003a.png" alt caption}
Select whether to create a Allowlist or a Blockedlist.
:::

:::WorkflowBlockItem
You cannot have both a Allowlist and a Blockedlist for a device simultaneously. Creating a Allowlist means all other apps are Blockedlisted.

Use the **Allowlist/Blockedlist Apps and App Lists** section to select apps and apps lists.
:::

:::WorkflowBlockItem
- Select the **Add App Lists** tab and then select the desired apps lists.
  Use the resultant fields to select the required apps or apps lists.
:::

:::WorkflowBlockItem
Click the **View Allowlist or Blockedlist** tab for a list of apps you have selected so far.

Click **Next**.
:::

:::WorkflowBlockItem
Select the actions to take when a device is out of compliance:
:::

:::WorkflowBlockItem
| Action                | What To Do                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Monitor**           | Currently always selected. Sentry version 9.0.0 or later is required to utilize the tiered compliance actions.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Do Nothing            | Select to take no action if the device is out of compliance.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Send Notification** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Send Email            | Select to send an email to the device user's email address notifying them the device is out of compliance.\* Turn on the **Use the Compliance Policy Email Template** option to insert the message you configure here into the policy notification email template you configure as described in [**Customizing an email template**](./Branding_Email_Templates.md) in [**Branding Email Templates**](./Branding_Email_Templates.md). See [**Configuring and using policy compliance notification emails**](./Configuring_policy_compliance_notification_emails.md) for an overview. |

::Image[]{src="Resources/Images/68CustomeComplianceTemplate.png" signedSrc="Resources/Images/68CustomeComplianceTemplate.png" size="37" caption alt isUploading="false" sha initialPath="Resources/Images/68CustomeComplianceTemplate.png" githubPath="Resources/Images/68CustomeComplianceTemplate.png" position="flex-start"}

- You can customize the messages by including optional substitution variables to provide recipients more details about policy violations and other relevant information. This provides users of non-compliant devices with relevant information about the policy violation so they can take remedial actions. Click the following attribute types to display the complete list of variables:\* Policy Attributes including $\{BlockedlistAppsInViolation}, $\{requiredAppsInViolation}, and $\{AllowlistAppsInViolation}.
  - User Attributes including $\{sAMAccountName}, $\{userCN}, and $\{userEmailAddressDomain}.
  - Device Attributes including $\{deviceClientDeviceIdentifier}, $\{deviceIMEI}, and $\{deviceModel}. |
    \| Send Push Notification                                             | Select to send a push notification to the device that the device is out of compliance.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
    \| Send Both                                                          | Select to send both a push notification to the device and an email to the device user's email address notifying them the device is out of compliance. You can customize the messages by including optional substitution variables to provide recipients more details as described previously for the Send Email action.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
    \| **Wait**                                                           | Select to delay action for a specified time period to allow users to remediate the violation before additional actions are taken if the device remains in a non-compliant state.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    \| **Block**                                                          | Uses Sentry to block managed devices from accessing email and AppConnect-enabled applications.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
    \| **Quarantine**                                                     | Select to remove access to apps, content, and servers as per the actions in the following table. Remove all apps action is not allowed.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
    \| **Send a notification when the device comes back into compliance** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
    \| Send Email                                                         | Sends an email to the device user's email address notifying them when the device comes back into compliance.\* You can use the policy notification email template as described above.
- You can customize the messages by including optional substitution variables to provide recipients more details about policy violations and other relevant information. Click the following attribute types to display the complete list of variables:
  - Policy Attributes including $\{nameOfPolicy}, $\{nextAction}, and $\{nonComplianceTime}.
  - User Attributes including $\{sAMAccountName}, $\{userCN}, and $\{userEmailAddressDomain}.
  - Device Attributes including $\{deviceClientDeviceIdentifier}, $\{deviceIMEI}, and $\{deviceModel}.
  - Custom Device/User/LDAP attributes that are created from the **Admin > Attributes** page.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
    \| Send Push Notification                                             | Sends a push notification to the device when the device comes back into compliance.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
    \| Send Both                                                          | Sends both a push notification to the device and an email to the device user's email address notifying them when the device comes back into compliance. You can customize the messages by including optional substitution variables to provide recipients more details as described previously for the Send Email action.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
    The Allowed Apps policy supports [**tiered compliance actions**](./Custom_Policy.md) if you have a Platinum license.
    \| **(Optional) Additional Quarantine Actions**                         | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
    \| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
    \| Quarantine Managed Applications                                      | Removes Ivanti Neurons for MDM managed apps from the device and enables the Block New App Downloads option to block the apps from being re-installed on the device.Select one of the following options:\* **All Applications**
- **Designated Applications** - Add one or more apps by lookup or manually (using Bundle ID or Package name). Click the **View Apps** tab to review the list of added apps. The Block App Store Access default quarantine action is no longer available.On certain devices, the Quarantine action will not remove the application from the device due to certain device limitations. |
  \| Block New App Downloads                                              | Prevents download of any new apps to the device.Select one of the following options:\* **All Applications**
- **Designated Applications** - Add one or more apps by lookup or manually (using Bundle ID or Package name). Click the **View Apps** tab to review the list of added apps. The Block App Store Access default quarantine action is no longer available.                                                                                                                                                                                                                                                |
  \| Remove Configurations                                                | Removes Ivanti Neurons for MDM configurations from the device.Select one of the following options:\* **All Configurations**
- **Designated Configurations** - Select one or more configurations from the list or search for them. Click the **Selected Configurations** tab to review the list of selected configurations.                                                                                                                                                                                                                                                                                          |
  \| Remove Content                                                       | Removes all content and media associated with the apps distributed by Ivanti Neurons for MDM from the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
  \| Suspend Personal Apps                                                | Suspend apps on the personal side of the quarantined device to indicate that device user needs to address the compliance issues on the device to make it functional. Supported on Android 11+ Devices provisioned as a Work Profile on Company Owned Deviceon company owned device.                                                                                                                                                                                                                                                                                                                                |
  \| **Default Quarantine Actions** - these actions are always performed. |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Block App Store Access                                               | Prevents the device from accessing app stores via Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| Block Content Store Access                                           | Prevents the device from accessing content store via Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
  \| Block AppConnect                                                     | Prevents the device from using AppConnect features.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| Block AppTunnel                                                      | Prevents applications on the device from accessing content and servers via AppTunnel.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| Block ActiveSync                                                     | Prevents the device from accessing email via the ActiveSync server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

Click **Next**.
:::

:::WorkflowBlockItem
Configure the distribution.
:::

:::WorkflowBlockItem
Click **Done**.
:::
::::
