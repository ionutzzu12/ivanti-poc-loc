---
title: Apps@Work (iOS, Android, Windows, and macOS)
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

Apps\@Work is an enterprise app storefront that facilitates the secure distribution of software and apps. Apps\@work is available for iOS, Android, macOS and Windows devices. Apps\@Work corporate appstore is integrated into Ivanti Go app and Mobile\@Work clients for iOS, Android and macOS. For Windows devices it is a native standalone application. This section contains the following topics:

- [**iOS Apps@Work**](./Apps@Work__iOS__Android__Windows__and_macOS_.md)
- [**Android Apps@Work**](./Apps@Work__iOS__Android__Windows__and_macOS_.md)
- [**macOS Apps@Work**](./Apps@Work__iOS__Android__Windows__and_macOS_.md)
- [**Windows Apps@Work**](./Apps@Work__iOS__Android__Windows__and_macOS_.md)

## iOS Apps\@Work

The Apps\@work native appstore is deployed automatically with the Go client. No action from the administrator is required. The Apps\@work tab is displayed on the Go client task bar. End user can go to this tab to view and install their company approved apps. For more information, see [**iOS Apps@Work AppStore Features**](./iOS_Apps@Work_AppStore_Features.md).

The iOS Apps\@Work end user notifications for app updates are enabled by default. If you want to change the settings see the **Notifications** topic in [**Catalog Settings**](./Catalog_Settings.md).

## Existing Customers with iOS Apps\@Work Webclip

The customers who have the legacy iOS Apps\@Work webclip deployed, will not get the Native Integrated AppCatalog by default. If you would like to transition to the iOS Apps\@Work Native catalog and remove the Apps\@work webclip from the devices, perform the following steps:

### Pushing the configurations

The administrator must push the App Catalog for Native Client configuration to the devices to make Apps\@Work available in a Native Appstore experience from Go client application. For more information, see [**Working with Configurations**](./Working_with_Configurations.md).

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Go to **Configurations** > Filter and select **Client Services**. All the client configurations are listed.
3. Select **App Catalog for Native Client**. The App Catalog for Native Client configuration page opens.
4. Click the **Edit Distribution** icon. The Edit Distribution page opens.
5. Select one of the following options:\* **All Devices**
   - **No Devices** - if you do not want to distribute to any devices
   - **Custom** - lets you select Devices, Device Groups, Users, User Groups
6. After the configuration is distributed the user must upgrade the Go client version to 83 or above. Apps\@Work tab is now visible in the Go app client.The configuration cannot be pushed for devices that are registered using iReg because Go client is unavailable on the device. You must install the Go app client to get the native app catalog. For more information, see [**Device Registration (iOS, macOS, and Android)**](./Device_Registration__iOS__macOS__and_Android_.md).

## Remove iOS Apps\@Work Webclip

For customers who have Apps\@Work Webclip distributed to their devices and have already migrated to Apps\@Work Native experience they can remove iOS Apps\@Work webclip.

**Procedure**

1. Go to **Configurations**.
2. Filter the Configuration – **Apple App Catalog**.
3. Click **Edit**.
4. From **Distribution** select **Distribution to No Devices**.
5. Click **Save**.

## Android Apps\@Work

The Apps\@work native appstore is deployed automatically with the MI Go client. No action from the administrator is required. The Apps\@work tab is displayed on the Mi Go client task bar. End user can go to this tab to view and install their company approved apps. For more information, see [**Admin - Android Enterprise**](./Admin_-_Android_Enterprise.md).

## macOS Apps\@Work

macOs Apps\@work is integrated into the macOS Mobile\@Work client. Once device has registered into Ivanti Neurons for MDM the client will switch and display as Apps\@Work. For newly created tenants the Apple App Catalog Webclip configuration will not be pushed to macOS devices. If required the administrator can distribute the Apps\@work Webclip configuration to macOS devices. For more information, see [**Configuring macOS devices**](./Configuring_macOS_devices.md).

### Distributing macOS apps

- Ivanti supports macOS apps distribution via Apple MDM protocol and using the Mobile\@Work app. Administrators can choose to use one or both of the following approaches:
  - Apple's MDM protocol - Administrators can upload only specific PKG formats (distribution format) as in-house apps and can also distribute apps from Mac App Store (Apple's Apps and Books licensing support is included). However, this approach does not allow administrators to distribute DMG and other PKG formats.
  - Mobile\@Work for macOS app - As a way to distribute apps to users, administrators can use MobileIron Packager (MIP) app to convert any PKG, DMG or .app files to a MIP file. Upload the MIP file into Ivanti Neurons for MDM as an in-house app
    You can download the utility from the [**software downloads site**](https://support.mobileiron.com/mi/mobileatwork-macos/current/).
- Administrators can use Mobile\@Work to distribute in-house apps that are in the DMG, PKG or .app format. For apps that are only available in the Mac App Store, administrators can continue to use Apple's native MDM capabilities, which includes Apple Apps and Book licenses capabilities. For more information, see [**Configuring macOS devices**](./Configuring_macOS_devices.md).

## Windows Apps\@Work

Apps\@Work is a stand alone native app that can be downloaded from the Microsoft Store or can be push directly from Ivanti Neurons for MDM. It enables use of Windows public and in-house apps on Windows 10+ devices in Ivanti Neurons for MDM. Apps\@Work is installed silently on supported Windows 10+ devices.

For more information, see [**App Configuration**](./App_Configuration.md).

### Using Windows Apps\@Work

Apps\@Work enables use of Windows public and in-house apps on Windows 10 devices in Ivanti Neurons for MDM. Apps\@Work is installed silently on supported Windows 10 devices.

**Apps\@Work Certificate Authentication**

To use Certificate Authentication with Windows Apps\@Work:

1. Go to **Admin**\*\*>**Windows**>\*\***Apps\@Work Certificate Authentication**.
2. Toggle the setting to **ON**.
   Toggle the setting to **OFF** enforces the use of username and password.

SAML is not supported for Apps\@Work for Windows.

To configure an app for Apps\@Work:

1. Select a Windows app.
2. Click the **App Configuration** tab.
3. Click **Install on Device**.Windows In-house app configuration can be set to the silent install flag or install using Apps\@Work. Public apps cannot be set to silent install.
4. Optionally, choose to display or hide apps in Apps\@work catalog.This option applies to in-house apps only.
5. Click the **Promotion** tab.Apps\@Work currently does not support the banner promotion so the available options are **Featured** and **Not Featured**.Only the **Promotion** option is displayed for public apps.
