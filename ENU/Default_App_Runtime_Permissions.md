---
title: Default App Runtime Permissions
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** Apps built targeting Android API 23+ and running Android 6.0+ on Android enterprise devices.

Administrators can set the runtime permission configuration for apps deployed to Android enterprise devices. Apps built targeting API 23 (or higher) and running Android 6.0 or later, are able to prompt users for permissions at runtime. The Default App Runtime Permissions configuration sets the default for these app runtime permissions. Ivanti Neurons for MDM creates this configuration by default. You can edit this default system configuration or create a new configuration based on your requirements.

The app-specific permissions take precedence over the general app permission configuration. In-house apps are subject to the global permissions. Setting the per-app permissions for in-house apps is not supported.

## Setting global runtime permissions

Administrators can edit the default app runtime permissions and the distribution of this configuration as follows:

Procedure**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Configurations**.
:::

:::WorkflowBlockItem
Perform one of the following actions:
:::

:::WorkflowBlockItem
- To edit the default system configuration, click **Default App Runtime Permissions** and click **Edit**.
- To add a new configuration, click **Add > Default App Runtime Permissions**.
  Enter a name for the configuration.
:::

:::WorkflowBlockItem
Enter a description.
:::

:::WorkflowBlockItem
In the Configuration Setup section, set one of the following default runtime permissions:
:::

:::WorkflowBlockItem
- User Prompt (default option)
- Auto Grant
- Auto Deny (Use with caution)
  Click **Next**.
:::

:::WorkflowBlockItem
Select the **Enable this configuration option**.If you deselect this option, this configuration will not be applied to any devices. It will be removed from all devices if it was previously applied.
:::

:::WorkflowBlockItem
Select one of the following distribution options:
:::

:::WorkflowBlockItem
- All Devices
- No Devices (default)
- Custom
  Click **Done**.
:::
::::

## Setting app-specific runtime permissions

Administrators can set the default runtime permissions for an individual application as follows:

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Apps**.
:::

:::WorkflowBlockItem
Click the name of the app.
:::

:::WorkflowBlockItem
Click **App Configurations > Android enterprise**.
:::

:::WorkflowBlockItem
Click **Add** or click the configuration name to edit an existing configuration.
:::

:::WorkflowBlockItem
Set the configuration options such as a name, description, and restrictions.
:::

:::WorkflowBlockItem
In the Runtime Permissions section, click **Manage Permissions**.
:::

:::WorkflowBlockItem
Select the permissions in the displayed window and click **Select**.Only the dangerous permissions that are applicable to the specific application are listed for selection. The complete list of dangerous permissions (such as read your contacts, find accounts on the device, write call log, and so on) are listed at [**https://developer.android.com/guide/topics/permissions/requesting.html#perm-groups.**](https://developer.android.com/guide/topics/permissions/requesting.html#perm-groups)
:::

:::WorkflowBlockItem
- The permissions are applied only when the application requests permissions.
- The permissions are not applied if the users have previously accepted or denied permissions.
  In the Runtime Permissions section, select one of the following default runtime permissions:
:::

:::WorkflowBlockItem
- Default/Global (default option)
- Auto Grant
- Auto Deny (Use with caution)
  In the Distribute this App Config section, select one of the following distribution options:
:::

:::WorkflowBlockItem
- Everyone with App
- No One
- Custom
  Click **Save**.
:::
::::
