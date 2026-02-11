---
title: Exclude or Distribute apps
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

Exclude or distribute managed apps from a device without changing the app distribution configuration for in-house and public apps on iOS, macOS, and Windows devices. For all managed apps, these options are present in the **Actions** column of the **Available Apps** section for all devices.

### Permissions

To exclude or distribute an application to or from a device, you need to have the following authorizations:

- Access device in space (partition)
- Access the available apps for the device.

## Exclude

The exclude option for a selected app uninstalls and removes the associated data from the device. Follow the workflow to exclude a prerequisite app. A pop-up confirmation indicates that you are excluding a prerequisite app, resulting in the exclusion of the main app from the device.

If you exclude in-house apps with multiple versions, it then excludes all the undistributed app versions from the device. If you exclude an app from the device, it deletes from Apps\@Work and Ivanti Go. If you exclude and delete an app from the App Catalog and add again, the app will no longer remain excluded for the device. If you exclude a managed app from the device, it should be visible in the **Devices&#x20;**>**&#x20;Devices** > **Available Apps** list for the administrator to distribute the app after excluding it.

## Distribute

When the administrator triggers the **Send install** command from the app, the app will not install until the administrator decides to distribute it from the device's **Available Apps**. A new exclusion message appears for the devices that don't get the app. When the administrator distributes an available application, the next sync installs the distributed application on the device.
