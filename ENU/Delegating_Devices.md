---
title: Delegating Devices
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Spaces are used to separate your devices into independently managed entities. Membership for Spaces is determined by rules you create. Device delegation allows a Global Admin to partition and independently manage devices in an UEM system. When devices are delegated, access to those devices can be assigned to a subset of delegated administrators, thus distributing admin responsibilities.

Delegated devices can be grouped into device groups and different custom configurations can be applied to them without affecting devices in the default Space or other Spaces.

## Creating rules for delegating devices

The rules you define for a Space determine which devices belong to the Space. A device can belong to only one Space. Devices that do not match the rules for the Spaces you create automatically belong to the default Space.

1. Select **Any** if you want devices to be included in this definition if they meet any of the rules.
2. Select **All** if you want devices to be included in this definition only if they meet all of the rules.
3. Select one of the following rule types from the dropdown:\* **Custom LDAP Attribute:** For rules based on LDAP attributes.
   - **OS**: For rules based on the device's operating system.
   - **User Group**: For rules based on the device's user group (as defined in the device management service).
   - **Username**: For rules based on the username associated with the device.
4. Define the criteria for the selected rule type:- **Custom LDAP Attribute:** Enter the name of the custom LDAP attribute that was configured in the LDAP settings.
   - **OS**: Select Android, iOS, macOS, or Windows.
   - **User Group**: Select one of the user groups displayed in the dropdown. These are the user groups defined under **Users > User Groups**.\* **Username**: Type in a username.
5. To add another rule for this Space, click the + next to the previous rule.
6. Click **Preview** to see which devices will be assigned to the Space.
7. Click **Save** when you are satisfied with the devices in the Space.

Devices that no longer match the rules for a Space are automatically moved to the next matching Space. If the device does not match the rules of an existing Space, then the device moves to the Default Space. For example, removing a user from a user group can cause that user's devices to move to a different Space. Moves to a different Space can result in changes in policies and configurations.
