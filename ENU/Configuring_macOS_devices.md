---
title: Configuring macOS devices
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
---

This is an overview topic that provides a list of common procedures and other content related to configuring macOS devices in Ivanti Neurons for MDM. You can access all the macOS topics in the Ivanti Neurons for MDM*Administrator Guide*.

Contents

- [**Registering devices**](./Configuring_macOS_devices.md)
- [**Configuring user invitation template**](./Configuring_macOS_devices.md)
- [**Setting up Zero Sign-on features**](./Configuring_macOS_devices.md)
- [**Setting up Mobile@Work for macOS client**](./Configuring_macOS_devices.md)
- [**Setting up macOS shell scripts**](./Configuring_macOS_devices.md)
- [**Setting up macOS configurations**](./Configuring_macOS_devices.md)
- [**Setting up macOS policies**](./Configuring_macOS_devices.md)
- [**Verifying reports and other information**](./Configuring_macOS_devices.md)

## Registering devices

Most users start by registering a device. You can use any of the following approaches to start the registration process:

- Send an invitation to one or more end users (iReg registration). For more information, see the *macOS Device Registration* topic in the [**Device registration**](./Device_Registration__iOS__macOS__and_Android_.md) section.
- [**Device Enrollment**](./Device_Enrollment.md) and [**User Enrollment with Apple Business Manager**](./User_Enrollment_with_Apple_Business_Manager.md)

For more information, see [**Device registration**](./Device_Registration__iOS__macOS__and_Android_.md).

## Configuring user invitation template

You can brand the end user email invitation to make its appearance more familiar to your end users. For more information, see [**Branding Email Templates**](./Branding_Email_Templates.md).

You can customize the device registration process with names and logos that your users will recognize. For more information, see [**User Branding**](./User_Branding.md).

For more information, see [**Configuring and Using Registration Confirmation Emails**](./Configuring_registration_confirmation_emails.md).

## Setting up Zero Sign-on features

For Zero Sign-on related documentation, see Zero Sign-on with Access in the *Access Guide*.

For zero-touch automated enrollment, see the [**User settings**](./User_Settings.md) topic, Configuring the settings for new device registrations section, Step 13.

## Setting up Mobile\@Work for macOS client

Mobile\@Work for macOS app provides:

- Scripting capabilities on macOS devices
- App Catalog for end users
- Push notifications
- User onboarding (welcome/status) screen for automated device enrollment registrations

Before pushing Mobile\@Work to the end users, ensure that [**Mobile@Work for macOS Configuration.htm**](./Mobile@Work_for_macOS.md)[**Mobile@Work for macOS**](./Mobile@Work_for_macOS.md) is created and is set to be distributed to the target macOS devices.

You can enable user onboarding for macOS devices during the automated [**Device Enrollment**](./Device_Enrollment.md) process. As soon as the Device Enrollment is completed, Mobile\@Work for macOS is pushed to the device along with the profiles, configurations, and apps.

## Setting up macOS shell scripts

Ivanti Neurons for MDMallows you to create your own macOS shell scripts, which you can then upload to Ivanti Neurons for MDM and run on managed macOS devices. You can configure the scripts using the Mobile\@Work for macOS Script configuration. Mobile\@Work for macOS returns the script execution results to Ivanti Neurons for MDM, which are shown in the device logs. You can check the device logs from the device details page of the macOS device, in the **Logs** tab. For more information about creating, uploading, and managing the scripts repository, see [**All Scripts**](./All_Scripts.md).

Before you can run shell scripts on macOS devices, ensure that the users have the Mobile\@Work for macOS app running on their devices and have a Mobile\@Work for macOS configuration pushed to their devices. Scripts can be run once or on a recurring basis. Scripting on Ivanti Neurons for MDM also allows administrators to collect information from a device and then be stored in Ivanti Neurons for MDM as a custom attribute. For example, if you need to know Java version on a macOS device, you can collect this information and store it on a per-device-basis in a custom device attribute. For more information, see *Creating a Mobile\@Work for macOS Script Configuration* in [**Mobile@Work for macOS**](./Mobile@Work_for_macOS.md).

