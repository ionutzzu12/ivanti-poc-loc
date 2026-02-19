---
title: Windows 10 Update Management
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

As an administrator, you can view and approve the updates reported by Windows 10 devices that you want to be updated using Windows 10 Update Management. By using this feature you can prevent unnecessary or untested updates from being installed in devices.

Update Management feature requires devices to be configured with **Software Updates** configuration with **Require update approval** option enabled. Only by applying this configuration to the devices, the devices report updates for installation and wait for approval.

## Managing updates

::::WorkflowBlock
:::WorkflowBlockItem
Go to the **Admin>Windows Updates**. The following details of the updates are displayed in the page.**Creation Date**: The date when the update was created.**Title**: Describes the type of update along with the Knowledge Base article number.When clicked on the update, the description is displayed.**Classification**: Classifies the type of update into one of the following categories:\* Critical Updates

- Definition Updates
- Driver Updates
- Security Updates
- Updates
- Upgrade
- Update Rollups**Distribution**: The distribution performed for the update. For example, it display **All** when the update is distributed to all the devices.If the update is distributed to a certain specific number of groups, it displays the count of the distribution. For example, it displays 3 if the distribution is performed only to 3 groups.
:::

:::WorkflowBlockItem
In addition, you can view if an update has been distributed to the required devices or not. The following columns have numbers that indicate the number of devices present under different category of the updates: 

- Eligible devices
- Installed devices
- Failed devices
- Reboot pending devices
  When you click on any of these numbers, you will be directed to the filtered view on the Devices page to know the status of updates and perform the required actions.

Review the updates and select the update that you would like to distribute to the devices by clicking the check-box for the update.
:::

:::WorkflowBlockItem
Under **Actions**, click **Set Distribution**.
:::

:::WorkflowBlockItem
In the **Distribute Windows Update** window, select any of the following distribution options:**All Devices**: Distributes the updates to all the devices.**No Devices**: Withholds the updates to be distributed to devices**Custom**: Distributes the updates for the specified device groups.
:::

:::WorkflowBlockItem
Click **Save**.
:::
::::

## Searching and filtering updates

You can search and filter updates based on the following criteria:

- Knowledge base article ID
- Configured distribution

Filtering based on Knowledge base article ID:

1. In the **Windows 10 Update Management** page, type the Knowledge base ID in the quick search field(only the number in the Search field.Example: For KB4056892, type 4056892. The update that matches with the search criteria is displayed on the page.You can further look for additional information on the update by clicking **Support** and **More Information** link. The **Support** links to the Microsoft web page that provides product support information for the update and the **More Information** links to the Microsoft web page that displays more information on the update, such as the Knowledge Base article.

Filtering based on configured distribution:

In the **Windows 10 Update Management** page, select any of the following filtering options based on the configured distribution:

- **All**: Displays all the updates.
- **Configured**: Displays the list of updates that are distributed to devices.
- **Unconfigured**: Displays the list of updates for which the distribution is not specified.Configured and Unconfigured filters are based on the distribution performed and the distribution can also be **None**.

## Viewing updates for a device

To view the detailed update information specific to a device:

1. Go to **Devices > Devices**.
2. Click a device name to view the details page.
3. Go to **Updates** tab. The updates for the device that are pending (update approved by the admin but not reported as installed on the device), failed, and installed are displayed.You can also see notifications about new Windows updates available in the Notifications page under Dashboard. The notification includes creation date of the notification, number of notifications available and the purpose of the notification. The Windows update notification is also visible in the top right corner of the Admin Portal.
