---
title: Managed Google Play Configuration
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

Administrators can configure the automatic update setting that Google Play Store uses to update apps on the Android Enterprise device.

To configure auto-update settings:

1. Go to **Configuration \*\*\*\*> +Add**.
2. Select **Managed Google Play** configuration.
3. Enter a name for the configuration.
4. Enter a description.
5. In the Configuration Setup section, select an option to update apps from Google Play.|                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   \| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Setting**      | **What To Do**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
   \| **User Defined** | The device user can set the auto-update apps maintenance window setting to define when the apps should be updated.1) In the **Start Time** field, select the time to perform the app update.
   2\) In the **Duration** field, select the duration (in hours) within which the update should be performed. The minimum and maximum range is between 1 hour to 24 hours.The apps can be updated anytime between the start time to selected duration. For example, if the 'Start Time' is set as 6PM and the 'Duration' is set for 12hrs, the apps may be updated anytime from 6PM to 6 AM. |
   \| **None**         | Google Play Store never automatically updates apps on the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   \| **Wifi Only**    | Google Play Store automatically updates apps on the device but only using Wi-Fi, not cellular, connections.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
   \| **Always**       | Google Play Store automatically updates apps on the device using either Wi-Fi or cellular connections.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
6. Click **Next**.
7. Select one of the following distribution options:\* All Devices
   - No Devices(default)
   - Custom
8. Click **Done**.
