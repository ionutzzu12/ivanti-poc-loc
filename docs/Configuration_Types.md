---
title: Configuration Types
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Search a Configuration**](./Configuration_Types.md)
- [**Security**](./Configuration_Types.md)
- [**User Resources**](./Configuration_Types.md)
- [**Enterprise Network Access**](./Configuration_Types.md)
- [**Cellular Network**](./Configuration_Types.md)
- [**More Configurations**](./Configuration_Types.md)
- [**Device Sync Configuration**](./Configuration_Types.md)

## Search a Configuration

Use the search and filter capability on the **Choose Configurations** page to find the configuration you want to apply.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Choose **Configurations**.
:::

:::WorkflowBlockItem
Choose one of the configurations listed or click the **+Add** button.
:::

:::WorkflowBlockItem
The **Choose Configuration** page is displayed

Click one of the configurations listed or :
:::

:::WorkflowBlockItem
- Enter the name of the configuration in the search box
- Click a filter icon on the right of the search box to display configuration types compatible with platform.
  Click a configuration button to access configuration setting options.
:::
::::

For more information, see [**Working with Configurations**](./Working_with_Configurations.md).

## Security

| Type                                              | What It Does                                                   | For These Devices  | Needs This License |
| ------------------------------------------------- | -------------------------------------------------------------- | ------------------ | ------------------ |
| [**Android Enterprise**](./Android_Enterprise.md) | Specifies Android Enterprise options                           | Android Enterprise | Silver             |
| [**AppConnect Device**](./AppConnect_Overview.md) | Specifies security settings AppConnect-enabled apps on devices | - Android          |                    |

- iOS                                 | Gold                                                                                                                 |
  \| [**Entra ID (Azure Tenant)**](./Azure_Tenant_Requirements.md)                              | By connecting Ivanti Neurons for MDM to the Entra ID, you can use the device compliance status of managed devices for conditional access to Microsoft 365 apps.                                                                                                                                                                                                                                                                                                                      | \* iOS
