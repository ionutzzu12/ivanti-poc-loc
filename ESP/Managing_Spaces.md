---
title: Managing Spaces
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Spaces enable you to designate device groups for management by different administrators (delegated administration). The administrator for a space can define the configurations and policies applied to the devices in the space. After you create the spaces, you can assign each space to the relevant or appropriate administrator. You cannot edit or delete the default space.

The user can view only the spaces assigned and not all the available spaces. As of now, this setting applies to the **Devices**, **Device Groups**, **Apps**, **App Inventory**, **Content**, **Configurations**, **Policies**, and **Certificate Management** modules only. Spaces selected from the Spaces list while viewing any of these modules are saved as administrator preferred default selection for that module. These preferences are not only saved for the current login session, but also for the future sessions.

The spaces you create inherit all configurations from the default space. Therefore, any configurations you create later in the default space are eligible to be applied to the other spaces. However, changes made to an existing configuration are not inherited.

The spaces you create receive copies of only those policies that exist in the default space at that time. Any policies you create later in the default space apply only to the default space.

Create the rules that define which devices are in the space. These rules can be filtered using the applicable operators, including the "begins with", "ends with", "contains", "does not contain", "does not begin with", "does not end with", "is less than", "is greater than", "is in range", "is equal to", and "is not equal to" operators. The rules can be nested together using the ANY (OR) or ALL (AND) options. The accuracy of the rules can be reviewed using the text that appears at the end of the rules.

The Ivanti Neurons for MDM Administrator portal displays the number of duplicate user groups and the corresponding number of GUIDs to identify duplicate groups, when the User Group Name attribute is selected in the rule builder. Also, a table under this rule displays the list of the duplicate user groups and their details such as User Group Name, GUID, Source, and distinguished name (DN).

Rules can identify devices by:

- Entra ID Enrolled
- APNS Capable
- Alternative Serial Number (Android Only - applicable for Samsung devices in Device Admin or Device Owner mode)
- Android 5G Network Slicing Enabled
- Android Work Managed Device Non-GMS mode (AOSP) Enabled
- Android Dedicated Device
- Android Enterprise Capable
- Android Managed Device with Work Profile
- Android SafetyNet Attestation Type
- Android Work Enabled
- Android Work Managed Devices (Device Owner) Enabled
- Android Work Profile Enabled
- Android Work Profile Enabled on Company Owned Devices Enabled
- Anti-phishing native status
- Anti-phishing status
- Anti-phishing VPN status
- Automated Device Enrollment Enrolled
- Autopilot Enrolled
- Azure Client Status Code
- Azure Device Compliance Report Time
- Azure Device Compliance Status
- Azure Device Identifier
- Sentry Blocked
- Access Blocked
- Bootstrap Token Available
- Bulk Provisioned Type (Apple Configurator, None, or Automated Device Enrollment Enrolled)
- Carrier
- Client Last Check-in
- Client Registered
- Compliance
- Compliance Action Blocked
- Current Country Name (select the country name from the drop down list)
- Current MCC
- Current MNC
- Custom Device Attribute
- Custom LDAP Attribute
- Custom User Attribute
- Data Roaming
- Device Source
- Device Type
- Device Type (Apple)
- Display Name
- Encryption Enabled
- Home Country Name (select the home country from the drop down list)
- Home MCC
- Home MNC
- IMEI
- IMEI2 (only on Android devices with a dual SIM port and applicable for Android 8.0 or higher devices)
- IP Address
- Kiosk Mode
- Last Check-in
- Lost Mode Enabled
- MAM Only
- Manufacturer
- MTD activation status
- Multi-User Mode
- OS
- OS Version
- OS With Version
- Ownership
- Phone #
- Quarantined
- Recovery Lock Enabled
- Roaming
- Secure Apps Status
- Serial Number
- Status
- Supervised
- Supplemental Build Version
- Supplemental OS/Version Extra
- Unlock Token Available (iOS)
- User Enrollment Enrolled
- User Group
- Username
- Voice Roaming
- macOS Personal Recovery Key escrowed
- macOS Recovery Key Type

These rules are available only for **Silver** license and above.

## Creating a Space

**Procedure**

1. Go to **Admin >****Spaces**.
2. Click **Manage**.
3. Click **Create New Space**.
4. Click **Preview** to see which devices will be assigned to the space.
5. Click **Save** when you are satisfied with the devices in the space.To delete, click on the Delete icon for the created space.

## Prioritizing Spaces

Ivanti Neurons for MDM assesses spaces in order of appearance. To change the order, click the arrows in the upper right corner of the space definition.

::Image[]{src="partitionarrows.png" signedSrc="partitionarrows.png" size="10" caption alt isUploading="false" sha initialPath="partitionarrows.png" githubPath="partitionarrows.png" position="flex-start"}

## Assigning an Administrator to a Space

**Procedure**

1. Go to **Users**.
2. Search for the user who will be the administrator.
3. Click the link for the user to display detail.
4. Select **Actions > Assign Roles**.
5. Select **Device Management**.
6. Under **Device Management**, select the space for this administrator.
7. Click **Done**.

When this administrator logs in, only devices, configurations, and policies in the assigned space will be visible.

## Cloning a Configuration or a Policy

You can clone a configuration or a policy if you need to duplicate them with a few differences. You can also associate the cloned configurations or policies to different device groups. All the policies can be cloned within a space. All configurations, except the user-provided Identity Certificate and Threat Defense, can be cloned within a space. The following configurations can also be cloned across spaces from the default space:

- iOS Restrictions
- Web Clip
- Certificate
- Passcode
- SCEP (iOS and Windows)
- Identity Certificate (dynamically generated)
- The name of a configuration or a policy type should be unique in a space. All other properties of a configuration or a policy can be cloned.
- The configurations will be cloned to all spaces which you, the administrator, have access to. You do not need to be a Global Administrator to clone a configuration.

## Clone a configuration or a policy

**Procedure**

1. Go to **Configurations** or **Policies** depending on what you want to clone.
2. Click the link for the configuration or the policy to display the details.
3. Click the **Clone** icon.
4. In the pop-up window, enter a **Name** and optionally a **Description**.
5. Click **Next**.
6. Modify the configuration or the policy as per your requirements.
7. Click **Next**.
8. Configure the distribution.
9. Click **Done**.
