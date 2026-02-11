---
title: Pushing SyncML to Devices using Custom Configurations
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

You can create your own Synchronization Markup Language (SyncML) configuration files or get them from a third party source to implement custom features by adding them to a custom configuration.

Supported platforms:

- Windows

**Supported devices:**

- Windows 10+
- Microsoft HoloLens 2

**Procedure**

1. Go to **Configurations**.
2. Click **+Add**.
3. Click **Custom Configuration** to display the **Create Custom Configuration** page.
4. Enter a name for the configuration.
5. Click the Windows OS icon.
6. Drag and drop the SyncML file in the interface or click **Choose File** to navigate to the file to select for uploading to the device.Ivanti Neurons for MDM does not perform any validation checks on the code in the file.
7. Click **Next**.

**Custom SyncML Log**

The SyncML commands sent to Windows device and SyncML responses on these commands from the device can be viewed under the Device Logs tab. This log information will be available after sending the **Windows Custom SyncML** configuration. When the system sends a Custom SyncML configuration, it has the "Installed" status always on the device "Configuration" tab for the configuration irrespective of the SyncML responses.
