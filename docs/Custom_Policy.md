---
title: Custom Policy
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

[**Policies**](./Policies.md)

**License:** Platinum

**Eligible devices:** Android, iOS, macOS, Windows.

Allows you to create a custom policy based on device and user attributes, section criteria, values, and compliance actions you specify.

Even Android Security Patch level setting can be used when defining a custom policy.

## Adding a custom policy

1. Go to **Policies**.
2. Click **+ Add**.
3. Select **Custom Policy**.
4. Provide a name for the custom policy.
5. Click **+ Add Description** to enter additional details if desired.
6. Use the Rule Builder to define conditions that trigger actions when the conditions evaluate as true. See [**Understanding\_the\_conditions\_settings**](./Custom_Policy.md) for guidance on creating the conditions. The Ivanti Neurons for MDM administrator displays the number of duplicate user groups and the corresponding number of GUIDs to identify duplicate groups, when the User Group Name attribute is selected in the rule builder. Also, a table under this rule displays the list of the duplicate user groups and their details such as User Group Name, GUID, Source, and distinguished name (DN).
7. Select one of the compliance actions (see Default Actions below) to take when the specified conditions are met. Adding the action “**Wait**” in between other actions provides a way to allow device users to fix their device and get it back into compliance before additional actions are taken. As an example, you may want to send a warning message and wait 24 hours before applying a quarantine action.
8. Select the **Send a notification when the device comes back into compliance** option, which is turned off by default.\* **Send Email Notification** - Sends an email to the device user's email address notifying them when the device comes back into compliance.- Turn on the **Use the Compliance Policy Email Template** option to insert the message you configure here into the policy notification email template you configure as described in [**Customizing an email template**](./Branding_Email_Templates.md) in [**Branding Email Templates**](./Branding_Email_Templates.md). See [**Configuring and using policy compliance notification emails**](./Configuring_policy_compliance_notification_emails.md) for an overview.

```javascript
![](Resources/Images/68CustomeComplianceTemplate.png)
```

:::Paragraph{listStyleType="disc" indent="2"}
 You can customize the messages by including optional substitution variables to provide recipients more details about policy violations and other relevant information. Click the following attribute types to display the complete list of variables:\* Policy Attributes including $\{nameOfPolicy}, $\{nextAction}, and $\{nonComplianceTime}.
:::

:::Paragraph{listStyleType="disc" indent="3"}
User Attributes including $\{sAMAccountName}, $\{userCN}, and $\{userEmailAddressDomain}.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Device Attributes including $\{deviceClientDeviceIdentifier},  $\{deviceIMEI}, and $\{deviceModel}.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Custom Device/User/LDAP attributes that are created from the **Admin > Attributes** page.
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Send Push Notification** - Sends a push notification to the device when the device comes back into compliance.
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Send Both** - Sends both a push notification to the device and an email to the device user's email address notifying them when the device comes back into compliance. You can customize the messages by including optional substitution variables to provide recipients more details as described previously for the Send Email action.
:::

9. Specify the following options from the table to notify the administrators and the registered device owners if the device owners violate the policy rules:|                      |                                                                                                                 |
   \| -------------------- | --------------------------------------------------------------------------------------------------------------- |
   \| **Option**           | **Description**                                                                                                 |
   \| Subject              | Enter the subject text. For example, "You have violated a policy!."                                             |
   \| Body                 | Enter the message as needed. For example, "Action required!."                                                   |
   \| CC to administrators | Enter the e-mail ID of the administrators. Use a semicolon (;) as a separator to add multiple e-mail addresses. |
   \| Preview E-Mail       | Click the **Preview E-Mail** button to view the e-mail address.                                                 |
10. Click **Next** to save the policy details.

Default actions:

