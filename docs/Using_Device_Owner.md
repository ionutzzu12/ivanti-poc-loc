---
title: Using Device Owner
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Provisioning Android Enterprise Devices using a QR code or NFC Bump**](./Using_Device_Owner.md)
- [**Provisioning Android Enterprise devices using client token**](./Using_Device_Owner.md)

**License**: Gold

You can designate devices as company-owned or employee-owned after the devices have been registered. This designation helps manage policies that are based on whether a user has a personal device or a company owned device. With the proper license, you can then use ownership in rules for creating device groups.

Starting with a new or factory-reset device, use the [**Provisioner**](./Setting_up_the_Provisioner_app.md) app to provision device owner mode using one of the following options:

- NFC (Near Field Communication) bump
- QR code scan

An NFC bump involves tapping the master or template device against a new or factory-reset device to provision it.

A QR code scan involves tapping the screen of a new or factory-reset device, configuring a Wi-Fi network, and scanning the code when the device is ready to be provisioned.

While provisioning Device Owner mode using NFC or QR code, the provisioner app accepts an enrollment token. On registration, the enrollment token is sent to the server. If it is present in the server and the device is assigned to a user, the device is successfully registered.

The Go client will control the device once it is in Device Owner mode and locks itself to the screen until the device is registered with Ivanti Neurons for MDM to prevent users from leaving the provisioning process. Device Owner mode also supports Kiosk mode. For configuration information go to: [**Lockdown & Kiosk Configuration**](./Lockdown___Kiosk__Android_Device_Admin_Mode.md).

**Important**

- If you retire a device in Device Owner mode, the device will factory reset.
- All devices in Device Owner mode can optionally have all the system apps enabled.
- A device can only have one active device owner at a time.
- Only devices that are Android Enterprise capable are able to be provisioned into device owner mode.
- For Samsung Knox Standard devices that are in Device Owner mode, users will be prompted to activate Samsung ELM license. This prompt will also appear on Samsung devices that are in Device Owner mode when the Go client app is upgraded from a previous release to the most recently released version as supported by Ivanti Neurons for MDM. After activation, the serial number is displayed on the Device Details page, which would match with the Device > Settings > Serial Number field.

## Provisioning Android Enterprise Devices using a QR code or NFC Bump

To provision Android Enterprise devices using QR code or NFC bump you will need to download and install the Provisioner app from Google Play on the master device.

Compatible Components

Provisioner version: 1.3.0.

Provisioner is compatible with or works with the following:

| Item                                    | Version                                                        |
| --------------------------------------- | -------------------------------------------------------------- |
| Android OS(on device to be provisioned) | - 5.0 - or supported newer versions is required, if using NFC. |

- 7.0 - or supported newer versions is required is required if using QR code.Device must be Android Enterprise capable. |
  \| Android OS (on master device)                      | 5.1 - through the most recently released version.Device must have NFC for using NFC bump. It is not required for QR code.                                                              |
  \| UEM server product, enabled for Android Enterprise | One of the following\:Ivanti Neurons for MDM, or Allow-labeled Ivanti Neurons for MDM.                                                                                                 |
  \| Android client app                                 | The latest client app version is automatically installed on the provisioned device by Provisioner.                                                                                     |

**Prerequisites**

To provision an Android Enterprise device to be a work managed device, you need to:

- Ensure the required Android Enterprise-related configuration is defined and will apply to the registered device.
- The default Android Enterprise: Work Managed Device configuration must be enabled for the device.
  Enable Android Enterprise on the server.
- Have an NFC-capable Android device (only if NFC is used) to serve as the master, with the Provisioner app installed.
- Have Android Enterprise-capable devices to provision.

To enable the Android beam for use with NFC bump:

**Procedure**

1. Go to **Settings** on the device.
2. Go to **Networks > Wireless Networks**.
3. In the **Connectivity section** select **Share & connect**.
4. Slide the **NFC** switch to **On**.
5. Slide the **Android Beam** switch to **On**.

The steps to enable the Android beam and NFC may vary on different devices.

## Provision Android Enterprise devices to become work managed devices

**Procedure**

