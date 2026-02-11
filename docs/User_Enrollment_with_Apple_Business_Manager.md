---
title: User Enrollment with Apple Business Manager
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Requirements for enabling User Enrollment**](./User_Enrollment_with_Apple_Business_Manager.md)
- [**Priority of registrations**](./User_Enrollment_with_Apple_Business_Manager.md)
- [**Difference between standard MDM enrollment and User Enrollment**](./User_Enrollment_with_Apple_Business_Manager.md)
- [**Difference between User Enrollment vs Device Enrollment**](./User_Enrollment_with_Apple_Business_Manager.md)
- [**Connecting Ivanti Neurons for MDM to Apple Business Manager**](./User_Enrollment_with_Apple_Business_Manager.md)

**Applicable to**:

- Unsupervised devices with iOS 13.0 through the latest version as supported by Ivanti Neurons for MDM.
- Devices with macOS 10.15or supported newer versions Ivanti Neurons for MDM.

Apple Business Manager is a place for IT teams to automate device deployment, purchase and distribute content, and manage roles in their organizations. Apple Business Manager implements User Enrollment - an enrollment option designed for companies implementing BYOD (Bring Your Own Device). User Enrollment is a modified version of the MDM protocol with a much greater focus on user privacy, implemented with a level of security that enterprises need.

User Enrollment allows the administrator to do the following:

- Install and remove managed applications
- Install and remove network configurations
- Install a partial VPN scoped to managed apps and accounts
- Require the usage of a password

## Requirements for enabling User Enrollment

Below are the requirements for enabling User Enrollment. If any of them are not met, the enrollment type will be device enrolled.

