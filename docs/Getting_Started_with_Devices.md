---
title: Getting Started with Devices
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Managing devices**](./Getting_Started_with_Devices.md)
- [**Performing actions on a device**](./Getting_Started_with_Devices.md)
- [**Setting the time zone for a device**](./Getting_Started_with_Devices.md)
- [**Listing devices by criteria**](./Getting_Started_with_Devices.md)
- [**Displaying detailed device information**](./Getting_Started_with_Devices.md)
- [**Bulk assign or change users and custom attributes to devices**](./Getting_Started_with_Devices.md)
- [**Exporting devices to a CSV file**](./Getting_Started_with_Devices.md)
- [**Searching device logs**](./Getting_Started_with_Devices.md)

Each entry in the **Devices** page represents a mobile device that has been registered with Ivanti Neurons for MDM and lists important information about the device. The Devices list page displays devices with information such as:

- Name
- Email Address
- Phone #
- OS
- Device Type
- Status
- Last Check-In
- Violation Count
- Space
- Legal Owner (for Shared iPads)

The Wi-Fi IP address is reported to the Ivanti Neurons for MDM server. Any changes to IP address is reported at every check-in. GDPR-compliant IP address is available as an option in the device list page and in the device details page. This feature requires devices to be registered via Go 5.5 for iOS or later versions, and Go 72 or later versions for Android as supported by Ivanti Neurons for MDM.

As new GDPR fields (such as IP Address and eSIM ID) are added over Ivanti Neurons for MDM releases, the admins who have configured GDPR already need to edit the GDPR profile if they want to hide the new fields.

The equipment identifier (EID) shows up as an iOS attribute when a device list is exported to spreadsheet (CSV) format. The EID and mobile EID (MEID) (when present) are prefixed by an EID string or MEID string, respectively.

The Ivanti Neurons for MDM server cannot handle processing the same device with different client identifiers and registered across different tenants. The server can only handle the instance where it is the same device with different client identifiers and registered to the same tenant.

## Managing devices

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Go to **Devices**.
3. Select one or more devices.
4. Select an action from the **Actions** drop-down list.

The following table lists the actions that are available on the Devices page:

| **Category** | **Action**     |
| ------------ | -------------- |
| Common       | - Add to Group |

- AppConnect Unlock>
- Assign Custom Attributes
- [**Assign to User**](./Assigning_a_Device_to_a_new_user.md)
- Device Compliance Status Sync
- Disable Remote Desktop
- Enable Remote Desktop
- Enable/Disable Bluetooth
- [**Force Check-in**](./Forcing_a_device_to_Check-in.md)
- [**Lock**](./Locking_a_Device.md)
- Remove Custom Attributes
- Restart/Shutdown
- Device Compliance Status Sync
- [**Device Retire**](./Retiring_a_Device.md)
- [**Send Message**](./Sending_a_Message.md)
- Set Ownership
- [**Unlock**](./Unlocking_a_Device.md)
- [**Wipe**](./Wiping_a_Device.md) |
  \| iOS          | \* [**Assign to Legal Owner**](./Shared_iPad_devices_for_business.md) (Shared iPads only)
- Reinstall iOS System Apps
- Set Time Zone                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| macOS        | - Set macOS Auto Admin Password
- Set/Change Firmware Password
- Set/Change Recovery Lock                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Android      | \* Enter Kiosk Mode
- Exit Kiosk Mode                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
  \| Windows      | Scripts and Actions via Ivanti Bridge                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |

## Performing actions on a device

The Actions menu (ellipsis button) lets you perform various actions on a selected device.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Click a device name. The device details page opens.
:::

:::WorkflowBlockItem
Click the Actions (ellipsis) menu to perform one of the following device actions:

- Change Device Name
- Delete Device
- Edit Group Membership
- Enable/Disable Bluetooth
- Scripts and Actions via Ivanti Bridge
- Pull Ivanti Bridge Log
- [**Relinquish Ownership**](./Relinquishing_Ownership_of_a_Device.md)
- Request Debug Logs
- Restart/Shutdown Device
- Retire
- Set Ownership
- Set/Change Recovery Lock
- Wipe
- Device Compliance Status Sync
:::
::::

