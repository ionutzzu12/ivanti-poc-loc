---
title: Device Logging configuration
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

The Device Logging configuration allows you to enable network and security logs for Android devices.

### Creating a Device Logging configuration

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Select **Configurations**.
:::

:::WorkflowBlockItem
Click **+ Add**.
:::

:::WorkflowBlockItem
In the search field, type **Device Logging** and select the configuration.
:::

:::WorkflowBlockItem
Enter a name and describe the configuration.
:::

:::WorkflowBlockItem
Under the **Configuration Setup** section, select one or both options:
:::

:::WorkflowBlockItem
- Enable Network Logging
- Enable Security Logging
  For information on supported Android versions for Security and Network logging, refer to the tables under **Security Logging matrix** below.

Under the **App Usage** section, select **Enable Application usage data collection** option to collect data usage information. Enabling this option requires the user to allow the permission to collect data usage on the device.
:::

:::WorkflowBlockItem
- Collect Application Usage data - Select to collect the application usage data for apps in App Catalog
  App Usage data is collected once a day and shows the previous day's usage. The Present day usage is not reported. End users will be requested to provide permission to retrieve this information. Some device manufacturers may allow pre-granting this permission on Fully Managed devices using OEMConfig (Managed Configurations). This feature requires a Secure UEM Premium license.

Some device manufacturers may allow pre-granting this permission on Fully Managed devices using OEMConfig (Managed Configurations).
:::

:::WorkflowBlockItem
Click **Next** to configure the distribution settings.
:::

:::WorkflowBlockItem
Click **Done**.
:::
::::

**Security Logging matrix**

| Device type                                                      | Supported Android versions |
| ---------------------------------------------------------------- | -------------------------- |
| Work Managed Devices and Work Managed Device Non-GMS mode (AOSP) | 7, 8, 9, 10, 11, 12, 13    |
| Managed Devices with Work Profile                                | 8, 9, 10                   |
| Work Profile                                                     | NA                         |
| Work Profile on Company Owned Device                             | 11, 12, 13                 |

**Network Logging matrix**

| Device type                                                      | Supported Android versions |
| ---------------------------------------------------------------- | -------------------------- |
| Work Managed Devices and Work Managed Device Non-GMS mode (AOSP) | 8, 9, 10, 11, 12, 13       |
| Managed Devices with Work Profile                                | 8, 9, 10                   |
| Work Profile                                                     | 12, 13                     |
| Work Profile on Company Owned Device                             | 12, 13                     |

After installing the Device Logging Configuration on the device, the user gets a notification which has info about the Device management and Network logging. Click **OK** to acknowledge the notification.

### Requesting Debug Logs

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Log in to the Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Go to **Devices** > **Device details**.
:::

:::WorkflowBlockItem
From the **Overview** section, click on the three vertical dots button next to the **Force Checkin** button.
:::

:::WorkflowBlockItem
Select **Request Debug Logs**.
:::

:::WorkflowBlockItem
Select one of the following two options:

- Exclude Bug report - When you select this option and click Next, a confirmation window appears on the screen. Click **Request Debug Logs**. Users do not have to provide any consent for this option, and these logs would exclude bug report for the selected Android devices.
- Include Bug report - When you select this option and click Next, a confirmation window appears on the screen. Click **Request Debug Logs**. Users must provide consent for sharing the bug report. In the case of Android devices, users will be prompted to submit the device logs, to include bug report.
:::
::::
