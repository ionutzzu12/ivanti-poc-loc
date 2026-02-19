---
title: Apple App Catalog
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** iOS and macOS

The Apple App Catalog configuration manages access to the Apple App Catalog via a web clip. Starting from Ivanti Neurons for MDM release 83, you can transition to Apps\@Work native experience from Go application. For newly created tenants the Apps\@work Webclip configuration is not distributed by default for iOS devices that are installed through iReg or client. The administrator has to manually distribute the webclip config to the devices that are registered through iReg or client.

The Apps\@Work webclip search result displays only 10 applications on iOS and iPad devices even if the search request has rows parameter as more than 10.

**Procedure**

Admins can edit the distribution of this system-defined configuration as follows:

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Configurations**.
:::

:::WorkflowBlockItem
Click **Apple App Catalog**.
:::

:::WorkflowBlockItem
Click **Edit Distribution**.
:::

:::WorkflowBlockItem
Select one of the following distribution options:
:::

:::WorkflowBlockItem
- All Devices - all compatible devices will have this configuration sent to them.
- No Devices - disable access to Apple App Catalog or stage this configuration for later distribution.
- Custom - define specific device groups that will have this configuration sent to them.
  Click **Save**.
:::
::::
