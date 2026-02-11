---
title: Reassigning an Android device
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

The administrator can transfer the ownership of an Android device from one user to a different user. During the reassignment process, the device’s management profile will be reconfigured or remapped from the current user to new user in Android Enterprise mode. The reassignment can be done on all Android Enterprise devices except the Android Management API (AMAPI) devices and cannot be done on Google Domain Android Enterprise devices.

The device reassignment can be done only with the devices in same mode. For example, a device in Work Managed Device mode can be reassigned to another user in the same mode.

The device reassignment process will have the following statuses:

- Initiated
- Success
- Failed
- Pending

You can view the last reassignment status of a device under the **Device Details** page -> **Overview** tab -> **Last Reassignment Status**.

**Procedure**

1. Go to **Devices**.
2. Select one or more devices from the list.
3. From the **Actions** list, click **Assign to user**.
4. Alternatively, you can click on any device name. The **Device Details** page opens. Click the **Assign to User** icon to get the Assign to user screen and select the required user.
5. Click **Assign to user**. The selected options will be validated to check if the selected devices can be reassigned to the selected users or not.
   After successful validation and reassignment, a confirmation message appears on the screen.
   If you have selected a maximum number of 10 devices, then the "Assignment initiated" message appears on the screen. If you have selected 11 or more devices, then "Validation is in progress" pop up appears on the screen.

Android Device Reassignment is an innovative solution built uniquely with focus on eliminating data-left-overs from the previous registered user and is only available in SUEM-Premium SKU.
