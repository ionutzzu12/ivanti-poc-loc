---
title: Deploying Apple Devices
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM supports management for all your Apple devices. It is a comprehensive solution to provision, manage, update, and secure your fleet providing the end user with the best user experience.

This section contains the following topics:

- [**Installing your Apple MDM certificate**](./Deploying_Apple_Devices.md)
- [**Enrolling Apple Devices**](./Deploying_Apple_Devices.md)
- [**Ivanti Go for iOS Client**](./Deploying_Apple_Devices.md)
- [**Managing Applications for Apple Devices**](./Deploying_Apple_Devices.md)
- [**Managing Configurations**](./Deploying_Apple_Devices.md)
- [**Managing Software Updates**](./Deploying_Apple_Devices.md)
- [**Setting up iOS/iPadOS Devices**](./Deploying_Apple_Devices.md)
- [**Setting up watchOS Devices**](./Deploying_Apple_Devices.md)
- [**Supported device actions for watchOS Devices**](./Deploying_Apple_Devices.md)
- [**Setting up visionOS Devices**](./Deploying_Apple_Devices.md)
- [**Supported device actions for visionOS Devices**](./Deploying_Apple_Devices.md)
- [**Setting up macOS Devices**](./Deploying_Apple_Devices.md)
- [**Setting up TvOS devices**](./Deploying_Apple_Devices.md)
- [**Support for Declarative Device Management (DDM)**](./Deploying_Apple_Devices.md)

## Installing your Apple MDM certificate

To manage Apple devices, start by requesting and installing an Apple MDM certificate to manage iOS devices. Renew the Apple MDM certificate once a year. (The Apple account used for creating the certificate receives a notification from the Apple site when the expiration date approaches.) Use the MDM Certificate page to add or renew this certificate.

Follow steps described in [**Install MDM Certificate**](./Install_MDM_Certificate.md)

## Enrolling Apple Devices

You can choose any one of the following method to enroll devices:

- [**Automated Device Enrollment**](./Device_Enrollment.md)
- [**Apple School Manager**](./Apple_Configurator.md)
- [**Apple Configurator**](./Apple_Configurator.md)

## Ivanti Go for iOS Client

The next step is to select the enrollment type that your company allows for your devices. Ivanti Neuros for MDM currently supports:

- [**Device Registration (iOS, macOS, and Android)**](./Device_Registration__iOS__macOS__and_Android_.md)
- [**User Enrollment with Apple Business Manager**](./User_Enrollment_with_Apple_Business_Manager.md)
- [**Account driven User Enrollment**](<Account driven User Enrollment.htm>)
- [**Settings (Apple)**](./Settings__Apple_.md)

## Managing Applications for Apple Devices

The App Catalog page in Ivanti Neurons for MDM serves as an interface for administrators to govern their app catalog efficiently. This functionality encompasses the orchestration of mobile applications available to end-users, spanning both public app stores and those earmarked for distribution through Ivanti Neurons for MDM.

Supported Apps:

The App Catalog page aggregates various types of apps, including Public AppStore apps, Custom Apps, in-house developed apps, AppConnect-enabled apps, GoClient for iOS, and M\@W for macOS, streamlining the importation process for subsequent configuration and distribution.

On devices operating under Mobile Application Management (MAM)-Only configurations, iOS users are prompted to select an authentication certificate upon accessing the App Catalog. This authentication step is crucial for securing access to the listed apps and aligning with robust security practices.

M1 chipset MacBooks from Apple offer specialized support for iPhone and iPad VPP apps within \[Your Software Product]. Notably, only administrators have the authority to push supported iPhone and iPad VPP apps, restricting users from installing them directly from the App.

For detailed implementation instructions and configuration options, please refer to the comprehensive documentation available in the in the Admin guide and resources below:

- [**Managing Apps**](./Apps.md)
- [**App Catalog Settings**](./Catalog_Settings.md)
- [**Set up Apple Apps and Books**](./Apple_Apps_and_Books.md)
- [**Apps@Work Corporate App Store**](./Apps@Work__iOS__Android__Windows__and_macOS_.md)
- [**MacOS AppStore Restrictions**](./macOS_AppStore_Restrictions.md)

## Managing Configurations

