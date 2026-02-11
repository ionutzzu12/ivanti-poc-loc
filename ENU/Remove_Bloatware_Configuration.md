---
title: Remove Bloatware Configuration
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

Remove Bloatware configuration allows you select the list of applications installed in devices which needs to be forcibly removed. It is a prerequisite to have a Bridge setup for this configuration. See [**Bridge**](./Ivanti_Bridge.md) for more details.

To run or uninstall apps:

1. In the **Configuration** tab click **+Add**.
2. Select **Remove Bloatware** configuration. The **Remove Bloatware Configuration** page is displayed.
3. In the **Name** field, type an appropriate name for the configuration.
4. Click the +**Add Description** link to add a description for the configuration.This field is optional.
5. In the **Configuration Setup** section, select the apps that should be removed or uninstalled. You can alternatively search for an app in the Search field using the App name displayed in Desktop-apps list.Before creating the **Remove Bloatware** configuration, you should fetch apps by going to **Apps>Desktop Apps>Fetch Apps**. If not, no applications will be available to search or choose from when creating the **Remove Bloatware** configuration.The file types .appx,.appxbundles,.xap and .msi can be removed but not the file type .exe.
6. In the Advanced options, configure the following options:|                                            |                                                                                  |
   \| ------------------------------------------ | -------------------------------------------------------------------------------- |
   \| Option                                     | Description                                                                      |
   \| **Run this configuration every**           | Set the interval duration (in minutes) after which the configuration should run. |
   \| **Run at Logon**                           | Select the checkbox to run the configuration at logon.                           |
   \| **Suppress force restart after uninstall** | Select the checkbox to prevent force restart after uninstalling the app.         |
