---
title: Editing the Android Enterprise default configuration
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

Global Administrators can allow space administrators to edit the distribution for any of the following Android Enterprise default configuration in custom space.

- Android Enterprise: Work Profile on Company Owned Device (Android for Work)
- Android Enterprise: Work Managed Device (Android for Work)
- Android Enterprise: Managed Device with Work Profile
- Android enterprise: AOSP

## Edit the distribution for any of the above configurations

**Procedure**

1. In the Configurations tab, select the configuration to be edited.
2. Click on the Edit icon.
3. Click **Next**
4. Select any of the following distribution levels to edit and configure from the distribution page:\* **All Devices**: Select one of the following options to distribute the configuration to all compatible devices:1) Do not apply to other spaces
   2\) Apply to devices in other spaces.
   - **No Devices** (default) 
   - **Custom**: Select one of the following options to distribute the configuration to all compatible devices or users:1) **User/User Groups**: Select the checkbox next to the users or user groups. Alternatively, you can type and search for the users or user groups.
     2\) **Device/Device Groups**: Select the checkbox next to the devices or device groups. Alternatively, you can type and search for the devices or device groups.In the **Distribution Summary**, select one of the following options to enable or disable configurations across spaces:•Do not apply to other spaces.•Apply to devices in other spaces.The checkbox **Allow Space Admin to Edit the Distribution** appears if you select the **Apply to devices in other Spaces** option, and it allows the delegated space administrators to edit the distribution for the specific space.If you edit the distribution option, you must select the checkbox "**I understand changing distribution of Android Enterprise-Device Mode Configuration can cause devices to retire or wipe if the configuration is removed from existing devices**."
5. Click **Done**.

When this configuration is applied to spaces, the Space administrators will be able to edit the distribution by clicking the distribute icon in custom space.