Configurations are collections of settings that you as an administrator send to devices. For example, you can use configurations to automatically set up VPN settings and passcode requirements on the devices. The existing configurations for your system are listed in the Configurations page. You can select multiple configurations from the Configurations page and push them to multiple devices at once. These configurations can be pushed to devices specific to spaces and the devices in other spaces remain unaffected. Configurations can be pushed to either a single space or multiple spaces or all spaces at a time.

Most configurations in Ivanti Neurons for MDM are common to all platforms. For more details on how to work with configurations see Working with Configurations.

Some configurations are supported only by specific Platforms. You can review the list by platform supported on Configuration Types

## Managing Software Updates

You can start by setting up the Software Update configuration for your iOS and macOS devices.

When setting up a scheduled windows for the Software Update, the OS Update command will be pushed every hour to the device to make sure the update does not miss the window. As per Apple behavior every time the OS update command is received by the device a pop-up will notify the user to upgrade. User can defer up to three times. At the third time as per Apple behavior the Device will Force Upgrade.

MacOS devices have some specific rules that can be applied. See macOS Software Update Rules Configuration

### OS Update Command for iOS

You can also send a one time command to update to one or more devices from the Device List or from the Device Page. See Schedule OS Update Command.

## Setting up iOS/iPadOS Devices

The following configurations are supported for your iOS/iPadOS :

- [**iOS/iPadOS Restrictions**](./iOS_Restrictions.md)
- [**eSIM configuration**](./eSIM_Configuration.md)\* [**Preserve Data Plan**](./Wiping_a_Device.md)
- [**Mobile Network Configurations**](./Cellular_Network_Configuration.md)
- [**Enable Lost Mode**](./Managing_Apple_devices_in_lost_mode.md)
- [**Configuring an iOS MDM Profile**](./Configuring_an_iOS_MDM_Profile.md)
- [**Single App Mode**](./Configuring_Single_App_Mode_for_iOS.md)\* [**Autonomous Single App Mode**](./Create_Autonomous_Single_App_Mode_Configuration.md)
- [**Shared iPad for Business**](./Shared_iPad_devices_for_business.md)
- [**Education Configuration**](./Education.md)
- [**iOS Custom Configuration**](./iOS_Custom_Configuration.md)
- [**Lock Screen Message**](./Lock_Screen_Message_Configuration.md)

## Setting up watchOS Devices

You can now enroll Apple watchOS devices into Ivanti N-MDM while pairing with the iOS devices.

This feature currently supports: watchOS 10+.

ProcedureProcedure

1. You must enroll the iOS 17+ supervised device.
2. Assign the Apple Watch enrollment configuration to the iOS device.
3. You can now pair your Apple Watch to the iPhone.

You can pair the Apple Watch after pushing the Watch configuration to the iPhone. You cannot enable Remote Management for an Apple Watch if the Watch configuration is pushed to the iPhone after the Apple Watch pairs with it.

The following configurations are supported for your watchOS devices:

- [**Cellular\_Configuration**](./Cellular.md)
- [**Certificate configuration**](./Certificate_configuration.md)
- [**Certificate Transparency**](./Certificate_Transparency.md)
- [**Identity\_Certificate\_Configuration**](./Identity_Certificate.md)
- [**iOS Restrictions**](./iOS_Restrictions.md)
- [**Passcode\_Settings**](./Passcode_Configuration.md)
- [**Per-App\_VPN\_Configuration**](./Per-app_VPN_Configuration.md)
- [**Wi-Fi\_Configuration**](./Wi-Fi_Configuration.md)

## Supported device actions for watchOS Devices

The following device actions are supported for your watchOS devices:

- Clear passcode
- Lock Apple watch
- Wipe Apple watch
- Unenroll Apple watch from Ivanti Neurons for MDMUnenrolling paired iOS device will reset the watch and unpairs from the iOS device.

## Setting up macOS Devices

The following configurations are supported for your macOS:

- [**macOS Restrictions**](./macOS_Restrictions.md)
- [**Configuring macOS Devices**](./Configuring_macOS_devices.md)
- [**Working with Scripts and the Mobile@Work Client**](./All_Scripts.md)
- [**Configuring a macOS MDM Profile**](./Configuring_a_macOS_MDM_Profile.md)
- [**Setting Firmware Password**](./Setting_firmware_password.md)
- [**Enable FileVault**](./FileVault_2.md)\* [**FileVault Recovery Key**](./FileVault_Recovery_Key.md)
  - [**FileVault Options Configuration**](./FileVault_Options_Configuration.md)
