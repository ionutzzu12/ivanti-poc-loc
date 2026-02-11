---
title: Assigning a Device to a new user
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

An existing registered device may need to be re-provisioned for a new user, if there has been a role change for the user, or if the previous user's relationship to the company has changed. These steps help to avoid retiring  and re-registering the device.

**Procedure**:

1. Navigate to the device in the [**Devices page**](./Devices.md).
2. Click the device name to display the Device details page.
3. Click **Assign to user&#x20;**

::Image[]{src="Assign_user_icon.png" signedSrc="Assign_user_icon.png" size="10" caption alt isUploading="false" sha initialPath="Assign_user_icon.png" githubPath="Assign_user_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
icon.
:::

4. Alternatively, you can select a device from the **Devices** page, and click **Assign to user** option from the **Actions** menu.
   Start to enter the users name in the **Search User**... field.
5. Select the desired user.
6. Click **Assign to user**.The device will be provisioned for that user.

You may notice that in user-based and license-based scenarios, you can assign a device to a user who has exceeded the assigned device limit. This is because the intent of the device limit feature is to limit the registration of devices in support of Bring Your Own Device (BYOD) scenarios.

In both device-based and user-based licenses, enforcing the device limit is inconsequential. For device-based licenses, the cost to the end customer does not change because the total number of devices in the system does not change. For User-based licenses, the lack of this check actually benefits the customer. For example, consider five users, U1 through U5 with 5 devices each. With user-based licensing, this would consume five licenses. If instead, two of the devices from U4 and U5 are moved to U1 and U2, then license consumption goes DOWN, from five to three.
