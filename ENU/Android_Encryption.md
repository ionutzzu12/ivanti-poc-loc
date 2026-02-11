---
title: Android Encryption
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

An encryption configuration defines device encryption requirements for Android devices in Device Admin mode. Device encryption ensures that sensitive corporate data cannot be accessed by known jailbreak or root exploits. Encryption stores the device's data in an unreadable form so that anyone who might steal the device cannot access the data.

Enabling encryption prompts the device user to encrypt the device and requires setting a device passcode. The passcode is what decrypts the data so that you can read it. Device encryption is automatically enabled on Android enterprise (work profile or managed devices) or iOS devices when a passcode is set. The device cannot be used while it is being encrypted. Once encryption is on, turning it off requires a factory reset of the device.

## Encryption settings

| Setting                  | What To Do                                                                                                           |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| Name                     | Enter a name that identifies this configuration.                                                                     |
| Description              | Enter a description that clarifies the purpose of this configuration.                                                |
| Enable Device Encryption | Select the setting to turn on encryption for all encryption-capable Android devices that receive this configuration. |

Android Encryption Configuration is deprecated for Samsung devices in Device Admin mode on Android 11. This encryption is supported by default on Android Enterprise devices when a device passcode is set.