::::WorkflowBlock
:::WorkflowBlockItem
- **Monitor** - Currently always selected. Sentry version 9.0.0 or later is required to utilize the tiered compliance actions.
- **Do Nothing**
- **Send Notification**\* **Send Email** - Sends an email to the device user's email address notifying them that the device is out of compliance.- You can use the policy notification email template as described above.
  - You can customize the messages by including optional substitution variables to provide recipients more details about policy violations and other relevant information. This provides users of non-compliant devices with relevant information about the policy violation so they can take remedial actions. Click the following attribute types to display the complete list of variables:\* Policy Attributes including $\{nameOfPolicy}, $\{nextAction}, and $\{nonComplianceTime}.
    - User Attributes including $\{sAMAccountName}, $\{userCN}, and $\{userEmailAddressDomain}.
    - Device Attributes including $\{deviceClientDeviceIdentifier},  $\{deviceIMEI}, and $\{deviceModel}.
    - Custom Device/User/LDAP attributes that are created from the **Admin > Attributes** page.
  - **Send Push Notification** - Sends a push notification to the device that the device is out of compliance.
  - **Send Both** - Sends both a push notification to the device and an email to the device user's email address notifying them the device is out of compliance. You can customize the messages by including optional substitution variables to provide recipients more details as described previously for the Send Email action.
