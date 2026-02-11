---
title: Unlocking a Device
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Unlocking Android devices**](./Unlocking_a_Device.md)
- [**Unlocking AppConnect for Android apps**](./Unlocking_a_Device.md)
- [**Unlocking an iOS device**](./Unlocking_a_Device.md)
- [**Unlocking ChromeOS devices**](./Unlocking_a_Device.md)

To unlock a device:

You can clear the screen lock on a device. Unlocking works somewhat differently on different devices.

**Procedure**

1. Go to **Devices > Devices**.
2. Select the devices.
3. Click **Actions**.
4. Select **Unlock**.
5. Alternatively, click the device name link to go to the Device details page and click the **Unlock**

::Image[]{src="Unlock_device_icon.png" signedSrc="Unlock_device_icon.png" size="10" caption alt isUploading="false" sha initialPath="Unlock_device_icon.png" githubPath="Unlock_device_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
icon and click **OK**.
:::

## Unlocking Android devices

When an Unlock command is received, the Android app attempts to reset the passcode. In the Device Admin and Device Owner modes, the unlock code is reset, whereas in the Profile Owner and Company Owned Personal Enabled modes, the work profile unlock code is reset.

Unlock command provides an option for the administrator to set the unlock code with a combination of alphanumeric characters. The default option, which sets the unlock code to '0000' can be performed on multiple devices. However, the new option, Custom unlock code for Android, can be performed on one device at a time. The minimum number of characters should be 6 and maximum should be 8. This option is available under the **Actions** tab, as well as in the **Device Details** page. When you select the Unlock option from **Actions** tab or from the **Device Details** page, you can see the following two options.

- Default
- (Android only) Provide an unlock code - You can provide an Unlock code from this section and click **Unlock**.\* Skip passcode reset prompt on device - Select to skip resetting the passcode if the passcode configuration is pushed to a device.

After setting the unlock code, the administrator can find the unlock code in the **Audit Trials** page and **Device Logs** page.

The Directboot unlock works only for default unlock option, '0000' unlock code. The custom unlock code for direct boot is not supported.

## Unlocking AppConnect for Android apps

For AppConnect apps, the **AppConnect Unlock** command helps to unlock containers that have been locked due to users trying to log in multiple times with incorrect passcodes. This unlock does not unlock the device.

## Unlocking an iOS device

When an Unlock command is received, the iOS app removes the passcode from the device. If the [**passcode configuration**](./Passcode_Configuration.md) specifies that a new passcode is required, then the device user will be prompted to set a new passcode that complies with the rules defined in the passcode configuration. The user must make this change within 60 minutes or the app will force the user to set the new passcode.

## Unlocking ChromeOS devices

When a ChromeOS device is selected and the **Unlock** option is clicked, a pop up window appears on the screen - "Unlocking may clear an existing passcode to enable a user to access the device. Unlocking differs by platform." Click **Unlock** and the device status will be updated to "Unlock Sent", and the updated status will be visible after periodic device sync.