## Setting the time zone for a device

**Applicable to:** iOS 14.0+ and tvOS 14.0+ devices

This action does not require Location Services. The time zone device action is also displayed in the device details page of a device. Time zone changes made in the device will also reflect in the Ivanti Neurons for MDM server.

This device action triggers an error if the **Force automatic Date & Time** restriction is enabled in [**iOS Restrictions configuration**](./iOS_Restrictions.md).

**Procedure**

1. Select one or more devices.
2. Click **Actions&#x20;**>**&#xA0;Set Time Zone** for the selected devices.
3. Enter the timezone string in the Olson Time Zone ID format. For example, Pacific/ Midway.
4. Click **Set Time Zone.**

## Listing devices by criteria

You can use the Filters side navigation bar to search and view specific devices among the entire list of devices. Use the Space drop-down list to select all or specific spaces to view the devices and their related information. You can also search for devices using either the display version or the bundle version. The Devices page displays both bundle version and display version of devices.

When you navigate from the Device Group page and click the number that is listed under the **# of devices** column or from the **#Installed** column in the **App Inventory** page, a message is displayed indicating the name of the space for which the devices are listed in the page.

## Displaying detailed device information

Click the link in the Name column of an entry to display the Device Details page. The Device Details page contains several tabs organizing the following information:

- **Overview** - The following table lists all the details displayed on the Overview tab:

| Section name | Description       |
| ------------ | ----------------- |
| **General**  | - Device Location |

:::Paragraph{listStyleType="disc" indent="2"}
Manufacturer
:::

:::Paragraph{listStyleType="disc" indent="2"}
Wi-Fi MAC Address
:::