- An unsupervised device with iOS 13.0 through the latest version as supported by Ivanti Neurons for MDM or a device with macOS 10.15or supported newer versions Ivanti Neurons for MDM.
- User setting for the Apple Enrollment Type field should be set as "User Enrollment."
- An Apple Business Manager account.
  - The Apple App License Account needs to be part of the same Apple Business Manager account.
  - Within Apple Business Manager, if you have an account listed in Locations, you need to have Apps and Books matched to the same location. You may need to add a new location (for example, West Coast).
    Managed Apple ID - Managed Apple ID to be associated with each enrolled device.
  - This Managed Apple ID provides authentication for MDM management and app licensing.
  - When the MDM pushes down apps and media, necessary Apple licenses are assigned to the Managed Apple ID associated with the device.
  - As part of GDPR compliance, Managed Apple IDs are masked in the user list and user details pages considering the Apple ID to be user data.
  - Managed Apple IDs were first utilized by Apple School Manager and are now utilized by Apple Business Manager for User Enrollment.
    The device's Managed Apple ID and Apps and Books Location token should be from the same Apple Business Manager account's Organization.
    If they are different, a notification is displayed in the Ivanti Neurons for MDM Admin Portal when the license allocation fails for an app.
    Microsoft Entra ID configured for Federated Authentication or an Apple ID created manually in Apple Business Manager with a validated domain.
  - For instructions on using Federated authentication, see the [**Apple Business Manager User Guide**](https://business.apple.com/) on the Apple website. A login is required.
    Device users who are synced to LDAP are to be assigned to a device management role and associated with a Managed Apple ID.

In the [**Users**](./Users.md) list page and the [**Devices**](./Devices.md) list page, you can add the Managed Apple ID column to be displayed for all users. In the [**Devices**](./Devices.md) list page, you can add the User Enrollment Enrolled column to display the status of User Enrollment devices. In addition, the user and device exports include these columns in CSV files.

## Priority of registrations

- User Enrollment is supported via Go for iOS client and iReg. Apple no longer supports User Enrollment through Ivanti Go for iOS and iReg. [**Account driven User Enrollment**](<Account driven User Enrollment.htm>) is only available in the Work or School account of the device.
- Automated Device Enrollment and Apple Configurator registrations will always be device enrolled.
- If MAM configuration is applied to a device, MAM registration takes precedence over User Enrollment.
- If both auth-only and User Enrollment requirements are met, User Enrollment takes precedence.
- If you Re-enroll a device from Go for iOS client, the enrollment type will be the same as the type during the device registration irrespective of the change in the enrollment type in Ivanti Neurons for MDM. For example, if a device was user enrolled, change the type to Device Enrollment in Ivanti Neurons for MDM, and Re-enroll the device from the Go client, the device will still be user enrolled and not device enrolled.

## Difference between standard MDM enrollment and User Enrollment

This section addresses the difference between standard MDM enrollment and User Enrollment with Apple Business Manager.

### Standard MDM enrollment

The following list indicates what a Ivanti Neurons for MDM server can do in a standard MDM enrollment, but will not be able to do in User Enrollment mode.

The MDM server:

- Cannot erase the device.
- Does not see the personal apps the device user has installed on the device.
- Cannot convert user-installed apps into MDM-managed apps.
- Cannot clear the device passcode (i.e. unlock the device).
- Cannot set a long, complex device passcode requirement.
- Cannot configure a device-wide VPN or Wi-Fi proxy, nor can it do any management of the cellular functionality.
- Cannot see device identifiers like the UDID, serial number, or IMEI.
- Cannot apply many device-wide restrictions (such as restricting the app content rating), block iCloud, and apply any the supervised restrictions.

### User Enrollment with Apple Business Manager

In User Enrollment, the MDM server can still do everything needed to manage enterprise apps, accounts, and data.

User Enrollment can:

- Install in-house apps or apps via user-based (Apple) Apps and Books licenses.
  - The licenses are applied on a first-come, first-served basis and are consumed by the Managed Apple IDs.
  - The license consumed by an app installed on the User Enrolled device will be different from the license consumed by the same app installed on the device enrolled device.
  - Check license type for Apple Apps and Books applications in a user details page via the License Usage tab - the Enrollment Type is displayed as User Enrollment or Device Enrollment.
    Enforce passcode payload settings. For example:
  - allowSimple = false
  - forcePIN = true
  - minLength = 6
    Query data related to enterprise-managed apps, certificates, and profiles.
- Configure a per-app VPN for apps, mail, contacts, and calendars that have been installed by MDM.
- Enforce some restrictions, like managed open in, managed contacts, managed data on the lock screen, and several others.

Enterprise data is stored in a separate Apple File System (APFS) volume, which is created at enrollment, and encrypted separately from device user data. This volume contains data stored by managed apps; enterprise Notes; enterprise iCloud Drive docs; enterprise Keychain entries; managed mail attachments and bodies; and calendar attachments. Un-enrolling from MDM destroys the volume and the keys.

All third-party apps can only be either a personal app or a managed app through Ivanti Neurons for MDM. The MDM service cannot start managing apps that the device user has already installed. In this case, the administrator will need to request the device user to delete the personal app before installing the app through MDM. The MDM service cannot start managing apps that the user has already installed. However, some system apps like Notes and Files will support both work and personal accounts.

### User Enrollment for macOS devices

User Enrollment is supported for devices with macOS 10.15or supported newer versions Ivanti Neurons for MDM.

- Mobile\@Work for macOS is not supported for macOS User Enrollment Enrolled devices.
  - Even if the app is distributed to the macOS User Enrollment Enrolled device, the app will not be pushed to the device from MDM.
  - Therefore, Mobile\@Work features such as script management and app management for the Packager (MIP) apps are not supported for macOS User Enrollment Enrolled devices.
    App dependency and behavioral changes in macOS User Enrollment Enrolled devices.
  - In macOS User Enrollment Enrolled devices, app dependency works on a best effort basis as the MDM is unaware of (cannot confirm) the installation status of prerequisite apps before distributing the main app.
  - Apps and configurations can be distributed to users and user groups that belong to macOS User Enrollment Enrolled devices. However, the apps always display the **Install** button instead of "Installed" because MDM cannot display the installation status of apps in macOS User Enrollment Enrolled devices.
  - Installed apps are indicated as Requested Apps in **Devices > App Inventory** page as the macOS User Enrollment Enrolled devices do not notify the Ivanti Neurons for MDM server whether the apps are installed or not installed in the inventory report.
    In the distribution filter for apps, User Enrollment Enrolled and Automated Device Enrollment Enrolled attributes can be used for custom distribution as required.
- User-based licenses are supported using managed Apple IDs to install Apple Apps and Books applications. Device-based licenses are not allowed. The app catalog only displays Apple Apps and Books applications.
- Not all configurations, policies, and actions are allowed. See full list of configurations and policies listed following this procedure.
  - If unsupported configurations are distributed to a macOS User Enrollment Enrolled device, they will not be distributed or applied to the device and may display a message such as "Restrictions - this is not a valid request type."
  - Similarly, unsupported admin device actions will be informed in Ivanti Neurons for MDM UI.
  - Unsupported reports will not be sent by Ivanti Neurons for MDM.

The following are the configurations and policies unsupported to be distributed to macOS User Enrollment Enrolled devices:

- Passcode
- Tunnel
- Tunnel (On Demand)
- VPN configurations
- Office 365 Auto Account Creation
- macOS Kernel Extension Policy
- Privacy Preference
- macOS Restrictions
- Software Updates
- AirPrint
- MI Client Privacy
- FileVault 2
- FileVault Recovery Key
- Firewall
- System Policy Rule
- Certificate Preference
- System Policy Control
- System Policy Managed
- macOS AppStore Restrictions
- macOS Disk Burning Restrictions
- macOS Finder Settings
- Mobile\@Work for macOS
- Mobile\@Work for macOS Script
- Allowed Media Control
- Time Server
- Allowed Apps Policy

## Difference between User Enrollment vs Device Enrollment

This section covers the difference between User Enrollment and device enrollment.

User Enrollment applies to devices with iOS 13.0 and macOS 10.15 through the latest version as supported. Devices lower than iOS 13.0 and macOS 10.15 will be considered “device enrollment” regardless of whether the device user has been enabled for User Enrollment or not.

User Enrollment for Apple Business Manager does not allow for wipe or unlock. However, the user portal will still have those options available even though they will not work.

| User Enrollment vs Device Enrollment                                                                                       |                                 |                                 |                                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------- | ------------------------------- | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Functionality                                                                                                              | User Enrollment                 | MAM                             | Device Enrollment                                                                                                                                                  |
| Erase the device and see user's personal apps                                                                              | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)     | ![](Resources/Images/Check.svg)                                                                                                                                    |
| Convert managed to unmanaged or vice versa                                                                                 | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)     | ![](Resources/Images/Check.svg)                                                                                                                                    |
| Clear device passcode, configure device-wide VPN or Wi-Fi proxy, or manage cellular functionality                          | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)     | ![](Resources/Images/Check.svg)                                                                                                                                    |
| See device identifiers like serial number, IMEI                                                                            | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)     | ![](Resources/Images/Check.svg)                                                                                                                                    |
| Apply supervised restrictions                                                                                              | ![](Resources/Images/X.svg)     | ![](Resources/Images/X.svg)     | :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/DpdcJ-ljWMFDNvIRnnSnw_check.svg" alt caption}(Supervised devices only) |
| Can install and configure apps and accounts                                                                                | ![](Resources/Images/Check.svg) | ![](Resources/Images/Check.svg) | ![](Resources/Images/Check.svg)                                                                                                                                    |
| Can configure a per-app VPN for apps, mail, contacts, and calendars that have been installed by MDM                        | ![](Resources/Images/Check.svg) | ![](Resources/Images/X.svg)     | ![](Resources/Images/Check.svg)                                                                                                                                    |
| Can enforce some restrictions, like managed open in, managed contacts, managed data on the lock screen, and several others | ![](Resources/Images/Check.svg) | ![](Resources/Images/X.svg)     | ![](Resources/Images/Check.svg)                                                                                                                                    |
| Can query data related to enterprise-managed apps, certificates, and profiles                                              | ![](Resources/Images/Check.svg) | ![](Resources/Images/X.svg)     | ![](Resources/Images/Check.svg)                                                                                                                                    |

