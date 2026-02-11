---
title: Setting firmware password
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** macOS 10.13 or supported newer versions.

The administrator can set or update the firmware (EFI) password for a macOS device. A firmware password prevents starting up of the macOS device from any internal or external storage device other than the startup disk selected by the device user. As a result, it also blocks the ability to use most startup key combinations.

**Procedure**:

::::::WorkflowBlock
:::WorkflowBlockItem
Go to **Devices**.
:::

:::WorkflowBlockItem
To set or change the firmware password for a single device:
:::

:::::WorkflowBlockItem
::::WorkflowBlock
:::WorkflowBlockItem
Click the user name the device is associated with to view the device details page.
:::

:::WorkflowBlockItem
In the General section, expand **Firmware Password** and click **Set Password** or click **Set/Change Firmware Password&#x20;**&#x66;rom the device Actions menu.
:::

:::WorkflowBlockItem
The following information is displayed in this section:

1. **Password:** Password or a list of probable passwords.When an admin sets the firmware password, the command is sent to the device. If the device does not respond in time, the password is stored temporarily and displayed in this field. The new password will not take effect until there is an acknowledgment from device and the device gets restarted. Till then, all probable passwords are displayed. After the device is restarted and the password change is acknowledged, then all the unwanted passwords are cleared.
2. **Change Pending -** Indicates if the password change is pending.
3. **Command Status -&#x20;**&#xA0;Indicates if the password change was success or failure.
4. **Allow OptionROMs -** Indicates whether option ROMs are to be enabled. By default, it is set to No.
:::
::::

To set or change the firmware password for more than one device:
:::::

:::WorkflowBlockItem
1. Select the devices.
2. From the Actions menu, click **Set/Change Firmware Password**.
   Enter the current and the new passwords.If it's the first time, the current password can be left blank.To reset the password, leave new password field blank.
:::

:::WorkflowBlockItem
Click **Save**.
:::
::::::

Only devices with supported macOS versions will be updated with new password. Unsupported devices will be skipped.