- [**Platform and Extensible SSO**](./Single_Sign-On_Configuration.md)
- [**Active Directory macOS**](./Active_Directory__macOS_.md)
- [**Firewall**](./macOS_Firewall.md)
- [**Ethernet**](./Ethernet_Configuration__macOS_.md)
- [**Office 365 Account Creation**](./Office_365_Auto_Account_Creation__macOS_.md)
- [**macOS System Extensions**](./macOS_System_Extension_configuration.md)
- [**Media Disk Burning Restrictions**](./macOS_Disk_Burning_Restrictions.md)
- [**Privacy Settings**](./Privacy_Preference__macOS_.md)

## Setting up TvOS devices

The following configurations are supported for your tvOS:

- [**Apple TV Configuration**](./Apple_TV_Configuration.md)
- [**Apple TV Restrictions**](./iOS_Restrictions.md)
- [**Conference Room Display**](./Conference_Room_Display.md)
- [**AirPlay Mirroring**](./AirPlay_Configuration.md)

## Setting up visionOS Devices

You can now enroll Apple visionOS devices into Ivanti Neurons for MDM.

This feature currently supports: visionOS 1.1+

You can enroll visionOS devices using one of the following methods:

- [**Account driven Device Enrollment**](<Account driven Device Enrollment.htm>)
- [**Account driven User Enrollment**](<Account driven User Enrollment.htm>)
- [**Device Enrollment**](./Device_Enrollment.md)

The following configurations are supported for your visionOS devices:

- [**CalDAV Configuration**](./CalDAV_Configuration.md)
- [**CardDAV Configuration**](./CardDAV_Configuration.md)
- [**Certificate configuration**](./Certificate_configuration.md)
- [**Certificate Revocation Checking Configuration**](./Certificate_Revocation_Checking_Configuration.md)
- [**Certificate Transparency**](./Certificate_Transparency.md)
- [**Creating DNS Proxy Configuration**](./Creating_DNS_Proxy_Configuration.md)
- [**Encrypted DNS**](./Encrypted_DNS.md)
- [**Email Configuration**](./Email_Configuration.md)
- [**Exchange Configuration**](./Exchange_Configuration.md)
- [**Google Configuration**](./Google_Configuration.md)
- [**Identity Certificate**](./Identity_Certificate.md)
- [**iOS Restrictions**](./iOS_Restrictions.md)
- [**LDAP Configuration**](./LDAP_Configuration.md)
- [**Managed Domains**](./Managed_Domains.md)
- [**Network Relay Configuration**](./Network_Relay_Configuration.md)
- [**Per-app VPN Configuration**](./Per-app_VPN_Configuration.md)
- [**Single Sign-On Configuration**](./Single_Sign-On_Configuration.md)
- [**Subscribed Calendar Configuration**](./Subscribed_Calendar_Configuration.md)
- [**VPN Configuration**](./VPN_Configuration.md)
- [**Web Content Filter**](./Web_Content_Filter.md)
- [**Wi-Fi Configuration**](./Wi-Fi_Configuration.md)

## Supported device actions for visionOS Devices

The following device actions are supported for your visionOS devices:

- Wipe Apple Vision Pro
- Retire Apple Vision Pro
- Unlock Apple Vision Pro

## Support for Declarative Device Management (DDM)

Apple's Declarative Device Management is a modern management protocol that allows managed devices to proactively and autonomously apply their own management settings with less communication. Declarative Device Management is enabled on newly enrolled devices during enrollment or during check-in for already enrolled devices.

Declarative Device Management is automatically enabled on the following eligible devices:

- Computers with macOS 13 or later
- Devices with iOS 15 or iPadOS 15 or later
- Devices enrolled via User Enrollment support Declarative Device Management on iOS or iPadOS 16 or later.
- Apple TV devices with tvOS 16 or later
- Apple Watch devices with watchOS 10 or later
- Apple Vision Pro devices with visionOS 1.1 or later

Current supported Declarative Management Features:

- **Status Channels**:\* Changes to the OS Version
  - Passcode compliance
  - Passcode present
- **Configuration**:- Declarative Management Configuration

### Predicates in DDM Configurations

Predicates are expressions in Cocoa language that can provide flexibility and granularity to the activation of a configuration a device. The expression resides on the device and will be applied when the conditions on this predicate are met. We have added a new feature where you can create, save, and apply Predicates to any DDM configuration.

DDM configuration displays a new option in the Distribution page to apply a Predicate. You can find the Predicates already created from the dropdown list in this section.