1. Using the Android master device, download the Provisioner app from Google Play and install the app.
2. Launch Provisioner on the master device.
3. Select NFC or QR code for the Provisioning method.
4. Tap **App for Provisioning**, and choose the client app to be installed on the provisioned device:| Select this client app: | To register with this UEM server:      |
   \| ----------------------- | -------------------------------------- |
   \| Go                      | Ivanti Neurons for MDM                 |
   \| At Work UEM             | (Allow labeled) Ivanti Neurons for MDM |
5. Fill out the remaining fields in the Provisioner app. Some fields may auto-populate if a supported Wi-Fi type is present. The Wi-Fi fields are not shown if QR code is selected. Use these guidelines:| Field                       | Value                                                                                                                                                                                                                                                  |
   \| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   \| Select app for provisioning | Go or At Work                                                                                                                                                                                                                                          |
   \| Time Zone                   | Enter the time zone to be configured on the device                                                                                                                                                                                                     |
   \| Locale                      | Enter the locale to be configured on the device                                                                                                                                                                                                        |
   \| Enable All System Apps      | Click the checkbox to enable all system apps                                                                                                                                                                                                           |
   \| Wi-Fi Network SSID          | Enter the Wi-Fi SSID the target device is to use                                                                                                                                                                                                       |
   \| Wi-Fi Security Type         | Enter the Wi-Fi security type                                                                                                                                                                                                                          |
   \| Wi-Fi Password              | Enter the password for the Wi-Fi                                                                                                                                                                                                                       |
   \| Bulk Enrollment             | The bulk enrollment feature is optional. To use the bulk enrollment, a hostname is required. Optionally, a username may be entered and the quick start option may be selected. To skip the bulk enrollment feature, these fields should be left blank. |
6. Tap **Continue**.
7. If you selected **NFC**, tap **Continue**. The screen **Bump the devices!** appears on the master device. Continue with the **NFC Bump** section below.
8. If you selected **QR code**, the screen **Scan this QR code!** appears on the master device. Continue with the **QR Code** section below.
   **Use the steps below for NFC Bump**
   Confirm that the target device is displaying the Android Welcome screen.
9. Press the master device back-to-back with the target device to initiate an NFC transfer. If the NFC transfer succeeds, the target device may make a sound, and then proceed to download the client app. If a Wi-Fi connection cannot be established, or if the device is unable to download the client app, the device will automatically do a factory reset.
10. If you hear the sound or see a screen other than the Welcome screen, you can decouple the devices. This typically takes a few seconds. If the device is not encrypted, it will start the encryption process before continuing.
11. You can continue to provision additional devices by “bumping” the devices to the master device. The target device must be showing the Welcome screen, and the master device must be showing the “Bump the devices!” screen.
    **Use the steps below for QR Code provisioning**
    Confirm that the target device is displaying the Android Welcome screen.
12. Tap the Android Welcome screen on the target device 6 times on the same place on the screen.
13. You will be prompted to configure a WiFi network so the setup wizard can download a QR code reader to the target device.
14. After the QR code reader is downloaded, the camera is launched.
15. Hold the target device a few inches above the master device until the QR code is scanned successfully. The setup wizard will then proceed to download the client app. If it is unable to download the client app, it will automatically do a factory reset.
16. You can continue to provision additional devices by scanning the QR code on the master device. The target device must have a camera ready to scan, and the master device must be showing the “Scan this QR code!” screen.
17. The QR code can also be exported by tapping the Share icon. The options offered for exporting will vary by device.

## Provisioning Android Enterprise devices using client token

You can provision an Android Enterprise device in Device Owner mode using a branded client token instead of using the NFC bump or QR code methods. This method enables you to sign on a device with a token which facilitates an automatic installation of the Go or At Work client and provisioning in Device Owner mode:

