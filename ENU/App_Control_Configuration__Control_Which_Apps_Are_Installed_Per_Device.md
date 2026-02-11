---
title: App Control Configuration: Control Which Apps Are Installed Per Device
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

The App Control configuration allows you to categorize apps as Allowlist or Blockedlist at the device level. Apps that are already installed will not be visible and cannot be launched. Apps will still be visible in the App Store, but they cannot be downloaded or launched. Any device to which this configuration is distributed will use this configuration and ignore any Allowed Apps Policy settings. This configuration supersedes any app-related policies that reference the same applications on the target devices.

This configuration supersedes any app-related policies that reference the same applications on the target devices. For Windows 10 devices, restrictions happen at the device level, therefore a configuration is the only way to enforce app rules.

The App Control configuration allows you to create a:

- **Allowedlist:** Only allow Apps that are explicitly added to this list. No other apps will be able to be installed on devices.
- **Blockedlist:** Disallow specific apps from being installed on devices.

**Supported Devices**

You can use the App Control configuration to Blockedlist or Allowlist different apps on the following devices:

- Android Work Profile on Company Owned devices
- iOS 9.3+ Supervised only
- tvOS 11+
- Windows

## Create App Control Configuration

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**
3. Enter **App Control** in the resultant **Choose Configuration** field, and then select the **App Control** configuration.
4. Enter name and description for the configuration.
5. Select an OS and then continue below at the section that applies to your OS.

### Android Work Profile on Company Owned devices

Users can add upto 50 application IDs to the Allowlist or Blockedlist group.

**Procedure**

1. Select **Create a Allowedlist for Personal Apps** or **Create a Blockedlist for Personal Apps** to add the list of appropriate applications to be Allowlisted or Blockedlisted.
2. Enter the application ID (com.example.com) and click Add.
3. Click **Next** and select a distribution option.
4. Click **Done**.

### iOS 9.3 supervised devices

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Choose whether to create a Allowedlist or Blockedlist.
:::

:::WorkflowBlockItem
Click **Add Apps**.
:::

:::WorkflowBlockItem
Choose the apps to Allowedlist or Blockedlist by clicking one or both of the following tabs:
:::

:::WorkflowBlockItem
- Click **Add by Lookup** to search for and choose apps from the App Store or App Catalog.
- Click **Add Manually** to choose apps by entering the Apple bundle ID (starts with "com.apple") for Apple System apps only.
  Click the **Allowedlist** or **Blockedlist** tab to review the list of chosen apps to be Allowedlist or Blockedlisted.
:::

:::WorkflowBlockItem
(Optional) Select the **Include all Webclips** option.
:::

:::WorkflowBlockItem
Click **Next** and then choose a distribution option.
:::

:::WorkflowBlockItem
Click **Done**.
:::
::::

### Windows devices

**Procedure**

1. Select **Allowed** or **Disallowed** to add the list of appropriate applications to be Allowlisted or Blockedlisted.
2. Under the **Rule Definition** section, select the **App Type** from the list.
3. Enter an identifier name in the **App Identifier** box to search for a specific app. You can also use the **Lookup Apps** link to open a new dialog and search for Windows-specific app identifiers.
4. (Optional) Enter some description about the app in **App Description** box.
5. Use **+Add** link to add more rule definitions to Allowlist or Blockedlist the apps.
6. Click **Next** and select a distribution option.
7. Click **Done**.
