---
title: Windows Desktop restrictions
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to: Windows 10 Desktops**

This section contains the following topics:

- [**Configure Windows Desktop restrictions**](./Windows_Desktop_restrictions.md)
- [**Creating a Allowlist for removable storage devices**](./Windows_Desktop_restrictions.md)

Administrators can control OS information on managed Windows 10 Desktop devices by restricting user access to the following areas on a device:

- Control Panel
- Task Manager
- File Explorer
- Registry Editor

The above functions enables a user to make a lot of changes to their device. Using this feature, administrators have the ability to restrict access to these system level controls and thereby secure the access.

This feature requires Bridge. See [**Ivanti Bridge**](./Ivanti_Bridge.md) for details.

## Configure Windows Desktop restrictions

**Procedure**

1. Go to **Configuration > +Add**.
2. Select **Windows Desktop Restrictions** configuration.
3. Enter a name for the configuration.
4. Enter a description.
5. In the Configuration Setup section, specify the remaining settings as described in the following table.| **Setting**                       | **What To Do**                                                                                                                                                                                                                                        |
   \| --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Task Manager**                  | Select the **Deny access** checkbox for the setting for which the access should be denied.                                                                                                                                                            |
   \| **Control Panel**                 |                                                                                                                                                                                                                                                       |
   \| **Registry Editor**               |                                                                                                                                                                                                                                                       |
   \| **File Explorer**                 | Select the **Restrict Capabilities** checkbox to restrict capabilities of File Explore. Example: Removal of map network drive.Click on the link provided to view the list of capabilities that are restricted.                                        |
   \| **Removable storage**             |                                                                                                                                                                                                                                                       |
   \| Access mode for Removable Storage | \* **Restrict Read Access**: This prevents any access and is the most restrictive configuration.
   - **Restrict Write Access**: This allows limited access, but prevents unauthorized removal of data or the ability to add viruses, etc. to the device. |
6. Click **Next**.
7. Select one of the following distribution options:\* All Devices
   - No Devices(default)
   - Custom
8. Click **Done**.For the configuration to take complete effect, the device should be rebooted after applying the configuration.

## Creating a Allowlist for removable storage devices

If you want to create a Allowlist of permitted storage devices, complete the following steps first:

- Attach the USB storage devices you want to allow to a PC.
- Open Device Manager and click on the USB controller.
- Look at the settings for each controller for device information.
- Store the device information to use when creating your Allowlist.

To create Allowlist for removable storage device:

**Procedure**

1. In the **Windows Desktop Restrictions** configuration page, click **+Add** under **Allowlisted Removable Storage** section.
2. In the **Add hardware IDs** window, enter the hardware ID for one or more devices that you wish to remove from the Allow list and block as storage devices.
3. Click **Add hardware IDs**. The list of Allowlisted hardware IDs are displayed under **Allowlisted Removable Storage** section.To edit or delete a hardware ID from the list, select the Edit or Delete option under the **Actions** column.For the configuration to take complete effect, the device should be rebooted after applying the configuration.