## Connecting Ivanti Neurons for MDM to Apple Business Manager

This section covers enabling User Enrollment for Apple Business Manager.

**Prerequisites**

- You must have an Apple Business Manager account. See [**https://business.apple.com/**](https://business.apple.com/).
- You must request and install an Apple [**MDM certificate**](./Install_MDM_Certificate.md) to manage iOS devices.

### Creating local users to enable User Enrollment

This section covers creating local and LDAP users and setting the User Enrollment for unsupervised Apple devices. User Enrollment will not work on supervised devices or devices enrolled in Apple's Device Enrollment.

### Creating a manually managed (static) user group

This is a one time procedure. If you have already created this group, skip to the "Creating users for User Enrollment" section.

**Procedure**

1. Go to User&#x73;**>**[**User Groups**](./User_Groups.md).
2. Create a manually managed (static) user group, such as User Enrollment Group, to add users with device registration type as User Enrollment.
3. Click **Save**.

### Creating a device registration type setting

This is a one time procedure. If you have already created this group, skip to the "Creating users for User Enrollment" section. For User Enrollment Enrolled devices, the default Device Owner Settings will be "User Owned."

**Procedure**

1. Go to **Users >**[**User Settings**](./User_Settings.md).
2. In the Device Registration Setting section, click **+ Add setting for specific user groups**.
3. Create a new setting, such as UE Registration, for users with device registration type as User Enrollment.
4. In the Apple Enrollment section, select **User Enrollment** as the Apple Enrollment Type.
5. Click **Next**.
6. In the User Setting Distribution page, select the newly created user group, such as User Enrollment Group.
7. Click **Done**.

### Creating a local user for User Enrollment

As a prerequisite, create a manually managed user group and a device registration setting for User Enrollment.

**Procedure**

1. Go to [**Users**](./Users.md).
2. Click + **Add** > **Single User**.
   Enter the new user information and add it to the newly created user group, such as User Enrollment Group. For more information, see *Adding a user* in the [**Users**](./Users.md) topic.

### Importing LDAP users to enable User Enrollment

**Prerequisites**

- As a prerequisite, set up a Ivanti Neurons for MDM connector to access [**LDAP**](./Configuring_LDAP_server.md) resources.
- Ensure that the **Managed Apple ID** setting is set to **Pattern** (user email address). Ensure the pattern for Managed Apple ID is unique. Otherwise, the account will not be updated with the Managed Apple ID if the same Managed Apple ID exists in another account.
- (Optional) include "appleid" subdomain to avoid conflict with existing Apple IDs.
- You can import users from LDAP and invite them for User Enrollment. The imported LDAP users will have their Managed Apple IDs synced with Ivanti Neurons for MDM, which is a requirement for User Enrollment.

**Procedure**

1. Go to **Users**.
2. Click **+Add > Invite Users from LDAP**.
3. Click **Select Users** in the LDAP server entry.
4. In the Add LDAP Users page, enter the name of the user, group, or OU in the search field.
5. To add new users or groups, click **+Add** next to the entry you want to add.
6. Click **Done**.

### Importing Entra ID users to enable User Enrollment

As a prerequisite, connect Ivanti Neurons for MDM with Microsoft Entra ID (Entra ID).

You can invite Entra ID users for User Enrollment. The imported Entra ID users will have their Managed Apple IDs synced with Ivanti Neurons for MDM, which is a requirement for User Enrollment.

Procedure

1. Go to **Admin >&#xA0;**[**Entra ID User Source**](./Connect_Ivanti_Neurons_for_MDM_with_Entra_ID_User_Source.md).
2. Edit the settings.
3. Select **Enable this Entra ID**.
4. In the Managed Apple ID setting, select one of the following options:\* **Pattern**- **User email address** - Ensure the pattern for Managed Apple ID is unique. Otherwise, the account will not be updated with the Managed Apple ID if the same Managed Apple ID exists in another account.
   - Alternatively, select **userUPN**.
5. (Optional), include "appleid" subdomain to avoid conflict with existing Apple IDs.
6. Select **Automatically invite users imported from Entra ID**. Users imported from Entra ID to Ivanti Neurons for MDM are automatically invited to register via email.
7. Click **Save**.

### Device user instructions for registering using User Enrollment

This section addresses the actions the device user needs to take for registering Apple User Enrollment.

**Procedure**

1. On the iOS device you wish to register, open the invitation email that contains a link and text guiding the end user to a registration link such as mobileiron.com/go.
2. Open the registration link in Safari.
3. The login page displays. The device user is to log in using their local user or LDAP credentials.
   The registration page displays with a message saying the profile was downloaded.
   Tap Settings. The Settings page displays.
4. Tap Enroll in \[Your Company Name].
5. The User Enrollment page displays.
6. Tap Enroll My \[Your Device]. For example, tap Enroll My iPhone.
   If you tap Cancel and Delete Profile, you will have to start the registration process all over again.
   You will be presented with a login for either Apple or your Federated account. Enter the password for your Managed Apple ID. (The Managed Apple ID will be listed at the top of your login page.)
   You may be presented with the option to stay signed in, make a selection.
   A page displays the "Enrollment is Successful.”

### Using device logs for troubleshooting

To troubleshoot errors or issues for a User Enrolled device, start by reviewing the device logs.

**Procedure**

1. Go to Devices.
2. Click on the device to display the device details page. You can verify User Enrollment Enrolled and Registered Managed Apple ID fields.
3. Select the Logs tab.
4. In the Filters region, narrow the device logs using filters based on action names (such as Checkout, Device Name, Set Bootstrap Token, Get Bootstrap Token, and so on), status, start date, and end date.
5. In the Actions column, click the eye icon to display the device log details, such as Enrollment ID.
6. Click **OK**.