Branded client tokens are supported on devices provisioned with Managed Google Play Accounts, using Android 6 or supported newer versions. For more details see the Android UEM Developers guide. [**https://developers.google.com/android/work/prov-devices#Key\_provisioning\_differences\_across\_android\_releases.**](https://developers.google.com/android/work/prov-devices#Key_provisioning_differences_across_android_releases)

Requirements to use this method:

- You must be enrolled with an Android Enterprise account.
- The device must be Android Enterprise-capable.
- The device must use Android 6 through the most recently released version.
- You must have a new or factory reset device.

## Configure (for devices running Android 5.0+)

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
In theIvanti Neurons for MDMportal, Go to **Configurations**.
:::

:::WorkflowBlockItem
Click **+Add**.
:::

:::WorkflowBlockItem
Select **Lockdown & Kiosk: Android Enterprise**.
:::

:::WorkflowBlockItem
The **Create Lockdown & Kiosk: Android Enterprise Configuration** page is displayed.

Enter a configuration name and description.
:::

:::WorkflowBlockItem
Choose a Lockdown type.

Click **Work Managed Devices (Device Owner)**.
:::

:::WorkflowBlockItem
Android Device Owner Lockdown settings options are displayed.

Optionally, choose to

- Disable WI-FI  or WI-FI settings
- Disable Camera
- Disable Bluetooth
- Disallow Bluetooth Settings
- Disable Screen Capture
- Mute Master Volume
- Disallow Apps Control
- Disallow Credentials
- Disallow Emergency Broadcasts
- Disallow Mobile Networks
- Disallow Tethering
- Disallow VPN
- Disallow Factory Reset
- Enable Factory Reset Protection.
- You can optionally specify a list of authorized Google account IDs (an integer value) that can provision the device after factory reset or hover over the help icon to view help for retrieving authorized account IDs).
  Disallow Modify Accounts
- Disable NFC (Outgoing Beam)
- Disallow Outgoing Calls
- Disallow Safe Boot
- Disallow Share Location
- Disallow Debugging features
- Ensure Verify Apps
- Disallow SMS
- Disallow Unmute Microphone
- Disable Auto Time
- Disable Auto Time Zone
- Disable Data Roaming
- Disable Wi-Fi Sleep
- Restrict Input Methods
- Restrict Accessibility Services
- Disable USB file transfer
- Disable external media
- Disable keyguard (no effect if PIN/Passcode is set)
- Keep screen on while connected to power
- Disallow create windows
- Skip first use hints
  Under **Enable/Disable System Apps** section, you can optionally choose to enable to disable the following System Apps:
:::

:::WorkflowBlockItem
| Item                                        | Version                                                                                                                                                                                         |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Preset System Apps**                      |                                                                                                                                                                                                 |
| **Built-In camera**                         | Click the toggle button to turn **ON** or **OFF** the Built-In Camera app.                                                                                                                      |
| **Built-In Phone**                          | Click the toggle button to turn **ON** or **OFF** the Built-In Phone app.                                                                                                                       |
| **System App Package Name**                 | To enable or disable any other system app(s) other than the preset system apps, Click the +(plus)  icon and add the system app package name. To remove the system app, click the -(minus) icon. |
| Optionally choose to enable **Kiosk Mode**. |                                                                                                                                                                                                 |

The following settings are displayed:

- Enable Lock Task Mode
- Enter Kiosk automatically (on initial setup only)
- Disable Quick Settings
- Allow User to Access WiFi Settings
- Allow User to Access Bluetooth Settings
- Allow User to Access Location Settings
- Allow User to Delay Application Updates
- Allow User to Access Date and Time Settings
- Allow User to Access Mobile Network Settings
- Allow User to Select Language
- Enable Shared Device (select any of the following options)
  - Enable Login
  - Enable Logout (provide the Timeout setting in hours)
    Optionally select the default or custom branding options from the drop-down list.
:::

:::WorkflowBlockItem
Optionally create a Kiosk Exit Pin to use to exit Kiosk mode.
:::

:::WorkflowBlockItem
Optionally create a Allowlist of apps that will be available to users in Kiosk Mode.
:::
::::

## Provision the device

**Procedure**

1. Power on the device and enter your WI-FI password. Your device may prompt you for a different password.
2. In the **Verify your account** screen enter your Android Enterprise token. Click **Next**.
3. On the **Google Services** screen click **Install**.
4. Accept the Terms and Conditions.
5. On the Setup work device screen click **Next**. The Go or At Work client downloads and installs on the device. The device now enters Device Owner mode.

**Related topics**

- [**Using Bulk Enrollment for Android**](./Using_Bulk_Enrollment_for_Android.md)
