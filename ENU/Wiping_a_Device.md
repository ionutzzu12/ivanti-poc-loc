---
title: Wiping a Device
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

Wiping a device removes all the data and returns the device to factory default settings.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Devices > Devices**.
:::

:::WorkflowBlockItem
Select the device.
:::

:::WorkflowBlockItem
Click **Actions** (upper right).
:::

:::WorkflowBlockItem
Select **Wipe**.
:::

:::WorkflowBlockItem
Alternatively, click on the device name link to go to the Device details page and click the

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start"}

icon. Select **Wipe** and click **OK**.
:::

:::WorkflowBlockItem
By default, the **Preserve Data Plan** option is selected.

(Optional, applicable to iOS 11.3+ devices) Select the **Skip Proximity Setup** option.
:::

:::WorkflowBlockItem
Select the **Enable Return to Service** option to automatically re-enroll after the data is erased, so that you don’t have to re-enroll the device manually after a wipe. Select **Wifi profile data** from the drop-down menu. The user needs to deactivate all activation locks. Currently this is applicable only for iOS 17+ devices enrolled in DEP mode.
:::

:::WorkflowBlockItem
For macOS devices, you can send a 6-digit PIN to the device as passcode. On the device, the user is prompted to enter the PIN to access the device. To proceed with the wipe action, the device user needs to:1) Enter the PIN.
2\) Select the check box to confirm the device wipe action.
3\) Click **Yes, wipe this device**.
:::

:::WorkflowBlockItem
For ChromeOS devices, when you perform a Wipe operation from the **Device Details** or **Device Listing** page, a pop up window "Wiping a device returns it to factory settings, which can result in a loss of data on the device. The Wipe action differs by platform." appears on the screen.

1. Select the "I understand that Wipe cannot be reversed" check box to confirm the device wipe action.
2. Click **Wipe** to wipe the device.
   The device status changes to "**Wipe Sent**." The updated device status will be visible after a periodic device sync.
:::
::::

On Android Enterprise devices, you can perform the **Wipe** device action even after the device reboots and remains locked.

Android devices that are in the **Wipe Pending** state can be deleted using the **Delete Device** option present on the **Device Details** page. Once a device is deleted, it loses connection to the server and becomes non-compliant. So the user must re-enroll the device after performing the factory reset.