- **Block** - Uses Sentry to block managed devices from accessing email and AppConnect-enabled applications. Sentry version 9.0.0 or later is required to utilize the block action.
- **Retire** - Retires the device. **This action cannot be undone**. For example, there can be a rule to retire the devices for all the disabled users by using the User Enabled condition.
- **Wait** - Delays action for a specified time period (hours or days) to allow users to remediate the violation before additional actions are taken if the device remains in a non-compliant state.
- **Quarantine** - Removes access to apps, content, and servers as per the following actions:|                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
  \| **(Optional) Additional Quarantine Actions**                         | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Quarantine Managed Applications                                      | Removes Ivanti Neurons for MDM managed apps from the device and enables the Block New App Downloads option to block the apps from being re-installed on the device.Select one of the following options:\* **All Applications**
  - **Designated Applications** - Add one or more apps by lookup or manually (using Bundle ID or Package Name). Click the **View Apps** tab to review the list of added apps. The Block App Store Access default quarantine action is no longer available.On certain devices, the Quarantine action will not remove the application from the device due to certain device limitations. |
    \| Block New App Downloads                                              | Prevents download of any new apps to the device.Select one of the following options:\* **All Applications**
  - **Designated Applications** - Add one or more apps by lookup or manually (using Bundle ID or Package Name). Click the **View Apps** tab to review the list of added apps. The Block App Store Access default quarantine action is no longer available.By default this option is selected (for both All Applications and Designated Applications) and cannot be de-selected. This blocks the apps from being re-installed on the device.                                                               |
    \| Remove Configurations                                                | Removes Ivanti Neurons for MDM configurations from the device.Select one of the following options:\* **All Configurations**
  - **Designated Configurations** - Select one or more configurations from the list or search for them. Click the **Selected Configurations** tab to review the list of selected configurations.                                                                                                                                                                                                                                                                                          |
    \| Push Designated Configurations                                       | Distribute designated configurations as part of custom compliance.This list contains configurations meeting the following criteria:\* Enabled configuration
  - Non-system configuration
  - Quarantinable configuration
  - Configurations created in the current space or delegated from the default spaceFor the list of non-quarantinable configurations, see [**Non-quarantinable configurations.**](./Custom_Policy.md)For more information, see the [**Pushing a designated configuration&#x20;**](./Custom_Policy.md)section after this procedure.                                                                                                |
    \| Remove Content                                                       | Removes all content and media associated with the apps distributed by Ivanti Neurons for MDM from the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
    \| Suspend Personal Apps                                                | Suspend apps on the personal side of the quarantined device to indicate that device user needs to address the compliance issues on the device to make it functional. Supported on Android 11+ Devices provisioned as a Work Profile on Company Owned Device.                                                                                                                                                                                                                                                                                                                                                       |
    \| **Default Quarantine Actions** - these actions are always performed. |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
    \| Block App Store Access                                               | Prevents the device from accessing app stores via Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
    \| Block Content Store Access                                           | Prevents the device from accessing content store via Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
    \| Block AppConnect                                                     | Prevents the device from using AppConnect features.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    \| Block AppTunnel                                                      | Prevents applications on the device from accessing content and servers via AppTunnel.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
    \| Block ActiveSync                                                     | Prevents the device from accessing email via the ActiveSync server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    Click the **Yes** check box to affirm that you understand that if this policy has previously been triggered on a device, adding the tiered policy will reset the policy and any compliance actions that had previously been applied. The new custom policy takes effect upon the next device check-in. If you selected the Retire action, then click **Yes** to affirm that you understand that you cannot undo the action.
:::

:::WorkflowBlockItem
Click **Next** to configure which devices the policy and actions will apply to.
:::

:::WorkflowBlockItem
Click **Done**.
:::
::::

The following table illustrates the quarantine behavior on various Android devices when the Ivanti Neurons for MDM is the initiator of the quarantine action:

| **Devices**                                                | **Quarantine behavior**                           |
| ---------------------------------------------------------- | ------------------------------------------------- |
| Samsung devices in Device Admin mode via the Go client app | - Uninstall both managed public and in-house apps |

- Remove certain profiles (excluding Mobile Threat Defense and others)                             |
  \| Non-Samsung devices in Device Admin mode via the Go client appMAM via the AppStation app | \* Do not support uninstalling or hiding both managed public and in-house apps
- Remove certain profiles (excluding Mobile Threat Defense and others) |
  \| Android Enterprise via the Go client app                                                 | - Hide both managed public and in-house apps
- Remove certain profiles (excluding Mobile Threat Defense and others)                                  |

### Pushing a designated configuration

Distribute designated configurations as part of custom compliance. Configure the Custom Policy to distribute a set of configurations when a device goes out of compliance. Reset the device to its previous state as part of remediation action when a device status changes from non-compliant to compliant status.

An error occurs when an administrator tries to delegate a custom policy that has non-delegated configurations under the Push Designated Configurations tab.

The following are the behaviors when configurations are pushed via custom policies under certain conditions:

| Condition(s)                                                                                                                                                                                                              | Behavior                                                                                                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Two configurations of same type are selected which have priority set                                                                                                                                                      | Configuration with the higher priority will be pushed to the device.                                                                                                                                                                                  |
| Two configurations of same type are selected which do not have priority set                                                                                                                                               | Both configurations will be pushed to device. May result in unexpected behaviors.                                                                                                                                                                     |
| When device already has a configuration of the same type which supports priority defined in the Custom Policy                                                                                                             | The configuration defined in the Custom Policy will take precedence and will be pushed to the device. The one existing on the device will be removed irrespective of priority (even if its priority is higher than the one defined in custom policy). |
| When device already has a configuration of the same type which does not support priority defined in the Custom Policy                                                                                                     | The configuration defined in the Custom Policy will be pushed to the device. Both configurations will be present on the device. May result in unexpected behaviors.                                                                                   |
| If the priority of a configuration is changed after the Custom Policy is created                                                                                                                                          | On device check-in, the configuration with the highest priority will be pushed if it is part of the Custom Policy.                                                                                                                                    |
| When both conditions are met:\* Condition A: When a device with a violation has had a configuration pushed as part of a custom policy (and it took priority over a configuration of the same type already on the device). |                                                                                                                                                                                                                                                       |

- Condition B: Violation has been re-mediated and device is no longer in quarantine | The configuration defined in the Custom Policy will be removed and the one of the same type on the device before quarantine will be pushed through the application of existing device groups, reverting the device back to its original state.        |

In the Quarantine action, if you select Remove Configurations along with Push Designated Configurations, note the following rules:

- Remove all configurations + Push Designated Configurations: In this scenario, all configurations from the device will be removed and the configurations selected under Push Designated Configurations will be pushed to the device.
- Remove designated configuration(s) (in one custom policy) + Push Designated Configuration(s) (in another custom policy) with common configuration(s) in the selection of both: As the configurations are selected in two different compliance policies, the most restrictive approach would be taken i.e. the configuration(s) will be removed from the device.

You can delegate a custom policy from the default [**space**](./Managing_Spaces.md) to a custom space. For a custom policy to be delegated, the configurations mentioned in the custom policy under the Push Designated Configurations tab need to be delegated to spaces.

On the [**Devices**](./Devices.md) page, you can click the name of a device to visit the device details page. Under the Configurations tab, the Distribution Method column indicates the distribution method for a configuration pushed to the device. It can be either "Device Group" or "Compliance Action."

On the Configurations page, for each configuration, Ivanti Neurons for MDM displays a count of devices that received the configuration via device group and via compliance action.

### Understanding the conditions settings

The following table describes some fields available to build rules:

| **UI Field** | **Description**                                          | **Possible values**                   | **Supported Platforms** |
| ------------ | -------------------------------------------------------- | ------------------------------------- | ----------------------- |
| APNS Capable | This field indicates whether the device is APNS capable. | Possible operators are:\* is equal to |                         |

- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/macOS/Android                  |
  \| Anti-phishing native status      | This field displays the anti-phishing native status                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Possible operators are:\* is equal to
- is not equal toPossible valuesare:- Not Enabled\* N/A
- Enabled
- Unknown                                                                                                                                                                                                                                                                       | iOS/Android                        |
  \| Anti-phishing status             | This field displays the anti-phishing status                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Possible operators are:\* is equal to
- is not equal toPossible values are:\* Not Enabled
- N/A
- Enabled
- Unknown                                                                                                                                                                                                                                                                     | iOS/Android                        |
  \| Anti-phishing VPN status         | This field displays the anti-phishing VPN status                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Possible operators are:\* is equal to
- is not equal toPossible values are:- Not Enabled\* N/A
- Enabled
- Unknown                                                                                                                                                                                                                                                                      | iOS/Android                        |
  \| Battery Information              | This field has the following attributes:\* Battery Level - Displays current battery charge level as reported by the Android OS
- Battery Health Status - As reported by the Android OS
- Battery Charging Status - As reported by the Android OS
- Battery Health Percentage (OEM Specific) - Battery health in percentage for supported device manufacturers such as Zebra devices
- Battery Manufacture Date (OEM) - Battery manufactured date for supported device manufacturers such as Zebra devices
- Battery Charge Cycles (OEM) - Number of cycles completed in total for supported device manufacturers such as Zebra devices | For information on possible values, see [**Using Advanced Search**](./Finding_and_Filtering_Devices.md).                                                                                                                                                                                                                                                                           | Android                            |
  \| Bootstrap Token Available        | This field indicates whether a bootstrap token is available for a device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Possible operators are:\* is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | macOS                              |
  \| Autopilot Enrolled               | This field indicates whether device is Autopilot Enrolled or not.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | - is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                                        | Windows                            |
  \| Bridge Last Check-in             | This field indicates the bridge last check-in time of the client.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Possible operators are:- is less than
- is less than or equal to
- is greater than
- is greater than or equal to
- is in range
- is not in rangeEnter the numerical value of bridge last check-in time. Select any of the following option for the duration:- hours
- daysExample: Bridge Last Check-in is less than 12 hours ago.                                                    | Windows                            |
  \| Client Last Check-in             | This field indicates the last check-in time of the client.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Possible operators are:- is less than
- is greater thanEnter the numerical value of last check-in time. Select any of the following option for the duration:- hours
- daysExample: Client Last Check-in is less than 12 hours ago.                                                                                                                                                    | iOS/macOS/Android                  |
  \| Client Registered                | This field indicates the status of the client registered.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/macOS/Android                  |
  \| Compromised                      | This field indicates whether the device is rooted/compromised.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Possible operators are:- is equal to
- is not equal toPossible values are:- jailbroken or rooted
- not compromised                                                                                                                                                                                                                                                                    | iOS/Android                        |
  \| Current Country Name             | This field indicates the name of the current country corresponding to the Mobile Country Code (MCC) or Mobile Network Code (MNC) that the device reports to be currently connected.                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Possible operators are:- is equal to
- is not equal toPossible value is a drop down list value that indicates the home country name.                                                                                                                                                                                                                                                  | iOS/macOS/Android                  |
  \| Current MCC                      | This field indicates the current mobile country code                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Enter the attribute's value to be verified. Possible operators are:- is equal to
- is not equal to                                                                                                                                                                                                                                                                                    | iOS/macOS/Android                  |
  \| Current MNC                      | This field indicates the current mobile network code                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Enter the attribute's value to be verified. Possible operators are:- is equal to
- is not equal to                                                                                                                                                                                                                                                                                    | iOS/macOS/Android                  |
  \| Custom Device Attribute          | This field enables adding an existing custom device attribute as a condition of a rule to verify its value.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Enter the attribute's value to be verified. Possible operators are:- is equal to
- is not equal to
- contains
- does not containValue can be a string of ASCII characters, including Space and Unicode characters.                                                                                                                                                                    | iOS/macOS/Android/Windows          |
  \| Custom LDAP Attribute            | This field enables adding an existing custom LDAP attribute as a condition of a rule to verify its value.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Enter the attribute's value to be verified. Possible operators are:- is equal to
- is not equal to
- contains
- does not containValue can be a string of ASCII characters, including Space and Unicode characters.                                                                                                                                                                    | iOS/macOS/Android/Windows          |
  \| Custom User Attribute            | This field enables adding an existing custom user attribute as a condition of a rule to verify its value.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Enter the attribute's value to be verified. Possible operators are:- is equal to
- is not equal to
- contains
- does not containValue can be a string of ASCII characters, including Space and Unicode characters.                                                                                                                                                                    | iOS/macOS/Android/Windows          |
  \| Data Roaming                     | This field enables data roaming to be used as a condition of a rule to verify its value.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.Default value is No if the supported device does not report info about this field.                                                                                                                                                                                                               | iOS/Android                        |
  \| Device Type                      | This field represents the device model.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Possible operators are:- is equal to
- is not equal to
- begins with
- ends withPossible value is a text value.                                                                                                                                                                                                                                                                       | iOS/macOS/Android/Windows          |
  \| Device Type (Apple)              | This field represents the device model pretty name.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Possible operators are:- is equal to
- is not equal to
- begins with
- ends withPossible value is a text value.                                                                                                                                                                                                                                                                       | iOS/macOS                          |
  \| Encryption Enabled               | This field determines whether the device is encryption/data protection enabled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Yes - Device is encryption/data protection enabled.No - Device is not encryption/data protection enabled.                                                                                                                                                                                                                                                                             | iOS/Android/Windows                |
  \| GUID                             | This field indicates the device GUID.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Possible operators are:- is equal to
- is not equal to
- begins with
- ends with                                                                                                                                                                                                                                                                                                      | iOS/macOS/Android/Windows          |
  \| Home Country Name                | This field indicates the name of the home country corresponding to the Mobile Country Code (MCC) or Mobile Network Code (MNC) that is programmed into the SIM or eSIM of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Possible operators are:- is equal to
- is not equal toPossible value is a drop down list value that indicates the home country name.                                                                                                                                                                                                                                                  | iOS/Android/Windows                |
  \| Has Failed Windows Update        | This field determines whether the device is out of compliance with the latest update rules.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Yes - Device is not compliant with the latest update.No - Device is compliant with the latest update.                                                                                                                                                                                                                                                                                 | Windows                            |
  \| Home MCC                         | This field indicates the home Mobile Country Code.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Enter the attribute's value to be verified. Possible operators are:- is equal to
- is not equal to                                                                                                                                                                                                                                                                                    | iOS/macOS/Android                  |
  \| Home MNC                         | This field indicates the home Mobile Network Code                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Enter the attribute's value to be verified. Possible operators are:- is equal to
- is not equal to                                                                                                                                                                                                                                                                                    | iOS/macOS/Android                  |
  \| IMEI                             | This field indicates the IMEI number of the first SIM slot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Possible operators are:- is equal to
- is not equal to
- begins with
- ends with                                                                                                                                                                                                                                                                                                      | iOS/Android/Windows                |
  \| IMEI2                            | This field indicates the IMEI number of the second SIM slot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Possible operators are:- is equal to
- is not equal to
- begins with
- ends with                                                                                                                                                                                                                                                                                                      | Android                            |
  \| IMSI                             | This field indicates the IMSI number of the SIM card.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Possible operators are:- is equal to
- is not equal to
- begins with
- ends with                                                                                                                                                                                                                                                                                                      | Android/Windows                    |
  \| Last Check-in                    | This field allows you to set conditions related to the last check-in time of the managed device via MDM channel.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Possible operators are:- is less than
- is greater thanEnter the numerical value of last check-in time. Select any of the following option for the duration:- hours
- daysExample: Last Check-in is greater than 12 hours ago.                                                                                                                                                        | iOS/macOS/Android/Windows          |
  \| Last Hotfix ID                   | This field allows you to set conditions related to the last hotfix ID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Possible operators are:- is equal to
- is not equal to
- is less than
- is less than or equal to
- is greater than
- is greater than or equal to
- contains
- does not contain
- begins with
- does not begin with
- ends with
- does not end with                                                                                                                                    | Windows                            |
  \| Last Hotfix Installed On         | This field allows you to set conditions related to the hotfix that was last installed.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Possible operators are:- is less than
- is greater than                                                                                                                                                                                                                                                                                                                               | Windows                            |
  \| Locator Services Enabled         | This field indicates whether the device has a device locator service (such as Find My iPhone) enabled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS                                |
  \| Manufacturer                     | This field allows you to set conditions related to manufacturer of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Possible operators are:- is equal to
- is not equal toPossible values are:- Samsung
- NOKIA
- HTC
- LGE
- Apple Inc                                                                                                                                                                                                                                                                   | iOS/macOS/Android/Windows          |
  \| MTD activation status            | This field represents the MTD activation status                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Possible operators are:- is equal to
- is not equal toPossible values are:- N/A
- Error
- Pending
- Protected                                                                                                                                                                                                                                                                         | iOS/Android                        |
  \| MDM Managed                      | This field determines whether the device is MDM/Device admin enabled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/macOS/Android                  |
  \| OS                               | This field represents the OS type of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Possible operators are:- is equal to
- is not equal toPossible values are:- macOS
- Android
- iOS
- Windows
- visionOS                                                                                                                                                                                                                                                                | iOS/macOS/visionOS/Android/Windows |
  \| OS Build Version                 | This field represents the OS build version of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Possible operators are:- is equal to
- is not equal to
- is less than
- is less than or equal to
- is greater than
- is greater than or equal to
- contains
- does not contain
- begins with
- does not begin with
- is not blank
- is blank
- ends with
- does not end with                                                                                                          | iOS/macOS/visionOS/Android/Windows |
  \| OS Version                       | This field represents the OS version of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Possible operators are:- is equal to
- is not equal to
- is less than
- is less than or equal to
- is greater than
- is greater than or equal to
- is in range
- is not in rangePossible value is text.                                                                                                                                                                               | iOS/macOS/visionOS/Android/Windows |
  \| OS With Version                  | This field represents the OS and the OS version of the device                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Possible operators are:- is equal to
- is not equal to
- is less than
- is less than or equal to
- is greater than
- is greater than or equal to
- is in range
- is not in rangePossible value is text.                                                                                                                                                                               | iOS/macOS/visionOS/Android/Windows |
  \| Ownership                        | This field indicates the ownership type of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Possible operators are:- is equal to
- is not equal toPossible values are:- user owned
- not set
- company owned                                                                                                                                                                                                                                                                      | iOS/macOS/Android/Windows          |
  \| Passcode Compliant With Profiles | This field indicates whether is device is passcode compliant with profiles.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/macOS/Android                  |
  \| Personal Hotspot Enabled         | This field indicates whether Personal Hotspot feature is enabled on the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.The Personal Hotspot setting is only available on certain carriers.                                                                                                                                                                                                                              | iOS                                |
  \| Phone #                          | This field indicates the device phone number.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Possible operators are:- is equal to
- is not equal to
- contains
- begins with
- ends with                                                                                                                                                                                                                                                                                           | iOS/Android/Windows                |
  \| Public IP Address                | This field indicates the public IP address.If the device uses a VPN connection or a proxy server to connect to Ivanti Neurons for MDM, it displays the proxy WAN IP address.                                                                                                                                                                                                                                                                                                                                                                                                                                     | Possible operators are:- is in range
- is not in range
- is not blank
- is blank                                                                                                                                                                                                                                                                                                      | Android/ChromeOS                   |
  \| Roaming                          | This field indicates the roaming status of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/Android/Windows                |
  \| Sentry Blocked                   | Indicates whether the device is blocked by Sentry.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/macOS/Android/Windows          |
  \| Status                           | This field indicates the registration status.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Possible operators are:- is equal to
- is not equal toThe default possible value is 'Active.'In custom policies, it restricts the device state to Active by removing all other potential values because policy evaluation occurs when the device checks in for Active, Retire-pending, and Wipe-pending statuses, and these devices will have their policies evaluated upon check-in. | iOS/macOS/Android                  |
  \| Serial Number                    | This field indicates the device serial number.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Possible operators are:- is equal to
- is not equal to
- begins with
- ends with                                                                                                                                                                                                                                                                                                      | iOS/macOS/Android/Windows          |
  \| Supervised                       | This field indicates whether the device is supervised.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/macOS                          |
  \| Supplemental Build Version       | This field represents the supplemental build version of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Possible operators are:- is equal to
- is not equal to
- is less than
- is less than or equal to
- is greater than
- is greater than or equal to
- contains
- does not contain
- begins with
- does not begin with
- ends with
- does not end with
- is not blank
- is blank                                                                                                          | iOS/macOS                          |
  \| Supplemental OS/Version Extra    | This field represents the supplemental OS build version of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Possible operators are:- is equal to
- is not equal to
- is less than
- is less than or equal to
- is greater than
- is greater than or equal to
- contains
- does not contain
- begins with
- does not begin with
- ends with
- does not end with
- is not blank
- is blank                                                                                                          | iOS/macOS                          |
  \| User Enabled                     | This field indicates whether the user is enabled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/macOS/Android/Windows          |
  \| User Group                       | This field represents the user group.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Possible operators are:- is equal to
- is not equal to                                                                                                                                                                                                                                                                                                                                | iOS/macOS/Android/Windows          |
  \| Voice Roaming                    | This field indicates whether voice roaming is enabled on the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.The voice roaming setting is only available on certain carriers.Disabling voice roaming also disables data roaming.Default value is not equal to if the supported device does not report info about this field.                                                                                  | iOS                                |
  \| Access Blocked                   | Indicates whether the device is blocked by Access.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/macOS/Android/Windows          |
  \| Compliance                       | Indicates whether the device is compliant or not.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Possible operators are:- is equal to
- is not equal toPossible values are In Compliance and Out of Compliance.                                                                                                                                                                                                                                                                        | iOS/macOS/Android/Windows          |
  \| Compliance Action Blocked        | Indicates whether the device is blocked or not.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Possible operators are:- is equal to
- is not equal toPossible values are Yes and No.                                                                                                                                                                                                                                                                                                 | iOS/macOS/Android/Windows          |

### Non-quarantinable configurations

The following table shows the list of configurations that are non-quarantinable:

| OS          | **Non-Quarantinable Configurations** |
| ----------- | ------------------------------------ |
| **Android** | - Android App Catalog                |

- Android Encryption
- Android enterprise
- Android enterprise App
- Android Zebra
- Anti-phishing Protection
- Android Work Challenge
- Device Passcode
- File download
- Lockdown & Kiosk: Android Device Admin Mode
- Lockdown & Kiosk: Samsung Knox Standard
- MAM Only
- Managed Device with Work Profile/Work Profile on Company Owned Device
- Work Managed Devices (Device Owner)
- Samsung Phone Restrictions
- SafetyNet Attestation
- Work Profile on Company Owned Device                                                                                       |
  \| **iOS and macOS** | \* Anti-phishing Protection (iOS)
- App Notifications (iOS)
- AppStation Sites (iOS)
- Filevault Recovery Key (macOS)
- Filevault 2 (macOS)
- Global Proxy (iOS)
- Home Screen Layout (iOS)
- iOS App Control
- iOS Restrictions
- iOS Software Updates (iOS)
- macOS Firewall
- macOS Software Updates
- MAM Only (iOS)
- MI Client Privacy (iOS/macOS)
- Network Usage (iOS)
- Office 365 Account Creation (macOS)
- Single App Mode (iOS)
- System Policy Control (macOS)
- System Policy Managed (macOS)
- System Policy Rule options (macOS)
- Time Server (macOS)
- Web Content Filter (iOS) |
  \| **Windows**       | - Windows App Control
- Windows Restrictions DDF (Data Definition File)
- Windows Firewall
- Windows Network Proxy
- Windows Restrictions
- Windows Update                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| **All**           | \* Active Directory
- Client Services
- Mobile Device Management
- Mobile Threat Defense Activation
- Mobile Threat Defense Local Actions
- Passcode
- Privacy
- Privacy Statement
- ServiceConnect
- Sync                                                                                                                                                                                                                                                                                                                                                                                         |

If you cannot see the Policy page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- Device Management
- Device Read Only
