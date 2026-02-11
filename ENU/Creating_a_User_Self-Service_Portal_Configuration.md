---
title: Creating a User Self-Service Portal Configuration
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

As an enterprise user, you can use the Self-Service portal to manage your devices and certificates. The My Devices tab displays the devices that you have registered.

You can do the following tasks from the My Devices tab:

- Lock
- Unlock
- Retire
- Reset Secure Apps Passcode

You can perform the following tasks from the My Certificates tab:

- Upload Certificate

You can distribute a maximum of 100 configuration files at once.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrator portal.
2. Click **Add** .
3. Search for **Create User Self-Service Portal Configuration**.
4. Click **Next**.
5. If you do not want this configuration enabled immediately, clear the **Enable this configuration** option.
6. Select a distribution level for the configuration:\* **All Devices** - Distribute the configuration to all the available devices. To delegate configurations across spaces, select one of the following options:- **Do not apply to other spaces**.
   - To delegate configurations across spaces, select **Distribution Summary** > **Apply to devices in other Spaces**.\* Select the **Allow Space Admin to Edit the Distribution** check box to allow the delegated space administrators to edit the distribution for the specific space.
   - **No Devices** - select this configuration for distribution at a later point in time.
   - **Custom** - define specific set of devices that will have this configuration sent to them. To delegate configurations across spaces, select one of the following options:\* **Do not apply to other spaces**.
     - **Distribution Summary** > **Apply to devices in other Spaces**.\* Select **Allow Space Admin to Edit the Distribution** check box to allow the delegated space administrators to edit the distribution for the specific space.
7. If your service has Spaces defined, specify whether the configuration should be applied to the other Spaces, and the priority.
8. Click **Done**.

For configurations that issue a command to the device instead of installing a profile on the device, the configuration details will not list the configuration as applied to any devices.
