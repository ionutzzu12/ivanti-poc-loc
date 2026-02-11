---
title: Device Enrollment
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Device Enrollment is part of Apple Business Manager that enables customers to purchase devices in bulk and automatically enroll these devices in MDM during activation. If you choose to participate, you can use Ivanti Neurons for MDM as the MDM server for managing these devices. For more information, see [**https://business.apple.com/**](https://business.apple.com/).

## Connecting Ivanti Neurons for MDM to Device Enrollment

To use Ivanti Neurons for MDM as the MDM server for Device Enrollment, setup Apple Business Manager server token in Ivanti Neurons for MDM.

For each Apple Business Manager server, the following actions are available in Ivanti Neurons for MDM:

- Test Connection
- Add Device Enrollment Profile
- Download Public Key
- Device Enrollment Full Sync - Initiate full sync. It may take some time to be completed. After the sync is completed, you can view the information in the Last Sync column. You cannot initiate the full sync if it is already in progress.
- Upload New Token
- Delete

The **Edit Authentication** and **Assign Device Enrollment Device Attribute** actions are now available for device enrollment profiles instead of device enrollment (MDM server).

Procedure

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Admin** > **Apple** > **Device Enrollment**.
:::

:::WorkflowBlockItem
Click **Download Key**.
:::

:::WorkflowBlockItem
Save your Ivanti Neurons for MDM key.
:::

:::WorkflowBlockItem
Click **business.apple.com**.
:::

:::WorkflowBlockItem
Sign in using your Device Enrollment-eligible Apple credentials.
:::

:::WorkflowBlockItem
On the Apple Device Enrollment site:
:::

:::WorkflowBlockItem
1. Click **Get Started**.
2. Select the trusted phone to use for authenticating to Apple service.
3. Enter the verification code sent to the selected phone.
4. Click **Add MDM Server**.
5. Enter a name to identify the virtual MDM server to be used with the service.
6. Click **Next**.
7. Upload the public key you downloaded earlier.
8. Click **Next**
9. Click **Your Server Token** to download the token.
10. Click **Done**.
    In Ivanti Neurons for MDM, click **Upload**.
:::

:::WorkflowBlockItem
Click **Next**.
:::

:::WorkflowBlockItem
Select an authentication option:\* **Prompt user for registration / login**Does not support devices operating with visionOS platform. Instead, use **Skip User Login** to enroll a device.Users will be prompted for a username and password. Users can enter either a password or a PIN for the password field. For macOS 15+ devices, additional options such as **Face ID**, **Touch ID**, or **security key** are also available for iDP users on passkey-supported identity providers. Password and PIN preferences can be configured in **Users** > [**User Settings**](./User_Settings.md) related to authentication.

- **Skip user login**Devices assigned to the nobody user (anonymous) or a defined user can be reassigned to specific users at a later time from the **Devices** page.Select one of the following options:\* **Define one user to assign all devices to**
  - **Assign all devices to an anonymous user**
:::

:::WorkflowBlockItem
The selected option overrides the selections under [**User Settings**](./User_Settings.md).

Click **Upload** to install the key you received in Step 3.
:::

:::WorkflowBlockItem
Complete the displayed form to define the profile for your Device Enrollment devices:
:::

:::WorkflowBlockItem
| **Setting**     | **What To Do**                                                                                                                                                                                                                                                                                          |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name            | Enter a name that identifies this Device Enrollment profile.                                                                                                                                                                                                                                            |
| Description     | Enter a description for the profile.                                                                                                                                                                                                                                                                    |
| Department      | Enter the department in your organization that is associated with this profile.                                                                                                                                                                                                                         |
| Supervised Mode | Enables additional administrative control over configurations and restrictions. For iOS 13+ and macOS 10.15+ devices, this option is enabled by default.                                                                                                                                                |
| iOS 17+         | - **Require minimum OS version for enrollment**: Admin can set a minimum required OS version for devices enrollment. If device does not meet the minimum OS version criteria, the system prompts the user to upgrade to the required version. If the user denies to upgrade, the enrollment is blocked. |

- **Minimum iOS**: If the build version is not consistent with the OS version specified in the '**OSVersion**' key, the OS version will take precedence.
- **Minimum Build version**: If the build version is not consistent with the OS version specified in the **'OSVersion**' key, the OS version will take precedence.This field is optional, if you enter incorrect build number
- **Message**: A description of the error suitable for displaying to the user. If needed,\* the client will make a best-effort attempt to display the message, but may not
  - be able to, due to local conditions.As a practice the message should be added.
- **Beta Programs for iOS**: Enforces beta software versions on iOS during Automated Device Enrollment.       |
  \| macOS 14+                                      | \* **Require minimum OS version for enrollment**: Admin can set a minimum required OS version for devices enrollment. If device does not meet the minimum OS version criteria, the system prompts the user to upgrade to the required version. If the user denies to upgrade, the enrollment is blocked.
- **Minimum macOS**: If the build version is not consistent with the OS version specified in the '**OSVersion**' key, the OS version will take precedence.
- **Minimum Build version**: If the build version is not consistent with the OS version specified in the **'OSVersion**' key, the OS version will take precedence.This field is optional, if you enter incorrect build number
- **Message**: A description of the error suitable for displaying to the user. If needed,\* the client will make a best-effort attempt to display the message, but may not
  - be able to, due to local conditions.As a practice the message should be added.
- **Beta Program for macOS** : Enforces beta software versions on macOS during Automated Device Enrollment. |
  \| Automatically download and install iOS updates | (iOS 9.0+ only) If the Automatic Downloads option is selected on the device under **Settings > iTunes & App Store**, the OS updates will be automatically downloaded, but not installed, even when the Device Enrollment Profile option is turned off.This setting will take preference when there is an iOS Software Updates configuration applicable to the Device Enrollment-enrolled supervised devices.Any change in this setting will be applicable to the Device Enrollment-enrolled supervised device even without reset of the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| MDM Removable                                  | Defines whether the user will be unable to unenroll from MDM after the device is registered.This setting is not applicable to [**Shared iPads**](./Shared_iPad_devices_for_business.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| MDM Mandatory                                  | Defines whether the user will be unable to skip installing MDM during the activation process. For iOS 13+ and macOS 10.15+ devices, this option is enabled by default.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Allow Pairing                                  | (Not applicable for iOS 13+ and macOS 10.15+) Allows host pairing functions, such as iTunes sync.Pairing is always allowed for hosts that have valid pairing certificates.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| Certificate                                    | Click **+ Add** to upload certificates.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Support Phone Number                           | Provide a phone number that device users can contact for help.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  \| Support Email Address                          | Provide an email address that device users can contact for help.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| Custom Enrollment                              | (iOS 13.0+ and macOS 10.15+) Create custom enrollment web page(s). Specify your own custom web page (web view) to authenticate users during Device Enrollment.Use this page to display custom information such as authentication type, branding, consent text, and privacy policy.See the "*Adding a custom Device Enrollment web page*" section following this procedure for more details.\* Select **Enable Custom Enrollment** to enable this feature.
- Enter the **URL**, such as [**https://mycustomweburl.com**](https://mycustomweburl.com). This URL defines the value of the custom URL to present to the user in a web view.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \| Multi-User                                     | (iOS 13.4+) Shared iPad for businessEnables businesses to share devices between multiple employees, while still providing a personalized experience.Select **Multi-User Mode** to enable Shared iPad on a device. For more information, see [**Shared iPad for business.**](./Shared_iPad_devices_for_business.md)\* This setting is not applicable to Apple Education.
- Select the **Supervised Mode** setting to modify the Multi-User setting.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| Quota Size                                     | (iOS 13.4+) Shared iPad for Business.The value is in megabytes (MB) which denotes the storage allocated for a user in a device.If the value is too small, a default quota size is allocated by the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| Resident Users                                 | (iOS 13.4+) Shared iPad for BusinessThe value denotes the number of users that can be persisted or residing on the device. If the value is greater than the value of maximum number of users that the device supports, MDM server uses that value (maximum number of users) as a default.Administrators can provide either Quota Size or Resident Users value. If both values are provided, MDM server uses Quota Size as default.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| User session timeout                           | (iOS 14.5+) Shared iPad for BusinessShows the timeout in seconds for a user session. The user session logs out automatically after the specified period of inactivity. The minimum value is 30 seconds. Setting this value to 0 removes the timeout and sets to device default timeout.Value from 1 to 29 is invalid. When set, the device is set to default timeout.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \| Temporary Session Timeout                      | (iOS 14.5+) Shared iPad for BusinessShows the timeout in seconds for a guest or temporary session. The temporary session logs out automatically after the specified period of inactivity. The minimum value is 30 seconds Setting this value to 0 removes the timeout and sets to device default timeout.Value from 1 to 29 is invalid. When set, the device is set to default timeout.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Temporary Session Only                         | (iOS 14.5+) Shared iPad for BusinessIf true, the user only sees the Guest Welcome pane and can only log in as a guest user.If false, the user can sign in with a managed Apple ID (the existing behavior).Default: false                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| Managed Apple ID Default Domains               | (iOS 16.0+) Shared iPad for BusinessSpecify a list of domains. Users can select their account domain from the list of domains in the QuickType keyboard.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| Online Authentication Grace Period             | (iOS 16.0+) Shared iPad for BusinessSpecify the number of days the user can login without connecting to the network.Setting this value to zero enforces online authentication every time.**Default**: 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Auto Lock Time                                 | (iOS 17.0+)Specify the time (in seconds) after which the device goes to sleep mode. Minimum value is 120 sec.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
  \| Passcode Lock Grace Period                     | Specify the time (in seconds) after which the device user must enter the device passcode to unlock it. Min value is 0 sec and max value is 14400 sec.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \| Time Zone                                      | Specify the timezone the device must belong to.**Example**: Pacific/Midway                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  Define which steps may be skipped by the user during device activation for the following setup options:.
  \| **Setup Options**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
  \| - Skip Entering Passcode - Selecting this will auto enable Skip Apple Pay setup and Skip Touch ID.
- Skip Location Services
- Skip Restore From Backup
- Skip "Move to iOS" From Android
- Skip Terms Of Service
- Skip Signing In To Apple ID And iCloud - Selecting this will auto enable Skip Apple Pay setup.
- Skip Touch ID Setup (iPhone 5s, 6, 6+, iPad Air 2, iPad Mini 3 only) - Selecting this will auto enable Skip Apple Pay setup.
- Skip Apple Pay Setup (iPhone 6, 6+, iPad Air 2, iPad Mini 3 only)
- Skip Zoom Setup
- Skip Siri
- Skip intelligence (iOS 18+ and macOS 15+)
- Skip automatically sending diagnostic information
- Skip Cloud Storage (iOS 10.3+ & macOS 10.13.4+)
- Skip Display Tone Setup(iOS 9+ & macOS 10.14+)
- Skip Home Button Sensitivity
- Skip the keyboard selection screen
- Skip on-boarding informational screens - This information is for user education. For example: Cover Sheet, Multitasking & Control Center.
- Skip the screen for Apple Watch migration
- Skip Choose Your Look screen (iOS 13.0+ & macOS 10.14+)
- Skip Screen Time (iOS 12.0+ & macOS 10.15+)
- Skip Privacy (macOS 10.13.4+ & tvOS 11.3+)
- Skip Software Update (iOS 12.0+ & macOS 15.4+)
- Skip Add Cellular Plan Pane (iPhone Xs, iPhone Xs Max, iPhone XR)
- Show custom text on the Login page - Select this option to enter a custom text message in the text box. This message will be displayed on the login page on the device during the Device Enrollment setup to provide any additional instructions to end-users to help them through the process.
- Auto advance setup - Select this option to setup assistant to automatically advance through the device setup screens. The default is set to false. Supported on tvOS and macOS 11 and later. Auto advance setup does not work on a WiFi connection, the device should be connected over an ethernet.
- Terms Of Address- Skips the Terms of Address pane. (iOS 16+) |
  \| **iOS**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
  \| \* Skip Get Started pane (13.0+)
- Skip iMessage & FaceTime (12.0+)
- Skip Spoken Language (13.0+)
- Skip Restore Completed (14.0+)
- Skip Update Completed (14.0+)
- Skip Safety (16.0+)
- Skip Web Content Filtering Pane (18.2+)
- Skip Safety & Handling Pane (18.4+)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  \| **macOS**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| - Skip iCloud Analytics screen
- Skip True Tone Display screen (macOS 10.13.6+) - (Optional) Select this option to skip the True Tone Display window.
- Skip Accessibility (macOS 11.0+)
- Skip Unlock with Watch (macOS 12.0+)
- Skip Enable Lockdown Mode (macOS 14.0+)
- Skip Wallpaper Selection (macOS 14.1+)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| **tvOS**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  \| \* Skip Apple TV home screen layout sync screen
- Skip the Apple TV provider sign in screen
- Skip Tap To Setup Option
- Skip The Aerial Screensaver Setup                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| **macOS account setup assistant options**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| - Skip admin account creation
- Skip Primary Setup Account Creation
- Create primary accounts as regular users (as admin if not checked)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  \| Await Device Configuration during Device Enrollment Setup                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| \* Wait until configurations and high priority applications are pushed to devices - Select to push the configurations and high priority applications to the device before continuing with the remaining Device Enrollment setup screens. This setting will prevent the end-user from using the device before the required configurations and high priority applications are pushed to the device.
- Time Limit - Default time limit is 3 minutes. Maximum time is 10 minutes.To enable this feature, select the **Supervised Mode** option while editing the Device Enrollment profile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  Click **Save**.The following table is populated in the **Admin** > **Apple** > **Device Enrollment** page:| **Setting**                                                                                                                         | **What To Do**                            |
  \| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
  \| **Name**(Click on column heading to sort alpha-numerically.)Use the Search field to search for items from this column               | MDM server name                           |
  \| **Apple Account Name**(Click on column heading to sort alpha-numerically.)Use the Search field to search for items from this column | Managed Apple ID                          |
  \| **Number of Devices**                                                                                                               | Assigned devices count                    |
  \| **Enrollment Profile(s)**                                                                                                           | Assigned device enrollment profiles count |
  \| **Last Sync**(Click on column heading to sort alpha-numerically.)                                                                   | Last contacted time                       |
  \| **Token Expires**(Click on column heading to sort alpha-numerically.)                                                               | Token expiry date                         |
:::
::::

- When new devices are added to Apple Device Enrollment, it might take up to 15 minutes for Ivanti Neurons for MDM to discover those new devices. The new devices are then assigned an enrollment profile. If you cannot add new devices to the Device Enrollment go to **Dashboard > Notifications** to check for notifications from Apple for Device Enrollment. If there are any updates to the EULA you will notified by email with steps to accept the new EULA.
- You can view all the custom device attributes that exist in your tenant and assign them to the devices during their enrollment via Apple Device Enrollment.
- In shared macOS devices, the ListUsers command shows a list all local users on the device and only the last check-in details of the user who registered the device.

## Editing the Device Enrollment profile

Procedure

1. Go to **Admin** > **Apple** > **Device Enrollment**.
2. Find the name of the Apple Business Manager server (you created on the Apple site) in the Apple Account Name column.
3. Click the number link in the Enrollment Profile(s) column.
4. For a specific profile, select **Actions** > **Edit Device Enrollment Profile**.
5. Update and save the profile.

- If a Device Enrollment profile is edited, the device count of the modified profile will be updated shortly.
- If you refresh the server token on Apple site, then the existing token will become invalid. However, the display in the Device Enrollment page, including the token expiration date, will remain until you upload the new token.

The Device Enrollment Profile contains the following details:

| **Setting**                                                                  | **What To Do**                                                                  |
| ---------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Profile Name**(Click on column heading to sort alpha-numerically.)         | Enter a name that identifies this Device Enrollment profile.                    |
| **Description**(Click on column heading to sort alpha-numerically.)          | Enter a description for the profile.                                            |
| **Department**(Click on column heading to sort alpha-numerically.)           | Enter the department in your organization that is associated with this profile. |
| **Support Phone Number**(Click on column heading to sort alpha-numerically.) | Provide a phone number that device users can contact for help.                  |
| **Number of Devices**                                                        | Displays the number of devices for the profile                                  |
| **Actions**                                                                  | Manage profiles                                                                 |

## Managing multiple Device Enrollment profiles

You can create multiple Device Enrollment profiles against each Apple Business Manager server. This way, different sets of devices can receive different configurations. Devices can also be moved from one Device Enrollment profile to another.

Procedure

1. Go to **Admin** > **Apple** > **Device Enrollment**.
2. Find the name of the Apple Business Manager server in the Apple Account Name column.
3. Click the number link in the Enrollment Profile(s) column.
4. To create a new Device Enrollment profile to be associated with the selected server, click **Create New Profile**. Create and save the profile.
5. To manage each profile, click **Actions** and select one of the following options:\* **Set as Default Profile&#x20;**- Set the profile as the default profile within same virtual server. New device registrations will receiving this default profile.
   - **Edit Profile&#x20;**- Update existing profile.
   - **Edit Authentication** - Edits Device Enrollment authentication setting.
   - **Assign Device Enrollment Device Attribute** - Administrators use custom attributes for devices to associate additional properties with these objects. These properties can then be used to build groups or distribute configurations.
   - **Delete&#x20;**- The default profile cannot be deleted. When a non-default profile is deleted, all the associated devices will be re-assigned to the default profile.
6. To move an enrolled device to from one profile to another within the same virtual server (and not between different Apple Business Manager servers), click the number link under the Number of Devices column. The reassignment of profiles are applicable to devices that are yet to be enrolled.1) To move a single device, click **Assign Enrollment Profile** for the specific device, select the profile from the drop-down list, and click **Assign**.
   2\) To move multiple devices, select the devices and click **Actions** >&#x20;**&#xA0;Assign Enrollment Profile**, select the profile from the drop-down list, and click **Assign**.

- If a Device Enrollment profile is edited, the device count of the modified profile will be updated shortly.
- If you refresh the server token on Apple site, then the existing token will become invalid. However, the display in the Device Enrollment page, including the token expiration date, will remain until you upload the new token.

## Adding a custom Device Enrollment web page

**Applicable to:** iOS 13.0 and macOS 10.15 and supported newer versions

In the Custom Enrollment section, you can specify your own custom web page (web view) to authenticate users during Device Enrollment. Use this page to display custom information such as authentication type, branding, consent text, and privacy policy.

Procedure

1. Go to **Admin** > **Apple** > **Device Enrollment**.
2. Find the name of the server you created on the Apple site.
3. Select **Actions** > **Edit Device Enrollment Profile**.
4. In the Custom Enrollment section, select **Enable Custom Enrollment**.
5. Select one of the following options:\* **MobileIron Hosted webpage** - redirected to an Identity Provider (IDP) if the enrollment is using an identity provider such as Microsoft Active Directory Federation Services (ADFS) or Okta. This can also be redirected to the self-service portal for a Ivanti Neurons for MDM user with a non-IDP based authentication.
   - **Custom URL** - enter a URL such as [**https://mycustomweburl.com**](https://mycustomweburl.com). This URL defines the value of the custom URL to present to the user in a web view loaded during the initial setup of a new Device Enrollment device or an erased device. Use this field to define your own authentication UI with authentication method. After the user is authenticated, the MDM enrollment profile is downloaded.

### Workflow of the custom Device Enrollment web page

This section elaborates the behavior of the custom Device Enrollment web page and the procedure to create the custom web page (web view).

When the custom web page specified in the **URL** field loads initially:

- The configuration web URL has an **https** scheme and is a **GET** request. The web page should use a publicly trusted certificate.
- A custom header **x-apple-aspen-deviceinfo** is appended to the GET request by the Apple device on which enrollment is initiated. It contains a base64 encoding of a CMS (Cryptographic Message Syntax) envelope that contains a plist with device attributes. This is the same information, in the same format, as provided in the initial POST request with token-based device enrollments.

When the custom web page loads subsequently:

- The device user interacts with the web page (web view) until the administrator's host server provides a **custom.mobileconfig** file to the client. The Ivanti Neurons for MDM server returns byte code of the MDM profile. In the administrator's host server, the custom.mobileconfig file should be set with a MIME type of **application/x-apple-aspen-config** so that the MDM profile for the device is downloaded and installed on the device.
- For authentication with Ivanti Neurons for MDM, the web page should contain the authentication user name and password credentials. It is recommended to create a separate user in Ivanti Neurons for MDM and assign Custom Enrollment role to the user fetching the MDM profile with the Ivanti Neurons for MDM server URL (for example, [**https://micloudDomain.com/c/i/dep/custom.mobileconfig**](https://micloudDomain.com/c/i/dep/custom.mobileconfig)).
- For device registration and to get the MDM profile from Ivanti Neurons for MDM, the administrator's host web server should make a POST call to the Ivanti Neurons for MDM server URL. It should also pass the header x-apple-aspen-deviceinfo with the value provided by the device when the device hits the GET URL to load the custom web page. If the registration user ID is not provided, the device is registered to the nobody user. Here are the additional details:\* When a device hits the custom web URL configured in the Device Enrollment profile, administrator's host web server should capture the header "x-apple-aspen-deviceinfo" presented by the device.
  - To get the MDM profile for that device and its related user, administrator's host web server should make a POST call to the Ivanti Neurons for MDM server URL with the header x-apple-aspen-deviceinfo. It should contain basic authentication using a Ivanti Neurons for MDM user ID as a request parameter (for example, [**https://miCloudDomain.com/c/i/dep/custom.mobileconfig?user=name@company.com**](https://miCloudDomain.com/c/i/dep/custom.mobileconfig?user=name@company.com)). The user should be assigned the Custom Enrollment role.
  - After the administrator's host web server receives the byte code, it should download the byte code to the device by setting response headers, Content-Disposition = attachment;filename="profile.mobileconfig" and Content-Type = application/x-apple-aspen-config.
- The web view closes and the OS attempts to install the profile, which must be an MDM enrollment profile.

Ivanti Neurons for MDM does not authenticate the user ID for which the MDM profile is returned. Therefore, administrators should perform the necessary authentication for the user ID before requesting for the MDM profile.

For iOS, this workflow is supported during initial setup of an erased device. For macOS, this workflow is supported both within Setup Assistant and also via the Profiles preference pane, if Device Enrollment was skipped during Setup Assistant.

For developer information related to creating a custom web page, see the following Apple documentation references:

- [**Web Views**](https://developer.apple.com/design/human-interface-guidelines/ios/views/web-views/)
- [**Authenticating Through Web Views**](https://developer.apple.com/documentation/devicemanagement/device_assignment/authenticating_through_web_views)
- [**Sample code to implement a simple iPad web browser that can view either the desktop or mobile version of a website**](https://developer.apple.com/documentation/webkit/viewing_desktop_or_mobile_web_content_using_a_web_view)

## Editing the Device Enrollment authentication setting

Procedure

1. Go to **Admin** > **Apple** > **Device Enrollment**.
2. Find the name of the server you created on the Apple site.
3. Select **Actions** > **Edit Authentication**.

## Bootstrap token management for mobile accounts

**Applicable to:** macOS 10.15 devices and supported newer versions that are device enrolled in MDM using Apple School Manager or Apple Business Manager.

Ivanti Neurons for MDM supports bootstrap token management for mobile accounts. Bootstrap tokens enable mobile accounts to sign in to macOS devices that are using FileVault. Using this feature, all mobile accounts that log in get a SecureToken automatically. This feature is beneficial when multiple users log in to an encrypted machine.

When a managed admin account tries to login to a device:

- For the first login, the bootstrap token is requested from the MDM server.
- If the MDM server provides the bootstrap token, the device will create a SecureToken for the account automatically.
- The device enables FileVault for the user.

Bootstrap Token Available is a field available in the device details page and as a filter attribute while creating a new device group or a custom policy.

For troubleshooting and verification purposes, go to the device details page for a device. Use the Logs page to narrow the device logs using filters based on action names Set Bootstrap Token and Get Bootstrap Token.

## Setting up managed macOS admin account using Device Enrollment

Ivanti Neurons for MDM supports Device Enrollment registration on devices that have been reset to factory default or are being activated for the first time. Using Device Enrollment, an admin account can be created on the macOS device. Ivanti Neurons for MDM supports only optional enrollment for macOS and, therefore, Ivanti Neurons for MDM ignores the **MDM Mandatory** field in the Device Enrollment profile because it only applies to iOS devices.

Procedure

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Admin > Apple > Device Enrollment**.
:::

:::WorkflowBlockItem
Find the name of the server you created on the Apple site.
:::

:::WorkflowBlockItem
Select **Actions > Edit Device Enrollment Profile**.
:::

:::WorkflowBlockItem
Select one of the following options from the macOS account setup assistant options:
:::

:::WorkflowBlockItem
- **Skip admin account creation** - Select this option to disallow creating an admin account, either visible or hidden. Deselect this option to allow an admin account to be created in the **Set up Managed macOS Admin Account** section (described below).
- **Skip primary setup account creation** - Select this option to skip setting up the primary account on the macOS device. No user account is created besides an admin account. An additional section, **Set up Managed macOS Admin Account**, will be displayed (described below) to create the managed macOS admin account. The account can also be hidden from Users & Groups.
- **Create primary accounts as regular users (as admin if not checked)** - Select this option to create a non-admin standard account as part of the enrollment. An admin account can still be created by the Admin and pushed to the device. An additional section, **Set up Managed macOS Admin Account**, will be displayed (described below) to create the managed macOS admin account. The account can also be hidden from Users & Groups.
  After selecting one of the above options, enter the following details in the **Set up Managed macOS Admin Account** section if you want to create a managed macOS admin account:
:::

:::WorkflowBlockItem
- Full Name
- Account Name
- Password
- Confirm Password
- (Optional) Hide managed administrator account in Users & Groups
  If you do not select **Skip Primary Setup Account Creation**, enter the following details in the **Set up Primary Account** section. This adds user channel support for managed admin account by setting managed local user short name to an administrator's short name.- **Full Name**
- **Short Name**
- (Optional) **Prevent modification by end user** - This setting will be overriden if Full Name and/or Short Name have substitution variables and are evaluated empty. If you select this option, confirm you understand that this primary admin account setup is applicable only if one of below option is set appropriately:1) Prompt User Registration/Login is selected in the Authentication setup view.
  2\) MobileIron-hosted webpage is selected for Enrollment Customization.
:::

:::WorkflowBlockItem
Select **Skip Primary Setup Account Creation** to enable user channel support for managed admin account. You can set managed local user short name to an administrator's short name.
:::

:::WorkflowBlockItem
Click **Save**.
:::
::::

### Changing the local macOS admin account password

An administrator can change the local password of a local macOS admin account that was created by Setup Assistant during Device Enrollment.

**Applicable to:** macOS 10.11 or supported newer versions.

Procedure

1. Go to **Devices**.
2. Click the user name the device is associated with to view the device details page.
3. From the Actions menu, click **Set\*\*\*\*macOS Admin Password**.This action can be performed in Device List page as well by selecting one or more devices.
4. Enter the password.
5. Click **Save**.

## Export to CSV

Ivanti Neurons for MDM lets you export the Device Enrolled devices to a CSV file.

Procedure

1. Go to **Admin&#x20;**>**&#x20;Apple&#x20;**>**&#x20;Device Enrollment**.
2. Click the specific device count link under the **Number of Devices** column.
3. Click the **Export to CSV** option to export the devices list and related details to a CSV file. Once the report is ready, you will be prompted with a message to either Download or Delete the report. You will also receive an email containing a link to download the report.
4. Click **Download**.
5. (Optional) Click **Delete&#x20;**&#x74;o delete the report.
