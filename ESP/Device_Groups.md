---
title: Device Groups
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Adding a device group**](./Device_Groups.md)
- [**Removing a device group**](./Device_Groups.md)
- [**Exporting devices to a CSV file**](./Device_Groups.md)

In the **Device Groups** page, you can create lists of devices that you want to treat in the same way. You can define and assign policies and configurations to the device groups. The following are the default device groups created by Ivanti Neurons for MDM:

- All Devices
- Android Devices
- Android Enterprise Devices
- iOS Devices
- Device Type (Apple )
- tvOS Devices
- macOS Devices
- visionOS Devices
- watchOS Devices
- Windows Devices

The details of the apps assigned to a specific device group is displayed under the **Apps** tab for the specific device group.

The tvOS device group is a subset of the iOS device group. Therefore, the configurations and policies applied to tvOS group might be overwritten by the iOS device group.

## Adding a device group

Adding a device group is not applicable to Dynamic User Groups.

Depending on the type of license you have, you can add a new device group based on rules to identify the devices with specific criteria. The devices matching the rules are displayed below the rule builder section. The rules can be nested together using the ANY (OR) or ALL (AND) options. The rules can be constructed using the following operators:

- begins with
- ends with
- contains
- does not contain
- does not begin with
- does not end with
- is less than
- is greater than
- is in range
- is equal to
- is not equal to
- is not blank
- is blank

The Ivanti Neurons for MDM Administrator displays a number of duplicate user groups and the corresponding number of GUIDs to identify duplicate groups, when the User Group Name attribute is selected in the rule builder. Also, a table under this rule displays the list of the duplicate user groups and their details such as User Group Name, GUID, Source, and distinguished name (DN).

**Bronze license:**

Rules can identify devices by the following criteria:

- Device Type
- OS - operating system (pre-populated)
- OS Version
- OS With Version
- User Group

**Silver license:**

Rules can identify devices by the following criteria:

- Entra ID Enrolled
- Alternative Serial Number (Android Only - applicable for Samsung devices in Device Admin or Device Owner mode)
- Android Dedicated Device
- Android Enterprise Capable
- Android Managed Device with Work Profile
- Android SafetyNet Attestation Type
- Android Work Enabled
- Android Work Managed Devices (Device Owner) Enabled
- Android Work Profile Enabled
- Android Work Profile on Company Owned Devices Enabled
- Anti-phishing native status
- Anti-phishing status
- Anti-phishing VPN status
- APNS Capable
- Apple Silicon Device
- Automated Device Enrollment Enabled
- Azure Device Identifier
- Azure Device Compliance Status
- Azure Client Status Code
- Azure Device Compliance Report Time
- BitLocker Encryption
- Sentry Blocked
- Access Blocked
- Bootstrap Token Available
- Bulk Provisioned Type (Apple Configurator, None, or Automated Device Enrollment Enrolled)
- Carrier
- Client Last Check-in
- Client Registered
- Compliance
- Compliance Action Blocked
- Current Country Name (select the current country name from the drop down list)
- Current MCC
- Current MNC
- Custom Device Attribute
- Custom LDAP Attribute
- Custom User Attribute
- Data Roaming
- Device Registered
- Device Source
- Device Type
- Display Name
- Encryption Enabled
- Hard Drive Partitions
- Home Country Name (select the home country name from the drop down list)
- Home MCC
- Home MNC
- IMEI
- IMEI2 (only on Android devices with a dual SIM port and applicable for Android 8.0 or higher devices)
- IP Address
- Kiosk Mode
- Last Check-in
- MAM Only
- Manufacturer
- MTD activation status
- OS
- OS Edition
- OS Version
- OS With Version
- Ownership
- Phone #
- Public IP Address (Android or ChromeOS devices)
- Quarantined
- Recovery Lock Enabled
- Roaming
- Secure Apps Status
- Serial Number
- Status
- Supervised
- System Version
- Total Device Capacity
- Total Memory MB
- TPM Version
- Unlock Token Available (iOS)
- User Enrollment Enabled
- User Group
- Voice Roaming
- macOS Personal Recovery Key escrowed
- macOS Recovery Key Type

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Click **Add**.
:::

:::WorkflowBlockItem
Enter a name for the group.
:::

:::WorkflowBlockItem
Enter an optional description for the group.
:::

:::WorkflowBlockItem
Select the type of device group you want to create:\* **Dynamically Managed**: Use rules to define which devices are in the group.

- **Manually Managed**: Enter each user whose devices are to be included in the group.
:::

:::WorkflowBlockItem
For dynamically-managed groups:1) Create a rule that defines the group.
2\) **Example**: OS is iOS

Click **+** to create additional rules, if needed.
3\) **Example**: Device is iPhone 5S

Click **Any** if the devices need to match at least one of the rules.
4\) Click **All** if the devices need to match all the rules.
:::

:::WorkflowBlockItem
For manually-managed groups:
:::

:::WorkflowBlockItem
1. Type the name of a user whose device you want to add.
2. Select the device from the displayed list.
3. Repeat steps a and b until all devices are displayed in the list.
   Click **Save**.
:::
::::

## Removing a device group

**Procedure**

1. Go to **Devices** > **Device Groups**.
2. Click the check-box for the device group you want to remove.
3. Click **Delete Device Group**.

## Exporting devices to a CSV file

You can export the device details of a specific device group using the **Export to CSV** option from the **Device Groups** page.

**Procedure**

1. Go to **Devices&#x20;**>**&#x20;Device Groups**.
2. Select all or multiple spaces to view the information related to specific spaces.
3. Click the device group count link. The Devices list page related to the selected space is displayed.
4. Click the **Export to CSV** option to export the devices list and related details to a CSV file. A pop-up message appears that the export report would take some time to process. Wait for the request to complete before you submit another request.
5. Click **Download**. You will receive an email containing a link to download the report.
6. (Optional) Click **Delete&#x20;**&#x74;o delete the report.

If you cannot see the **Device Groups** page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md)

- Device Management
- Device Read Only
