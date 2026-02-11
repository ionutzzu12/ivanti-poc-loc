---
title: Apple Activation Lock Configuration
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

**License:** Silver

This section contains the following topics:

- [**Enabling the iOS Activation Lock**](./Apple_Activation_Lock_Configuration.md)
- [**Enable the iOS Activation Lock feature on supervised devices**](./Apple_Activation_Lock_Configuration.md)
- [**Enabling the macOS Activation Lock**](./Apple_Activation_Lock_Configuration.md)
- [**Enable the macOS Activation Lock feature on supervised devices**](./Apple_Activation_Lock_Configuration.md)
- [**Using the iOS Activation Lock bypass code**](./Apple_Activation_Lock_Configuration.md)
- [**Clearing the iOS Activation Lock bypass code**](./Apple_Activation_Lock_Configuration.md)

Activation Lock is an Apple feature designed to prevent anyone from using a lost or stolen device. After Find My is enabled, a mapping between iCloud account and a hardware identifier for this device is saved to Apple’s activation servers. From that point, no one can disable Find My, erase the device, or reactivate it without entering the existing Apple ID and password. If someone other than the user wipes the device and then tries to re-activate and use it, they will be prompted for the Apple ID and password in Setup Assistant.

Disabling Activation Lock will not disable this feature on supervised devices if the end-user has enabled Find My Device. The Setup Assistant will prompt the user to take action when the device is reset or remotely wiped.

Activation Lock provides administrators with more options for deterring theft of supervised devices. However, most corporate administrators are likely to leave Activation Lock disabled because it is primarily a consumer feature. The following table summarizes the options for corporate-liable deployments:

| Device Type                     | Result                                                           |
| ------------------------------- | ---------------------------------------------------------------- |
| Corporate-liable and supervised | - Activation Lock is disabled for supervised devices by default. |

- Device users cannot turn on Activation Lock.                                                                                                                                                                                                                                                 |
  \| Corporate-liable and unsupervised | \* Activation Lock will be enabled as soon as the end-user signs in to iCloud with their Apple ID and turns on Find My Device.
- MDM servers, including Ivanti Neurons for MDM, cannot control Activation Lock on unsupervised devices. Device users can lock activation with their personal credentials, leaving you no recourse should they leave the company. |

## Enabling the iOS Activation Lock

**Applicable to:** iOS 7+ Supervised

This configuration will be applied to Supervised devices (iOS 7 and later) that have the [**Find My**](https://www.apple.com/icloud/find-my/) feature enabled. If an administrator or other user tries to Wipe, Activate, or disable Find My Device on the device, an Apple Activation Lock screen will be displayed. To proceed, iTunes credentials or a Bypass code must be entered.

The Bypass code for Supervised devices will be stored upon activation and can be viewed in device details. The Bypass code can be sent remotely using the "Clear Activation Lock" command for Supervised devices. However, the code must be entered manually when reactivating a device or turning off the Find My Device feature.

You can only create one Activation Lock Configuration for all spaces.

## Enable the iOS Activation Lock feature on supervised devices

**Procedure**

1. Enable the **Find My** feature on your device.
2. Go to **Configurations**.
3. Select the **Apple Activation Lock** configuration from the list of existing configurations.
4. Click **Edit**.
5. In the iOS 7+ Supervised section, click **Enable Activation Lock**.
6. Click **Done**.
7. Register the device.

## Enabling the macOS Activation Lock

**Applicable to:** macOS 10.15+ Supervised

This configuration will be applied to Supervised devices with macOS 10.15 and later. Activation Lock on macOS only applies to Macs that have an Apple T2 Security Chip. On Supervised devices, whether upgraded or freshly installed, and on upgraded currently registered devices, Activation Lock is off by default. Enabling Find My does not automatically enable Activation Lock on these devices

If an administrator or other user tries to Wipe, Activate, or disable Find My feature on the device, an Apple Activation Lock screen will be displayed. To proceed, iTunes credentials or a Bypass code must be entered. The Bypass code for Supervised devices will be stored upon activation and can be viewed in device details. The Bypass code can be sent remotely using the "Clear Activation Lock" command for Supervised devices. However, the code must be entered manually when reactivating a device or turning off the Find My feature.

You can only create one Activation Lock Configuration for all spaces.

## Enable the macOS Activation Lock feature on supervised devices

**Procedure**

1. Enable the Find My feature on your device.
2. Go to **Configurations**.
3. Select the **Apple Activation Lock** configuration from the list of existing configurations.
4. Click **Edit**.
5. In the macOS 10.15+ Supervised section, click **Enable Activation Lock**.
6. Click **Done**.
7. Register the device.

## Using the iOS Activation Lock bypass code

When the device is wiped with the iOS Activation Lock enabled, the bypass code is retained on the Apple Activation server and in the Ivanti Neurons for MDM Admin interface.

**Procedure**

1. Go to **Devices**.
2. Select the device.
3. Click **Actions > Wipe**. It may take a few minutes before the device restarts.
4. When the device prompts you for the Apple ID and password leave the **Apple ID** empty.
5. Enter the bypass code in the **password** field.
6. Click **Next**.  
7. Proceed with the setup.

## Clearing the iOS Activation Lock bypass code

When the iOS Activation Lock is cleared in the Ivanti Neurons for MDM Admin interface, the bypass code is removed from the Apple Activation server, but it is still present in the device details in the Ivanti Neurons for MDM Admin interface.

**Procedure**

1. Go to **Devices**.  
2. Select the device.
3. Select **Configurations**.
4. Select **Apple Activation Lock**.
5. Click **Edit**.
6. In the iOS 7+ Supervised section, disable **Enable Activation Lock**.
7. Click **Done**.
8. Go to **Devices**.  
9. Select the device.
10. Click **Actions > Wipe**. It may take a few minutes before the device restarts. The device can now be setup with the new user's AppleID and password. 
11. Proceed with the setup.

The status of the clear iOS Activation Lock is displayed on the interface as follows:

| State   | Result                                                           |
| ------- | ---------------------------------------------------------------- |
| Pending | - Server is sending the Clear Activation Lock code to Apple.     |
| Sent    | \* Apple acknowledges receipt of the Clear Activation Lock code. |
| Failed  | - The server was unable to send the code to Apple.               |

- Apple has reported an error. |