:::Paragraph{listStyleType="disc" indent="2"}
WiFi-IP Address (Android devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Network Tethered - (iOS devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Has Battery - (Only for macOS 13.3+)
:::

:::Paragraph{listStyleType="disc" indent="2"}
IP Address
:::

:::Paragraph{listStyleType="disc" indent="2"}
Public IP Address - Displays the device's IP address for Android or ChromeOS. If the device connects to a VPN or proxy server, it shows the proxy WAN IP address.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Model Number - (macOS 13.3+ and iOS 16.4+)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Serial number
:::

:::Paragraph{listStyleType="disc" indent="2"}
Alternative Serial Number (Android devices) - Manufacturer specific serial number applicable for Samsung devices in Device Admin or Device Owner mode.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Storage Usage - Used (except Windows) and available internal storage on devices
:::

:::Paragraph{listStyleType="disc" indent="2"}
Available Battery (Android) 
:::

:::Paragraph{listStyleType="disc" indent="2"}
Battery Status (Android) - Charging, Discharging, Full, and Not Charging
:::

:::Paragraph{listStyleType="disc" indent="2"}
Battery Estimated Charge Remaining (Windows)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Battery Estimated Runtime (Windows)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Update Available (macOS)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Available Update Name (macOS)
:::

:::Paragraph{listStyleType="disc" indent="2"}
OS Version
:::

:::Paragraph{listStyleType="disc" indent="2"}
OS Build Version
:::

:::Paragraph{listStyleType="disc" indent="2"}
Supplemental Build Version
:::

:::Paragraph{listStyleType="disc" indent="2"}
Supplemental OS/Version Extra
:::

:::Paragraph{listStyleType="disc" indent="2"}
Apple Silicon Device
:::

:::Paragraph{listStyleType="disc" indent="2"}
Firmware Version
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device Source
:::

:::Paragraph{listStyleType="disc" indent="2"}
Legal Owner
:::

:::Paragraph{listStyleType="disc" indent="2"}
Multi-User Mode
:::

:::Paragraph{listStyleType="disc" indent="2"}
Time Zone
:::

:::Paragraph{listStyleType="disc" indent="2"}
System Update (Android devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Zebra patch Version (Android devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Last Hotfix ID - (Windows devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Last Hotfix Installed On - (Windows devices)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
\| **Settings**                                         | \* Device Name
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device Identifier
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device GUID
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device Enrollment Device (Apple devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device Enrollment Enrolled (Apple devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Automated Device Enrollment Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
Automated Device Enrollment Enrolled
:::

:::Paragraph{listStyleType="disc" indent="2"}
User Enrollment Enrolled (Apple devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Registered Managed Apple ID (Apple devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device Groups
:::

:::Paragraph{listStyleType="disc" indent="2"}
Language
:::

:::Paragraph{listStyleType="disc" indent="2"}
MDM Device Identifiers
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device Client ID
:::

:::Paragraph{listStyleType="disc" indent="2"}
Client App version
:::

:::Paragraph{listStyleType="disc" indent="2"}
Client App BundleID
:::

:::Paragraph{listStyleType="disc" indent="2"}
Client Registered
:::

:::Paragraph{listStyleType="disc" indent="2"}
EAS Device Identifiers
:::

:::Paragraph{listStyleType="disc" indent="2"}
Activation Lock Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
Apple Declarative Management Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
Activation Lock Bypass Code
:::

:::Paragraph{listStyleType="disc" indent="2"}
Terms of Service
:::

:::Paragraph{listStyleType="disc" indent="2"}
Ownership
:::

:::Paragraph{listStyleType="disc" indent="2"}
iTunes Account Active
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device Location Service Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
Quarantined
:::

:::Paragraph{listStyleType="disc" indent="2"}
Sentry Blocked
:::

:::Paragraph{listStyleType="disc" indent="2"}
Access Blocked
:::

:::Paragraph{listStyleType="disc" indent="2"}
Compliance Action Blocked
:::

:::Paragraph{listStyleType="disc" indent="2"}
APNS capable
:::

:::Paragraph{listStyleType="disc" indent="2"}
Supervised Mode (iOS and macOS devices) - Identifies a supervised device. Device remains in direct control of the IT team. The supervised mode enables additional device capabilities (for example, field service deployments, retail point-of-sale devices), “loaner” devices used in hospitality and services, and devices shared among students in a classroom lab.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Wipe PIN - Click **View** to display the PIN.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Managed macOS Admin user (macOS devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device Encryption Status (macOS devices)\* FileVault Encryption Enabled
:::

:::Paragraph{listStyleType="disc" indent="3"}
Personal Recovery Key Used
:::

:::Paragraph{listStyleType="disc" indent="3"}
Institutional Recovery Key Used
:::

:::Paragraph{listStyleType="disc" indent="2"}
Bootstrap Token Available
:::

:::Paragraph{listStyleType="disc" indent="2"}
System Integrity Protection Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
Firmware Password\* Password
:::

:::Paragraph{listStyleType="disc" indent="3"}
Change Pending
:::

:::Paragraph{listStyleType="disc" indent="3"}
Command Status
:::

:::Paragraph{listStyleType="disc" indent="3"}
Allow Option ROMs
:::

:::Paragraph{listStyleType="disc" indent="2"}
Recovery Lock\* Password
:::

:::Paragraph{listStyleType="disc" indent="3"}
Recovery Lock Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
Firewall Settings (macOS devices)\* Firewall Enabled
:::

:::Paragraph{listStyleType="disc" indent="3"}
Block All Incoming
:::

:::Paragraph{listStyleType="disc" indent="3"}
Stealth Mode
:::

:::Paragraph{listStyleType="disc" indent="2"}
Application Firewall Status (macOS devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Firewall Status (Windows devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Last backup to iCloud (iOS devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Passcode Lock Grace Period (iOS devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Android ID
:::

:::Paragraph{listStyleType="disc" indent="2"}
Android Security Patch Level (Android devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Kiosk Mode (Android devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Android SafetyNet Attestation Type (Android devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Android Enterprise Capable (Android devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Android Work Enabled (Android devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Samsung SAFE Capable (Android devices)
:::

:::Paragraph{listStyleType="disc" indent="2"}
Android Work Managed Devices (Device Owner) Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
Android Work Profile on Company Owned Device Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
Anti-phishing native status
:::

:::Paragraph{listStyleType="disc" indent="2"}
Anti-phishing status
:::

:::Paragraph{listStyleType="disc" indent="2"}
Anti-phishing VPN status
:::

:::Paragraph{listStyleType="disc" indent="2"}
Android Managed Device with Work Profile
:::

:::Paragraph{listStyleType="disc" indent="2"}
Android Work Profile on Company Owned Device Lock Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
Help\@Work Available
:::

:::Paragraph{listStyleType="disc" indent="2"}
Zebra Capable
:::

:::Paragraph{listStyleType="disc" indent="2"}
Secure Apps Status
:::

:::Paragraph{listStyleType="disc" indent="2"}
Secure Apps Encryption Status
:::

:::Paragraph{listStyleType="disc" indent="2"}
Secure Apps Encryption Mode
:::

:::Paragraph{listStyleType="disc" indent="2"}
FCM Enabled
:::

:::Paragraph{listStyleType="disc" indent="2"}
MTD activation status |
\| **Windows Information Protection (Windows devices)** | - WIP
:::

:::Paragraph{listStyleType="disc" indent="2"}
App Locker Configured
:::

:::Paragraph{listStyleType="disc" indent="2"}
EDP Mandatory Settings                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
\| **Telephony&#x20;**&#x20;                                 | **Device Service Subscriptions**- Phone number
:::

:::Paragraph{listStyleType="disc" indent="2"}
Cellular Technology
:::

:::Paragraph{listStyleType="disc" indent="2"}
IMSI
:::

:::Paragraph{listStyleType="disc" indent="2"}
ICCID
:::

:::Paragraph{listStyleType="disc" indent="2"}
IMEI
:::

:::Paragraph{listStyleType="disc" indent="2"}
IMEI 2 - (Only on Android devices with dual SIM port. Applicable on Android 8.0 or higher)
:::

:::Paragraph{listStyleType="disc" indent="2"}
MEID
:::

:::Paragraph{listStyleType="disc" indent="2"}
Device Location
:::

:::Paragraph{listStyleType="disc" indent="2"}
Carrier
:::

:::Paragraph{listStyleType="disc" indent="2"}
Home MCC
:::

:::Paragraph{listStyleType="disc" indent="2"}
Home MNC
:::

:::Paragraph{listStyleType="disc" indent="2"}
Current Country Name
:::

:::Paragraph{listStyleType="disc" indent="2"}
Home Country Name
:::

:::Paragraph{listStyleType="disc" indent="2"}
Cellular Technology
:::

:::Paragraph{listStyleType="disc" indent="2"}
Roaming
:::

:::Paragraph{listStyleType="disc" indent="2"}
Current Operator
:::

:::Paragraph{listStyleType="disc" indent="2"}
Current MCC
:::

:::Paragraph{listStyleType="disc" indent="2"}
Current MNC
:::

:::Paragraph{listStyleType="disc" indent="2"}
Data roaming
:::

:::Paragraph{listStyleType="disc" indent="2"}
Voice roamingFor supported iOS devices, these properties are displayed for multiple eSIM active service subscriptions.**SIM Service Subscriptions**- Carrier Setting Version
:::

:::Paragraph{listStyleType="disc" indent="2"}
Carrier Setting Network
:::

:::Paragraph{listStyleType="disc" indent="2"}
Current MCC
:::

:::Paragraph{listStyleType="disc" indent="2"}
Current MNC
:::

:::Paragraph{listStyleType="disc" indent="2"}
eSIM Identifier
:::

:::Paragraph{listStyleType="disc" indent="2"}
ICCID
:::

:::Paragraph{listStyleType="disc" indent="2"}
IMEI
:::

:::Paragraph{listStyleType="disc" indent="2"}
Data Preferred
:::

:::Paragraph{listStyleType="disc" indent="2"}
Voice Preferred
:::

:::Paragraph{listStyleType="disc" indent="2"}
Label
:::

:::Paragraph{listStyleType="disc" indent="2"}
Label ID
:::

:::Paragraph{listStyleType="disc" indent="2"}
Phone Number
:::

:::Paragraph{listStyleType="disc" indent="2"}
SIM Slot
:::

:::Paragraph{listStyleType="disc" indent="2"}
Is Roaming
:::

:::Paragraph{listStyleType="disc" indent="2"}
Subscriber Carrier Network                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
\| **Azure Device Compliance**                          | \* Azure Device Identifier
:::

:::Paragraph{listStyleType="disc" indent="2"}
Azure Device Compliance Status
:::

:::Paragraph{listStyleType="disc" indent="2"}
Azure Client Status Code
:::

:::Paragraph{listStyleType="disc" indent="2"}
Azure Device Compliance Report Time
:::

:::Paragraph{listStyleType="disc" indent="2"}
Azure Intune Device User UPN                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
\| **Google BeyondCorp Device Compliance**              | - Device Identifier
:::

:::Paragraph{listStyleType="disc" indent="2"}
Compliance Status
:::

:::Paragraph{listStyleType="disc" indent="2"}
Compliance Report Time
:::

:::Paragraph{listStyleType="disc" indent="2"}
User                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
\| **Battery Information**                              | \* Battery Level - Displays current battery charge level as reported by the Android OS
:::

:::Paragraph{listStyleType="disc" indent="2"}
Battery Health Status - As reported by the Android, Mac, iOS, and iPad devices.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Battery Charging Status - As reported by the Android OS
:::

:::Paragraph{listStyleType="disc" indent="2"}
Battery Health Percentage (OEM Specific) - Battery health in percentage for supported device manufacturers such as Zebra devices
:::

:::Paragraph{listStyleType="disc" indent="2"}
Battery Manufacture Date (OEM) - Battery manufactured date for supported device manufacturers such as Zebra devices
:::

:::Paragraph{listStyleType="disc" indent="2"}
Battery Charge Cycles (OEM) - Number of cycles completed in total for supported device manufacturers such as Zebra devices                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
**Configurations** - Displays the details of the applied configurations For more information, see [**Working with Configurations**](./Working_with_Configurations.md).
:::

- **Installed Apps** - Displays the details of the applications that are installed on the device. The installation date of the current version of the installed app is displayed under the **App Reported Date** column. Search the installed apps for the device as follows:\* App Name
  - Bundle or Package IDThe app installation date of the devices coming out of quarantine is the date when the device is removed from quarantine.In the case of Android Enterprise devices, you can also view the installed apps usage details sorted by Day, Week, Month, or Year. To view these details, you must have selected the **Enable App usage data collection** option available in the **Configuration Setup** section, and then you can select **App Usage - Day**, **App Usage - Week**, **App Usage - Month**, **App Usage - Year** options to view the app usage details.
- **Available Apps** - Displays the details of the applications that are available for the device. Search the available apps for the device as follows:\* App Name
  - Bundle or Package IDIn the **App Configurations** column, when you select the **Configuration Name**, you will be directed to the app catalog’s **App Configuration** tab to review the app configuration options. If needed, you can modify the app configurations for the device on the **App Configurations Summary** page. For more information about configuring an app, see [**App Configuration**](./App_Configuration.md).In the **App Configurations** column, when you select the **Configuration Name**, you will be directed to the app catalog’s **App Configuration** tab to review the app configuration options. If needed, you can modify the app configurations for the device on the **App Configurations Summary** page. For more information about configuring an app, see [**App Configuration**](./App_Configuration.md).Make sure to remember the specific app configuration's name and type for the assigned device on the **App Configurations** page.The **Status** column indicates the application installation status on the device. The App installation status is captured only for managed applications. The application installation status for unmanaged apps is displayed as Not Installed. You must convert the application to Managed to view the correct installation status.
- **AppConnect Apps** - Details of the installed AppConnect apps.
- **Policies** - Details of the applied policies. For compromised devices, check the violation reason in the Violation column. If the device has been rooted, the system displays the reason shown in the **Violation** column:| Priority (1 = highest) | Violation                                                   |
  \| ---------------------- | ----------------------------------------------------------- |
  \| 1                      | Plugin compromised                                          |
  \| 2                      | Client tampered                                             |
  \| 3                      | Unknown device manufacturer: unknown                        |
  \| 4                      | Suspicious folder detected: \[path]                         |
  \| 5                      | Suspicious binary found at: \[path]                         |
  \| 6                      | Folder /data is browsable OR Folder /data/data is browsable |
  \| 7                      | Found /system/app/Superuser.apk                             |
  \| 8                      | Package manager compromised                                 |
  \| 9                      | Suspicious app found: \[package]                            |
- **Certificates** - details of the installed certificates.For the usage of the certificate, check the Usage Type column. If the certificate is device specific,it displays the usage type as 'device'. If the certificate is user specific, it displays the usage type as 'user'.
- **Sentry** - Sentry information (ActiveSync associations)
- **Attributes** - Custom Attributes and Device attributes
- **Users** - Displays the list of active users for supervised MacOS device.**Users** tab is enhanced and shows the managed apple id as a hyperlink, clicking which redirects to user account details page in a Shared iPad device.
- **Logs** - View and customize device filters. You can do the following from the Filters:\* Select the Action name to filter devices based on application actions.
  - Select Status.
  - Specify the Start Date and the End Date.
- **Hardware** - Hardware inventory details (system, motherboard, BIOS, hard drive, CD ROM, processor and physical memory)

## Bulk assign or change users and custom attributes to devices

You can use the Bulk Assign via Upload icon to upload a CSV file to assign or change users and/ or custom attributes to devices in bulk.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
From the Devices page, click the **Bulk Assign via Upload** icon (next to the Actions button).
:::

:::WorkflowBlockItem
(Optional) Click **Download template** to save a CSV template file that you can edit and upload.
:::

:::WorkflowBlockItem
After the CSV file is ready, click **Choose File** to browse to the CSV file location or drag and drop the CSV file to the File data section.
:::

:::WorkflowBlockItem
Select one of the following options:
:::

:::WorkflowBlockItem
- **Force assign (overwrite) all attributes even if any existing values are found**
- **Overwrite only if value is empty, and skip attributes with existing values**
  Click **Upload**.
:::
::::

## Exporting devices to a CSV file

You can export the device details of a specific device using the **Export to CSV** option from the **Devices** page.

**Procedure**

1. Go to **Devices**.
2. Select all or multiple spaces to view the information related to specific spaces.
3. Click the devices count link. The Devices list page related to the selected space is displayed.
4. Click the **Export to CSV** option to export the devices list and related details to a CSV file. A pop-up message appears that the export report would take some time to process. Wait for the request to complete before you submit another request. Once the report is ready, you will be prompted with a message to either Download or Delete the report.
5. Click **Download**. You will also receive an email containing a link to download the report.
6. (Optional) Click **Delete&#x20;**&#x74;o delete the report.

## Searching device logs

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Devices&#x20;**>**&#x20;Devices**, click the **Name** column link of an entry.
:::

:::WorkflowBlockItem
Click the **Logs** tab.
:::

:::WorkflowBlockItem
Use the Action, Status, Start Date, and End Date filters to narrow the displayed devices. You can do the following from the Filters:1) Select the Action name to filter devices based on application actions.
2\) Select Status.
3\) Specify the Start Date and the End Date.
:::

:::WorkflowBlockItem
The Device Details column displays the status of the application as follows\:For all devices the status shows the following details:\* App name, app version, bundle, or package ID

- Status of installation
- Any errors and reason for the errorFor example - appOrConfigName=Name:\<app name>;Identifier=\<bundleid>;iTunesStoreId:\<itunesid>;Status:\<status or error reason from Apple>version: \<app version>

For Windows devices the status shows the following details:

- Include bundle ID or package ID, status, and errorsFor example -
- For type - application inventory and status - acknowledge - displays - appType
- For type - application inventory and status - sending - Does not display anything
- For  type - install/uninstall and status - success/failure/sending - displays Include bundle ID or package ID, status, name, version, and errors
:::
::::

If you cannot see the **Devices** page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- Device Management
- Device Read Only
