---
title: ChromeOS Blueprint Configuration
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

The ChromeOS Blueprint Configuration has the following settings:

- Device settings
- User and browser settings
- Managed guest session settings

You can apply ChromeOS configuration on specific User Groups (also referred to as Organizational Units). When you try to distribute the ChromeOS Blueprint Configuration, only the User Groups section will be available, and all the LDAP User Groups that are also associated with the authorized Google Admin Console will be listed under the section. You can select one or more from the listed groups and apply the configuration.

**Procedure**

1. Go to **Configurations > Add**.
2. Select **Google ChromeOS** under the OS section. The **ChromeOS Blueprint configuration** tab appears on the screen.
3. Click **ChromeOS Blueprint**. The **Create ChromeOS Blueprint Configuration** page appears on the screen.
4. Enter a name for the configuration in the **Name** box.
5. Under the Configuration Setup, you can modify the Device Settings, User and browser settings, and Managed guest session settings, as needed and toggle the "Push to device" button to apply the modified settings.
6. Click **Next**.
7. Select **Custom** for the distribution options.
8. Only the LDAP User Groups will be available to distribute the configuration.
   In the case of distributing the configuration to everyone, it can be done only for the LDAP User Groups available in Ivanti Neurons for MDM and Google Admin Console.
   Select one or more groups and click **Done**.

When the distributed settings are undistributed, the applied settings will not be reverted.

You can upload files in ChromeOS Blueprint Configuration.
