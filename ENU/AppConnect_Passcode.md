---
title: AppConnect Passcode
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Changing/Resetting a passcode**](./AppConnect_Passcode.md)
- [**Generating a one-time PIN for resetting a secure apps passcode for iOS devices**](./AppConnect_Passcode.md)

You can require an AppConnect passcode, also known as the secure apps passcode. With a single login with the AppConnect passcode, the device user can access all the secure apps. On the Admin Portal, you configure the rules for the AppConnect passcode. The AppConnect passcode is not the same as the passcode used to unlock the device.

## Changing/Resetting a passcode

Users can change or reset the secure apps passcode in the Secure Apps Manager app for Android devices and in the Go for iOS app, provided it has been allowed in the AppConnect configuration. For iOS devices:

**Procedure**

1. Open the Go for iOS app.
2. Click **Secure Apps**.
3. Click **Authentication**.
4. Click **Change Secure Apps Passcode** and follow the instructions to change/reset the passcode.

For Android devices:

1. Open the Secure Apps Manager app.
2. Click **Change Passcode** in the options menu.
3. Click **Forgot Password** to reset the passcode.

## Generating a one-time PIN for resetting a secure apps passcode for iOS devices

Administrators can configure Ivanti Neurons for MDM to allow iOS device users to reset their secure apps (AppConnect) passcode when they forget it. When you have configured this option, device users who registered with Ivanti Neurons for MDM using a user name and password can enter those credentials in Go 3.1.0 for iOS or supported newer versions to authenticate themselves and then reset their secure apps passcode. However, device users who have forgotten the password and PIN need a different mechanism for authenticating themselves.

**Procedure**

1. On Ivanti Neurons for MDM, the administrator turns on the **Secure Apps Passcode** option in the Default iOS AppConnect Configuration (or in any other iOS AppConnect Configuration).
2. The user generates a one-time PIN for a specific iOS device on the self-service user portal by clicking the **Reset Secure Apps Passcode** option and following the instructions. The one-time PIN is valid for 30 minutes.
3. In Go for iOS on a device, the user follows the instructions for resetting a forgotten secure apps passcode.
4. When prompted for his user credentials, the user enters his user name and the one-time PIN instead of the regular passcode.
5. The user resets his secure apps passcode.