Creating a Predicate

1. Go to **Admin** > **Apple** > **Predicates**.
2. Click **Add**. The **Create Predicates** window appears on the screen.
3. Enter the following information:\* **Name** - Name of the predicate
   - **Description** - Add some relevant description
   - **Predicate Expression** - Predicate expression. For example, @status(device.model.family) ==’iPad’

::Image[]{src="Resources/Images/add_predicate1.png" signedSrc="Resources/Images/add_predicate1.png" size="99" caption alt isUploading="false" sha initialPath="Resources/Images/add_predicate1.png" githubPath="Resources/Images/add_predicate1.png" position="flex-start" indent="3"}

4. Click **Save**. A dialog appears on the screen confirming the predicate creation.
5. Check the validity of the predicate syntax by refreshing the page and observing values in the STATUS field (with values: **Unknown**, **In Progress**, **Valid**, **Invalid**).1) Click **Test**. The **Test Predicate** window appears on the screen.

::Image[]{src="Resources/Images/test_predicate1.png" signedSrc="Resources/Images/test_predicate1.png" size="36" caption alt isUploading="false" sha initialPath="Resources/Images/test_predicate1.png" githubPath="Resources/Images/test_predicate1.png" position="flex-start" indent="2"}

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
Enter the following information:\* **Name** - Default
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Predicate Expression** – Default
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Spaces** – Default Space
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Platform** – iOS/macOS
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Device Name** – Related to the predicate expression.The **Device Name** field will appear beneath the **Platform** field only after the **Spaces** and **Platform** field details are selected from the dropdowns.
:::

::Image[]{src="Resources/Images/test_predicate2.png" signedSrc="Resources/Images/test_predicate2.png" size="64" caption alt isUploading="false" sha initialPath="Resources/Images/test_predicate2.png" githubPath="Resources/Images/test_predicate2.png" position="flex-start" indent="4"}

:::Paragraph{listStyleType="decimal" listStart="3" indent="2"}
Click **Test Predicate**.
:::

:::Paragraph{listStyleType="decimal" listStart="4" indent="2"}
A dialog appears on the screen confirming the test predicate initiation.
:::

:::Paragraph{listStyleType="decimal" listStart="5" indent="2"}
Refresh the page to find the status of predicate syntax.\* For correct predicate expression, the status changes from **Unknown** > **In Progress** > **Valid**.
:::

:::Paragraph{listStyleType="disc" indent="3"}
For incorrect predicate expression, the status changes from **Unknown** > **In Progress** > **Invalid**.
:::

6. Repeat the procedure if you want to create multiple predicates using different Predicate Expressions.

### Distributing predicates for a DDM configuration

1. Create a DDM supported configuration.
2. Set the toggle switch “Activation with Predicates” to ON, and use + button to include the predicates (as needed).

::Image[]{src="Resources/Images/predicates.png" signedSrc="Resources/Images/predicates.png" size="66" caption alt isUploading="false" sha initialPath="Resources/Images/predicates.png" githubPath="Resources/Images/predicates.png" position="flex-start"}

To edit or delete a predicate, go to **Admin** > **Apple** > **Predicates**. You can find the list of predicates available in this page. Click **Edit** to make any changes to the existing predicate and save it. Similarly, to delete an existing predicate, select the predicate and click **Delete**.

You cannot delete a predicate if it is associated with any configuration.

### Management Properties for a DDM configuration

The administrator can use the following to create predicates: 

- User and Device variables
- User attributes
- Device attributes

Example of using Management Properties in predicates (Custom Attributes): 

Predicate to check if the user's first name is 'test' @property(userFirstName)=='test'

### More examples

- Hardware family of a device : (Mac, iPhone, iPad, etc.)@status(device.model.family) =='iPad'If true, a passcode is present on the device. If false, passcode is not present on the device.\@status(passcode.is-present)==true
- The Operating System family in use on the device, such as macOS or iOS.\@status(device.operating-system.family)=='iPadOS'
- The Operating System version in use on the device, such as 15.0\@status(device.operating-system.version)=='18.2'@status(device.operating-system.version)\<'18.3'@status(device.operating-system.version)>='18.2'
- Boolean value that specifies the File Vault enabled status on the device\@status(diskmanagement.filevault.enabled)==true
- Example of Management Properties (Custom Attributes)\:Predicate to check if the user's first name is 'test'@property(userFirstName)=='test'
