---
title: Deleting Apps from the App Catalog
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

You can delete public and in-house apps from the App Catalog. You cannot delete prerequisite apps. You need to edit the apps to remove the prerequisite relationships before deleting such apps. If the app is installed on devices, it will be removed the next time those devices check in. Silent app install/uninstall is supported on Samsung and Zebra devices in Device Admin mode, or all devices in Device Owner mode.

In the case of in-house apps, a confirmation window appears on the screen. You need to select the acknowledgment that you want to continue with the Delete operation and click **Delete App**. When you try to delete multiple apps and some apps cannot be deleted, a window appears on the screen which contains information about the apps that cannot be deleted and the reason for that.

The following conditions apply when you try to delete one or more apps from the App Catalog: 

- If one version of the in-house app cannot be deleted, then it is not possible to delete any version.
- If one version of the in-house app is a prerequisite app, then the app cannot be deleted and none of the versions can be deleted.
- When you select all or some of the in-house apps to delete them from the App Catalog, all the versions of the selected in-house apps will be deleted.
- An in-house app delegated from a Space cannot be deleted.

**Procedure**

1. Go to **Apps > App Catalog**.
2. Click the link for the app.
3. Select **Actions > Delete from Catalog**.
4. Read the warning that explains what happens when you delete an app.
5. The warning explains that Apps and Books licenses (iOS) and app reviews (all OSes) are also deleted.
   Select the "I understand the consequences of deleting an app" check box to proceed with the delete operation.
6. Click **Delete App**.
