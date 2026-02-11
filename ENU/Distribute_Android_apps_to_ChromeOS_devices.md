---
title: Distribute Android apps to ChromeOS devices
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

The administrator can distribute Android apps from the App Catalog to ChromeOS devices.

**Prerequisites**

1. Android Enterprise must be configured. For information on setting up Android Enterprise, see [**Setting up Android Enterprise**](./Setting_up_Android_Enterprise.md).
2. Android apps must be present in the App Catalog.
3. Ensure that the ChromeOS device (Chromebook) user is part of a User Group (also referred to as Organizational Unit) before distributing Android apps and ChromeOS Blueprint Configuration.

Once the Android app is identified, you need to distribute the app following the similar process that you follow to distribute any other app. When you are distributing the Android app, make sure to select the User Groups to which you want to distribute the app and perform a Silent Install on the device.

If your existing Android app deployment is set to be distributed to devices / device groups or users, you will have to change the distribution to be based on User Groups. This can impact exising deployments if the app is already in use. It is recommended to do this on a completely new app first.

Install Settings allows administrators to control the final silent installation and it is required to push the app to ChromeOS devices. User Groups must be selected here.
