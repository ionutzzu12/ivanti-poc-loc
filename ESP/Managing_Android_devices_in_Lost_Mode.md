---
title: Managing Android devices in Lost Mode
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Enabling Lost Mode**](./Managing_Android_devices_in_Lost_Mode.md)
- [**Disabling Lost Mode**](./Managing_Android_devices_in_Lost_Mode.md)

## Enabling Lost Mode

**Applicable to:** Android 8+ devices

You can place multiple Android devices simultaneously in Lost Mode through Ivanti Neurons for MDM. This means you can report a lost device to Ivanti Neurons for MDM by placing the device(s) in Lost Mode, which allows you to show a custom message, phone number, and footnote on the screen, along with an option to play a sound.

This functionality supports only Fully Managed devices including Non-GMS devices.

**Procedure**

1. Go to **Devices**.
2. Select the checkbox for the device(s).
3. Select **Actions > Enable Lost Mode**.
4. Alternatively, click on the device name link to go to the Device details page and click the

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
icon. Select **Enable Lost Mode**.
:::

5. Enter a lock screen message or phone number or both to be displayed on the locked screen of the lost device(s). Admins can also select the footnote and **Play Lost Mode Sound** options. If someone finds the device(s), they can call the number to report it.Either a message or phone number must be entered in the respective fields to activate the **Enable Lost Mode** option.The Lost Mode sound will play for 5 minutes unless the phone is unlocked, the call button is pressed, or the Admin disables Lost Mode within that time. To replay a sound, re-enable Lost Mode on the device(s).
6. Select **Enable Lost Mode** to place the Android device(s) in Lost Mode.

Activating Lost Mode will disable the following actions:

- Unlock
- Enter/Exist Kiosk
- Force Logout for shared Kiosk
- Assign to User
- Send Message
- Set Ownership

Once the lost mode is enabled in a device, Lost Mode option in server will be disabled.

## Disabling Lost Mode

If a device(s) in Lost Mode is retrieved, or the Lost Mode was enabled in error, you can disable Lost Mode.

If the lost device(s) is wiped from Ivanti Neurons for MDM, disabling Lost Mode will not work.

**Procedure**

1. Go to **Devices**.
2. Select the checkbox for the device(s).
3. Select **Actions > Disable Lost Mode**.
4. Alternatively, click on the device name link to go to the Device details page and select **Lost Device Mode: Enabled > Disable Lost Mode**.

In the **Details** section, **Disable Lost Mode** becomes visible only after **Enable Lost Mode** is activated. Once **Disable Lost Mode** is activated, the **Lost Device Mode: Enabled** field, which includes the **Disable Lost Mode** option disappears.

Devices that were previously in Kiosk mode will need to be re-entered into Kiosk after Lost Mode is disabled.