## Setting up macOS configurations

[**Configurations**](./Configurations.md) are collections of settings that you send to devices. For example, you can use configurations to automatically set up VPN settings and passcode requirements on these devices. Use the **Configurations** page to select, set up, and distribute configurations. There are many [**types of configurations**](./Configuration_Types.md) available. In the [**page**](./Configuration_Types.md), you can view a list of available macOS configurations, including the following configurations:

- [**Wi-Fi**](./Wi-Fi_Configuration.md)
- [**Passcode**](./Passcode_Configuration.md)
- [**VPN**](./VPN_Configuration.md)
- [**Encrypted DNS**](./Encrypted_DNS.md)
- [**FileVault 2**](./FileVault_2.md)
- [**FileVault Recovery Key**](./FileVault_Recovery_Key.md)
- [**macOS Firewall**](./macOS_Firewall.md)
- [**macOS Restrictions**](./macOS_Restrictions.md)
- [**macOS AppStore Restrictions**](./macOS_AppStore_Restrictions.md)
- [**macOS Finder Settings**](./macOS_Finder_Settings.md)
- [**macOS Kernel Extension Policy**](./macOS_Kernel_Extension_Policy.md)
- [**Active Directory (macOS)**](./Active_Directory__macOS_.md)
- [**Office 365 Auto Account Creation (macOS)**](./Office_365_Auto_Account_Creation__macOS_.md)

You can use [**custom configurations**](./Custom_Configuration.md) to import and distribute a predefined configuration file.

## Setting up macOS policies

[**Policies**](./Policies.md) define requirements for devices, as well as what will happen if a device does not comply with requirements. Each policy consists of a rule and a compliance action (what happens if the rule is violated). Use the **Policies** page to select, set up, and distribute policies. Data Protection/Encryption Disabled and [**Allowed apps**](./Monitoring_and_Controlling_Allowed_Apps.md) are macOS-related policies. You can use [**Custom Policies**](./Custom_Policy.md) to create a custom policy based on device and user attributes, section criteria, values, and compliance actions you specify.

## Distributing macOS apps

Ivanti Neurons for MDM supports macOS [**apps**](./App_Catalog.md) distribution via Apple's MDM protocol and using the Mobile\@Work app. Administrators can choose to use one or both of the following approaches:

- Apple's MDM protocol - Administrators can upload only specific PKG formats (distribution format) as in-house apps and can also distribute apps from Mac App Store (Apple's Apps and Books licensing support is included). However, this approach does not allow administrators to distribute DMG and other PKG formats.
- Mobile\@Work for macOS app - As a way to distribute apps to users, administrators can use MobileIron Packager (MIP) app to convert any PKG, DMG or .app files to an MIP file. Upload the MIP file into Ivanti Neurons for MDM as an in-house app.

You can download Ivanti Neurons for MDM Mac Packager utility from MobileIron software downloads.

Administrators can use Mobile\@Work to distribute in-house apps that are in the DMG, PKG or .app format. For apps that are only available in the Mac App Store, administrators can continue to use Apple's native MDM capabilities, which includes Apple Apps and Book licenses capabilities.

## Verifying reports and other information

The [**Dashboard**](./Dashboard.md) shows important statistics about registered devices and users. Each section on the dashboard is called a widget.

You can verify additional information as follows:

- Review notifications - Go to the **Dashboard > Notifications** page (or click the bell icon (top right)) to review notifications and take actions where necessary.
- Reports - Go to the **Dashboard > Reports** page to access the data in your Unified endpoint management (UEM) system.
- Audit Trails - Go to the **Dashboard > Audit Trails** page to access the chronological set of records that capture activities performed on all entities within Ivanti Neurons for MDM. To enable this feature, go to the **Admin > Infrastructure >Audit Trails** page and click **Enable Audit Trails**.