- Android                                 | - For new customers: [**Secure UEM Premium**](https://www.mobileiron.com/en/pricing#)
- For existing customers: Platinum |
  \| [**Certificate**](./Certificate_configuration.md)                                          | Establishes trust with servers                                                                                                                                                                                                                                                                                                                                                                                                                                                       | \* Android
- iOS
- macOS
- watchOS
- visionOS    |                                                                                                                      |
  \| [**Certificate Transparency**](./Certificate_Transparency.md)                              | Controls Certificate Transparency enforcement which can only appear in a device profile.                                                                                                                                                                                                                                                                                                                                                                                             | - iOS
- macOS
- tvOS
- watchOS
- visionOS       |                                                                                                                      |
  \| [**Device Logging**](./Device_Logging_configuration.md)                                                  | Retrieves additional logs such as network and security logs from devices.                                                                                                                                                                                                                                                                                                                                                                                                            | \* Android Enterprise                            |                                                                                                                      |
  \| [**Disk Management Configuration**](./Disk_Management_Configuration.md)                    | Defines the policies to manage external and network storage devices.                                                                                                                                                                                                                                                                                                                                                                                                                 | - Supervised macOS 15.0+                        |                                                                                                                      |
  \| [**Android Encryption**](./Android_Encryption.md)                     | Prompts users to start encryption.                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Android                                         |                                                                                                                      |
  \| [**Encrypted DNS**](./Encrypted_DNS.md)                                                    | Allows you to enhance security without needing to configure VPN.                                                                                                                                                                                                                                                                                                                                                                                                                     | \* iOS
- macOS
- visionOS                        | Gold                                                                                                                 |
  \| [**Mobile Threat Defense**](./Threat_Defense.md)                                             | Protects managed devices from mobile threats and vulnerabilities affecting device, network, and applications.                                                                                                                                                                                                                                                                                                                                                                        | - Android
- iOS                                 |                                                                                                                      |
  \| Threat Defense Local Actions                                                            | Create and distribute a device configuration defining the local actions to be taken on supported Android devices when the Threat Defense-enabled client detects a threat.                                                                                                                                                                                                                                                                                                            | Android                                         |                                                                                                                      |
  \| [**FileVault 2**](./FileVault_2.md)                                                          | Provides ability to perform full XTS-AES 128 disk encryption on the contents of a volume.                                                                                                                                                                                                                                                                                                                                                                                            | macOS                                           | Gold                                                                                                                 |
  \| [**FileVault Recovery Key**](./FileVault_Recovery_Key.md)                        | Determines settings for redirecting the FileVault recovery keys to a corporate server.                                                                                                                                                                                                                                                                                                                                                                                               | macOS                                           | Gold                                                                                                                 |
  \| [**Identity Certificate**](./Identity_Certificate.md)                          | \* Authenticates the device to servers.
- Authenticates the device to network resources.                                                                                                                                                                                                                                                                                                                                                                                              | - Android
- iOS
- macOS
- watchOS
- visionOS    |                                                                                                                      |
  \| [**iOS Activation Lock**](./Apple_Activation_Lock_Configuration.md)                            | Enables the Apple Activation Lock feature on supervised devices.                                                                                                                                                                                                                                                                                                                                                                                                                     | iOS                                             | Silver                                                                                                               |
  \| [**iOS Custom Configuration**](./iOS_Custom_Configuration.md)                                | Distributes an iOS configuration profile that was created by a different app.                                                                                                                                                                                                                                                                                                                                                                                                        | iOS                                             |                                                                                                                      |
  \| [**iOS Restrictions**](./iOS_Restrictions.md)                                              | \* Locks down device features.
- Enables device features.                                                                                                                                                                                                                                                                                                                                                                                                                             | - iOS
- watchOS
- visionOS                      |                                                                                                                      |
  \| [**Conference Room Display**](./Conference_Room_Display.md)                                | Turns on the Conference Room Display mode on Apple TV.                                                                                                                                                                                                                                                                                                                                                                                                                               | tvOS 10.2+                                      |                                                                                                                      |
  \| [**Lockdown & Kiosk: Android**](./Lockdown___Kiosk__Android_Device_Admin_Mode.md)                                 | \* Locks down device features.
- Re-enables device features.
- Applies the kiosk feature.                                                                                                                                                                                                                                                                                                                                                                                             | Android                                         |                                                                                                                      |
  \| [**Lockdown & Kiosk: Android Enterprise**](./Lockdown___Kiosk__Android_Enterprise.md)       | - Defines features and apps that are restricted on Android enterprise devices.
- Applies the kiosk feature.                                                                                                                                                                                                                                                                                                                                                                          | Android 5.0 +                                   |                                                                                                                      |
  \| [**Lockdown & Kiosk: Samsung Know Standard**](./Lockdown___Kiosk__Samsung_Knox_Standard.md) | \* Defines features and apps that are restricted on Samsung Knox Standard devices.
- Applies the kiosk feature.                                                                                                                                                                                                                                                                                                                                                                       | Samsung Knox                                    |                                                                                                                      |
  \| [**macOS Firewall**](./macOS_Firewall.md)                                                  | Manages the Application Firewall settings that are accessible in the Security Preferences pane on macOS devices.The Administrator can enable the stealth mode by specifying a device that cannot be discovered by the ping command.                                                                                                                                                                                                                                                  | macOS 10.12+                                    | Gold                                                                                                                 |
  \| [**macOS Restrictions**](./macOS_Restrictions.md)                                          | Determine which restrictions are enabled on macOS devices.                                                                                                                                                                                                                                                                                                                                                                                                                           | macOS                                           | Gold                                                                                                                 |
  \| [**macOS AppStore Restrictions**](./macOS_AppStore_Restrictions.md)                          | Define which restrictions are enabled in macOS AppStore.                                                                                                                                                                                                                                                                                                                                                                                                                             | macOS                                           | Gold                                                                                                                 |
  \| [**macOS Disk Burning Restrictions**](./macOS_Disk_Burning_Restrictions.md)                  | Manage disk burning restrictions in macOS.                                                                                                                                                                                                                                                                                                                                                                                                                                           | macOS                                           | Gold                                                                                                                 |
  \| [**Mobile@Work for macOS**](./Mobile@Work_for_macOS.md)                      | Create and distribute execution rules for Mobile\@Work for macOS.                                                                                                                                                                                                                                                                                                                                                                                                                    | macOS                                           | Gold                                                                                                                 |
  \| [**Mobile@Work for macOS Script**](./Mobile@Work_for_macOS.md)               | Create scripts to distribute to Mobile\@Work for macOS.                                                                                                                                                                                                                                                                                                                                                                                                                              | macOS                                           | Gold                                                                                                                 |
  \| [**Identity Preference**](./Identity_Preference.md)                                        | Identify an Identity Preference item in the user's keychain that references an identity payload included in the same profile.                                                                                                                                                                                                                                                                                                                                                        | macOS                                           | Gold                                                                                                                 |
  \| [**Certificate Preference**](./Certificate_Preference.md)                                  | Identify a Certificate preference item in the user's keychain that references a Certificate payload included in the same profile.                                                                                                                                                                                                                                                                                                                                                    | macOS                                           | Gold                                                                                                                 |
  \| [**Allowed Media Control**](./Allowed_Media_Control__Deprecated_.md)                                      | Configure mounting, unmounting, and eject options for physical media.                                                                                                                                                                                                                                                                                                                                                                                                                | macOS                                           | Gold                                                                                                                 |
  \| [**macOS Finder Settings**](./macOS_Finder_Settings.md)                                      | Manage settings of Finder app in macOS.                                                                                                                                                                                                                                                                                                                                                                                                                                              | macOS                                           | Gold                                                                                                                 |
  \| [**macOS Kernel Extension Policy**](./macOS_Kernel_Extension_Policy.md)                    | Controls restrictions and settings for loading user-approved Kernel Extensions.                                                                                                                                                                                                                                                                                                                                                                                                      | macOS                                           | Gold                                                                                                                 |
  \| [**Active Directory (macOS)**](./Active_Directory__macOS_.md)                                      | Configure advanced options to bind macOS devices to an Active Directory (AD) domain in order to access software services that rely on AD for authentication and security.                                                                                                                                                                                                                                                                                                            | macOS                                           | Gold                                                                                                                 |
  \| [**Office 365 Auto Account Creation (macOS)**](./Office_365_Auto_Account_Creation__macOS_.md)      | Configure user information and options to setup initial configuration for all Microsoft Office 365 applications.                                                                                                                                                                                                                                                                                                                                                                     | macOS                                           | Gold                                                                                                                 |
  \| [**Apple App Catalog**](./Apple_App_Catalog.md)                                              | Manages access to the Apple App Catalog via a web clip.                                                                                                                                                                                                                                                                                                                                                                                                                              | - iOS
- macOS                                   |                                                                                                                      |
  \| [**Managed Domains**](./Managed_Domains.md)                                    | Specifies trusted email and web domains.                                                                                                                                                                                                                                                                                                                                                                                                                                             | \* iOS 8+
- visionOS 1.1+                        | Silver                                                                                                               |
  \| [**Passcode**](./Passcode_Configuration.md)                                                       | - Makes a passcode mandatory.
- Specifies passcode length and content.
- Changes passcode requirements.                                                                                                                                                                                                                                                                                                                                                                              | \* Android
- iOS
- macOS
- watchOS               |                                                                                                                      |
  \| [**Privacy Preference (macOS)**](./Privacy_Preference__macOS_.md)                                  | Configure which applications are allowed to gain access to system services, system files, and system resources.                                                                                                                                                                                                                                                                                                                                                                      | macOS                                           | Gold                                                                                                                 |
  \| Authenticate                                                                            | Provide password-less authentication for cloud services and/or desktop logins.                                                                                                                                                                                                                                                                                                                                                                                                       | - macOS
- Windows                               |                                                                                                                      |
  \| [**Privacy Configuration**](./Privacy_Configuration.md)                                      | Specifies whether location data is collected.                                                                                                                                                                                                                                                                                                                                                                                                                                        | \* iOS
- Android
- Windows                       |                                                                                                                      |
  \| [**Client Privacy Statement Information**](./Client_Privacy_Statement_Information.md)                         | Display privacy policy to the user in Go client.                                                                                                                                                                                                                                                                                                                                                                                                                                     | - Android
- Android enterprise
- iOS            |                                                                                                                      |
  \| [**Ivanti Go Client Settings**](./Ivanti_Go_Client_Settings.md)                            | Configure to collect data via MixPanel including device and usage information to troubleshoot and maintain the highest quality of services.                                                                                                                                                                                                                                                                                                                                          | \* iOS
- macOS                                   |                                                                                                                      |
  \| [**Safari Extension Settings Configuration**](./Safari_Extension_Settings_Configuration.md)              | Manage Safari browser extensions from various domains.                                                                                                                                                                                                                                                                                                                                                                                                                               | - Supervised iOS 18.0+
- Supervised macOS 15.0+ |                                                                                                                      |
  \| [**Software Updates**](./Software_Updates.md)                                                | Creates and distributes rules for OS updates.                                                                                                                                                                                                                                                                                                                                                                                                                                        | \* iOS
- macOS
- Windows                         |                                                                                                                      |
  \| [**Software Update Settings Configuration**](./Software_Update_Settings_Configuration.md)                | Creates and updates Software Update Enforcement settings.                                                                                                                                                                                                                                                                                                                                                                                                                            | - Supervised iOS 18.0+
- Supervised macOS 15.0+ |                                                                                                                      |
  \| [**Time Server**](./Time_Server.md)                                                        | Allow devices to connect to custom time servers.                                                                                                                                                                                                                                                                                                                                                                                                                                     | macOS                                           | Gold                                                                                                                 |
  \| [**Web Content Filter**](./Web_Content_Filter.md)                              | Controls Safari content.                                                                                                                                                                                                                                                                                                                                                                                                                                                             | \* Supervised iOS 7
- visionOS 1.1+              | Silver                                                                  |
  \| [**Windows\_Firewall**](./Windows_Firewall.md)                                               | The Windows Firewall configuration has various firewall restrictions. Based on the firewall restrictions applied by the administrator, the Firewall Status result in one of the following firewall statuses in the Security Preferences pane on Windows devices:\* Firewall is on and monitoring.
- Firewall has been disabled.
- Firewall isn't monitoring all networks or some rules have been turned off.
- Firewall is temporarily not monitoring all networks.
- Not applicable. | Windows 10+                                     |                                                                                                                      |
  \| [**Windows Information Protection**](./Windows_Information_Protection.md)      | Defines Windows Information Protection (WIP) settings to protect enterprise data.                                                                                                                                                                                                                                                                                                                                                                                                    | Windows 10+                                     | Gold                                                                                                                 |
  \| [**Windows Restrictions**](./Windows_Restrictions.md)                          | Determines which features are available on Windows 10+ devices.                                                                                                                                                                                                                                                                                                                                                                                                                      | Windows 10+                                     |                                                                                                                      |
  \| [**Windows AI Management Configuration**](./Windows_AI_Management_Configuration.md)        | Allows you to manage Windows AI settings and configurations.                                                                                                                                                                                                                                                                                                                                                                                                                         | Windows 10+                                     |                                                                                                                      |

## User Resources

| Type                                    | What It Does                                               | For These Devices | Needs This License |
| --------------------------------------- | ---------------------------------------------------------- | ----------------- | ------------------ |
| [**CalDAV**](./CalDAV_Configuration.md) | - sets up access to a CalDAV server (like Google Calendar) | \* iOS            |                    |

- visionOS                   |                                                                                                              |
  \| [**CardDAV**](./CardDAV_Configuration.md)                                       | - sets up access to a CardDAV server (like Google Contacts)                                                                                                                                                                              | \* iOS
- visionOS                   |                                                                                                              |
  \| [**Email**](./Email_Configuration.md)                             | - sets up access for POP/IMAP email (like Gmail)                                                                                                                                                                                         | \* iOS
- visionOS                   |                                                                                                              |
  \| [**Exchange**](./Exchange_Configuration.md)            | - sets up access for ActiveSync-based email  (like Outlook) for Android and iOS mobile devices
- sets up Exchange Web Services (EWS)-based email for macOS devices
- defines how much to sync to the device
- defines security for email | \* Android
- iOS
- macOS
- visionOS | \* Exchange via sentry is not supported on macOS
- The Sync Past days emails flag is not applicable for macOS |
  \| [**Google**](./Google_Configuration.md)                                         | - Creates Google account configurations that connect iOS 9.3.2+ devices to Google accounts.
- Specifies which app to use to make calls to contacts in the Google system.                                                                 | \* iOS
- visionOS                   |                                                                                                              |
  \| [**Font**](./Font_Configuration.md)                               | - installs non-standard fonts necessary for proper display of documents                                                                                                                                                                  | \* iOS                              |                                                                                                              |
  \| [**Subscribed Calendar**](./Subscribed_Calendar_Configuration.md) | - sets up a subscription to an internet calendar                                                                                                                                                                                         | \* iOS
- visionOS                   |                                                                                                              |
  \| [**Web Clip**](./Create_a_Web_Clip_Configuration.md)            | - displays a shortcut (icon) to a web page                                                                                                                                                                                               | \* iOS
- macOS                      |                                                                                                              |
  \| [**Content Caching**](./Content_Caching.md)                     | - provides content-caching service in order to enable local copies of the App Store software and
- enables connected clients for faster software and app downloads.                                                                      | \* macOS                            |                                                                                                              |

## Enterprise Network Access

| Type                                      | What It Does                                            | For These Devices | Needs This License |
| ----------------------------------------- | ------------------------------------------------------- | ----------------- | ------------------ |
| [**AirPlay**](./AirPlay_Configuration.md) | - sets up access to alternate devices for media display | \* iOS            |                    |

- macOS                                                                                  | Silver |
  \| [**AirPrint**](./AirPrint_Configuration.md)                                 | - sets up wireless printing                                                                                                                      | \* iOS
- macOS                                                                                  | Silver |
  \| [**Always On VPN**](./Always-on_VPN_Configuration.md)                                     | - sets up access to a VPN server without user interaction                                                                                        | \* Android 7.0 +
- iOS 8+                                                                       | - Gold for Android enterprise
- Silver for iOS      |
  \| [**Default App Runtime Permissions**](./Default_App_Runtime_Permissions.md) | \* sets the runtime permission configuration for apps deployed to Android enterprise devices.                                                     | - Apps built targeting Android API 23+ and running Android 6.0+ on Android enterprise devices. |                                                     |
  \| [**Education**](./Education.md)                                             | \* configures the Apple Education payload and the Classroom app for Leaders and Members                                                           | - supervised iOS 9.3+                                                                          | Gold                                                |
  \| [**Global Proxy**](./Global_Proxy_Configuration.md)                         | \* sets up devices to forward HTTP traffic to a proxy server                                                                                      | - supervised iOS 7                                                                             | Silver |
  \| [**LDAP**](./LDAP_Configuration.md)                                         | \* sets up access to a corporate directory                                                                                                        | - iOS
- visionOS                                                                               |                                                     |
  \| Tunnel                                                                 | \* defines a per-app VPN connection between a client and Sentry using Tunnel                                                                      | - iOS 7+
- macOS 10.13+
- Windows 10+
- Android                                                |                                                     |
  \| [**Bridge**](./Ivanti_Bridge.md)                                                   | \* allows IT to modernize Windows operations on UEM without giving up critical functionality                                                      | - Windows 10+ desktop                                                                          | Bridge license                                      |
  \| [**macOS Server**](./macOS_Server_Configuration.md)                         | \* define a macOS Server account with the configured account types and relevant settings. Allows the user to activate File Sharing on the server. | - iOS 10+                                                                                      |                                                     |
  \| [**Per-app VPN**](./Per-app_VPN_Configuration.md)                           | \* sets up connections between specific apps and a VPN server                                                                                     | - iOS
- watchOS
- visionOS                                                                     | Silver |
  \| [**Network Relay Configuration**](./Network_Relay_Configuration.md)       | \* adds configuration to define settings for network relays                                                                                       | - iOS
- macOS
- visionOS                                                                       |                                                     |
  \| [**Single Sign-On**](./Single_Sign-On_Configuration.md)                     | \* sets up single sign-on for specified managed apps                                                                                              | - iOS
- macOS
- visionOS                                                                       |                                                     |
  \| [**Multi-user Secure Sign-in**](./Multi-user_Secure_Sign-in_for_iOS.md)             | \* sets up secure multi-user login via web clip                                                                                                   | - iOS                                                                                          |                                                     |
  \| [**VPN**](./VPN_Configuration.md)                                           | \* sets up access to a VPN server                                                                                                                 | - Android
- Windows
- iOS
- macOS
- visionOS                                                   |                                                     |
  \| [**VPN On Demand**](./VPN_On_Demand.md)                                     | \* sets up access to a VPN server based on domains, host names, etc.                                                                              | - iOS                                                                                          |                                                     |
  \| [**Wi-Fi**](./Wi-Fi_Configuration.md)                                       | \* sets up access to a wireless network                                                                                                           | - Android
- Windows
- iOS
- macOS
- watchOS
- visionOS                                         |                                                     |

## Cellular Network

| Type                              | What It Does                                            | For These Devices | Needs This License |
| --------------------------------- | ------------------------------------------------------- | ----------------- | ------------------ |
| [**APN**](./APN_Configuration.md) | - sets up the cellular Access Point Name for the device | \* iOS            |                    |
| [**Cellular**](./Cellular.md)     | - sets up cellular network access                       | \* iOS            |                    |

- watchOS   |                    |
  \| [**Cellular Private Network Configuration**](./Cellular_Private_Network_Configuration.md) | - sets the payload to provide device information on private network deployments                        | \* iOS             |                    |
  \| [**iOS Telecom Presets Configuration**](./iOS_Telecom_Presets_Configuration.md)             | - sets default values for roaming restrictions
- sets default values for personal hotspot restrictions | \* iOS             |                    |

## More Configurations

| Type                                                                          | What It Does                                                                                                                                            | For These Devices   | Needs This License |
| ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- | ------------------ |
| [**Apple TV**](./Apple_TV_Configuration.md)                                   | - defines language and locale for Apple TV                                                                                                              | \* supervised iOS 7 | Silver             |
| [**Default Device Name**](./Device_Name_Settings.md)                          | - defines a default device name using variables                                                                                                         | \* supervised iOS 8 | Silver             |
| [**iOS Wallpaper**](./Device_Wallpaper_Configuration.md)                      | - installs a home screen and lock screen background                                                                                                     | \* supervised iOS 7 | Silver             |
| macOS Wallpaper                                                               | - Installs a home screen and lock screen wallpaper on the devices. Wallpapers can be changed by the user but not removed from a device once distributed |                     | Not required       |
| [**Single App Mode**](./Single_App_Mode_Configuration.md)                     | \* restricts the device to use of the specified app                                                                                                     | - supervised iOS 7  | Silver             |
| [**Associated Domains Configuration**](./Associated_Domains_Configuration.md) | \* The Associated Domains configuration is a dictionary that maps apps to their associated domains.                                                     |                     |                    |

- Associated domains can be used with features such as Extensible AppSSO, universal links, and Password AutoFill. | macOS 10.15+       | Gold        |

## Device Sync Configuration

Device Sync settings provide a list data points you can monitor on devices. Device Sync configurations cannot be edited. You can view a list of the settings checked.

**Procedure**

1. Go to **Configurations**.
2. Click **Device Sync Config**.The Details tab of the **Device Sync Config** page is displayed with a list of items checked.

| **Settings**              | **Time between readings in minutes** |
| ------------------------- | ------------------------------------ |
| Certificate List          |                                      |
| Device Information        | 60                                   |
| Installed App List        | 60                                   |
| Managed App List          | 60                                   |
| Profile List              | 60                                   |
| Provisioning Profile List | 60                                   |
| Restrictions              | 60                                   |
| Security Information      | 60                                   |
| **iOS 9+**                |                                      |
| Check for Updates         | 1440                                 |

### Related topics

- [**Variables**](./Variables.md)
