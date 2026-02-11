---
title: Working with Policies
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Implement policies**](./Working_with_Policies.md)
- [**Compliance Actions**](./Working_with_Policies.md)
- [**Finding an existing policy**](./Working_with_Policies.md)
- [**Adding a policy**](./Working_with_Policies.md)
- [**Editing a policy**](./Working_with_Policies.md)
- [**Deleting a policy**](./Working_with_Policies.md)

## Implement policies

Policies define requirements for devices, as well as what will happen if a device does not comply with requirements. Each policy consists of a rule and a compliance action (what happens if the rule is violated). Use the **Policies** page to select, set up, and distribute policies.

The following policy types are available:

| **Type**            | **What It Does**                                                                                                                                                                                    |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Compromised Devices | Flags devices that have been jailbroken (iOS) or rooted (Android).To view the violation reason why the system flagged an Android device as compromised due to rooting:1) Click the **Policies** tab |

2. Click the **Compromised Devices** link.
3. Click the **Active Violations** tab.
4. Check the violation reason in the Violation column.To view the violation reason why the system flagged an Android device as compromised due to rooting:1) Click the **Policies** tab.
5. Click the **Compromised Devices** link.
6. Click the **Active Violations** tab.
7. Check the violation reason in the **Violation** column. It will be one of the following reasons\:Priority (1 = highest)

   Violation

   1	Plugin compromised
   2	Client tampered
   3&#x9;

   Unknown device manufacturer: unknown


   4	Suspicious folder detected: \[path]
   5	Suspicious binary found at: \[path]
   6	Folder /data is browsable OR Folder /data/data is browsable
   7	Found /system/app/Superuser.apk
   8	Package manager compromised
   9	Suspicious app found: \[package] |
   \| Data Protection/Encryption Disabled (macOS only) | Flags macOS devices that do not have a passcode or encryption enabled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
   \| International Roaming                            | Flags devices that might be incurring international roaming charges. Status is refreshed when the device checks in.For iOS, the service uses the roaming flag as set and reported by iOS. The compliance action is triggered by the first violation only.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
   \| MDM/Device Administration Disabled               | If the device is MDM-disabled, then it will not be evaluated for any other policies or delta processing of configurations or apps further during check-ins.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
   \| Out of Contact                                   | Flags devices that have been out of contact with Ivanti Neurons for MDM for the specified time range.Choose the actions to take if the device has not checked in for a specified range of hours (2-3 to 23-24) or number of days.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   \| MI Client Out of Contact (iOS only)              | Flags Ivanti Neurons for MDM clients that have been out of contact with Ivanti Neurons for MDM for the specified time range.Choose the actions to take if the client has not checked in for a specified range of hours (2-3 to 23-24) or number of days.This is also applicable for devices registered via iReg. The policy marks a device as non-compliant if there is no client or if the client has not checked-in for a defined period of time.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
   \| [**Allowed Apps**](./Monitoring_and_Controlling_Allowed_Apps.md)                 | Flags devices that violate rules about which apps are allowed or required.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
   \| [**Custom Policy**](./Custom_Policy.md)               | Creates a custom policy based on conditions and related actions you specify.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |

## Compliance Actions

The following compliance actions are available:

| Compliance Action    | What It Does                                                                                                                                                                        |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Monitor              | Flags the device in the Ivanti Neurons for MDM Devices page. By default, this action is turned on.                                                                                  |
| Block                | Instructs Access and /or Sentry to block a device if the device tries to access a resource via Sentry or Access after the policy has been violated as of the last check-in details. |
| Send message to user | - Flags the device in the Ivanti Neurons for MDM Devices page.                                                                                                                      |

- Sends an email to the device owner.
- In addition to the existing policies, the "**Use the Compliance Policy Email Template**" toggle is now available for the following policies as well:
  - Data Protection/Encryption Disabled
  - International Roaming
  - MDM/Device Administration Disabled
  - Out of Contact
  - MI Client Out of Contact

:::Paragraph{indent="1"}
Sends a push notification to the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
\| Quarantine                                | \* Removes most configurations from the device.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Exceptions: passcode configurations, Wi-Fi configurations for Wi-Fi-only devices, Restriction configurations (iOS).
:::

- Removes all apps installed by Ivanti Neurons for MDM.
- Removes all content distributed by Ivanti Neurons for MDM, including iBook and ePub files.
- Blocks access to Ivanti Neurons for MDM catalogs.
- Suspends prompts for installing additional apps.
- Blocks access to AppConnect-enabled apps.
- Includes support for AppConnect-enabled apps.
- If turned on, suspends personal apps on the personal side of the quarantined device to indicate that device user needs to address the compliance issues on the device to make it functional. Supported on Android 11+ Devices provisioned as a Work Profile on Company Owned Device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| Additional Quarantine Actions (Optional): | **Quarantine Managed Applications** - Removes Ivanti Neurons for MDM managed apps from the device and enables the Block New App Downloads option to block the apps from being re-installed on the device.Select one of the following options:\* **All Applications**
- **Remove all apps except the following** - Remove all applications except the ones that are added to the application list.
- **Designated Applications** - Add one or more apps by lookup or manually (using Bundle ID or Package Name). Click the **View Apps** tab to review the list of added apps. The Block App Store Access default quarantine action is no longer available.On certain devices, the Quarantine action will not remove the application from the device due to certain device limitations.- **Block New App Download** - Prevents download of any new apps to the device.By default, this option is selected (for all three: All Applications, Remove all apps except the following and Designated Applications) and cannot be de-selected. This blocks the apps from being re-installed on the device.**Remove configurations** - Removes Ivanti Neurons for MDM configurations from the device.Select one of the following options:\* **All Configurations**
- **Designated Configurations** - Select one or more configurations from the list or search for them. Click the **Selected Configurations** tab to review the list of selected configurations.**Push Designated Configurations** - Distribute designated configurations as part of custom compliance.This list contains configurations meeting the following criteria:\* Enabled configuration
- Non-system configuration
- Quarantinable configuration
- Configurations created in the current space or delegated from the default spaceFor the list of non-quarantinable configurations, see [**Non-quarantinable configurations.**](./Working_with_Policies.md)**Remove Content** - Removes all content and media associated with the apps distributed by Ivanti Neurons for MDM from the device.**Suspend Personal Apps** - Suspend apps on the personal side of the quarantined device to indicate that device user needs to address the compliance issues on the device to make it functional. Supported on Android 11+ Devices provisioned as a Work Profile on Company Owned Device. |

## Finding an existing policy

You can use filters and the search feature in the Policies page to find one or more existing policies.

Procedure

1. Go to **Policies**.
2. To filter a list of policies that match certain criteria, click **Filters**.
3. Select one or more filter criteria.
4. To search for an existing policy by its name, enter the policy name in the **Search** field.

## Adding a policy

Procedure

1. Go to **Policies**.
2. Click +**Add** (upper right).
3. Select a policy type.
4. Complete the settings.
5. Select the device groups you want to receive this policy.You can distribute to a maximum of 100 configuration files at once.
6. Click **Done**.

## Editing a policy

Procedure

1. Go to **Policies**.
2. For the required policy, click the **Edit** (pencil) icon under the Actions column.
3. Make your changes.
4. Save the changes.

## Deleting a policy

Procedure

1. Go to **Policies**.
2. For the required policy, click the **Remove** icon under the Actions column.
3. Click **Yes** to confirm.

If you cannot see the Policies page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- Device Management
- Device Read Only
