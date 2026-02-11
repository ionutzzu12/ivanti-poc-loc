---
title: Using Bulk Enrollment for Windows devices
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

The Bulk Enrollment feature enables you to quickly register multiple Windows devices with Ivanti Neurons for MDM.

**Prerequisites:**

- User accounts must be imported on Ivanti Neurons for MDM using Entra ID (Entra ID) Premium Account.
- All devices should have [**Windows Configuration Designer**](https://docs.microsoft.com/en-us/windows/configuration/provisioning-packages/provisioning-install-icd) installed.

**Procedure:**

::::WorkflowBlock
:::WorkflowBlockItem
Link the Ivanti Neurons for MDM and Entra ID tenants. See [**Connecting Entra ID to UEM for Windows 10 Devices.**](./Using_Microsoft_Azure.md)
:::

:::WorkflowBlockItem
Open the **Windows Configuration Designer** app and select **Provision desktop devices**. A New project window appears on the screen.
:::

:::WorkflowBlockItem
Enter the following details:
:::

:::WorkflowBlockItem
- Name - A unique name for your project
- Project folder - Location on the device where you want to save the project
- Description - Optional description of the project
  Click **Finish** to close the new project window and perform a sequence of steps.
:::

:::WorkflowBlockItem
**Set up device**

Enter a unique name for your devices. The name can include a serial number (%SERIAL%) or a random set of characters.
:::

:::WorkflowBlockItem
Optionally you can enter a product key if you are upgrading the Windows, configuring the device for a shared use, or removing pre-installed software.
:::

:::WorkflowBlockItem
**Set up network**

Optionally you can configure the Wi-Fi network devices to connect to when they first start. If the network devices are not configured, a wired network connection is required when the device is started first.
:::

:::WorkflowBlockItem
**Account Management**

Select **Enroll in Entra ID**, enter a **Bulk Token Expiry** date, and then click **Get Bulk Token**.
:::

:::WorkflowBlockItem
Enter your Entra ID credentials to get a bulk token.
:::

:::WorkflowBlockItem
In the **Stay signed in to all your apps** page, click **No, sign in to this app only**.
:::

:::WorkflowBlockItem
- Click Next when Bulk Token is fetched successfully and Create the Package.
- A user with provisioning package is created in the Azure portal - User principal name (like [**package\_0ea893a5-1e93-4d21-a6b1-dc788946fd1d@miwinqe.onmicrosoft.com**](mailto\:package_0ea893a5-1e93-4d21-a6b1-dc788946fd1d@miwinqe.onmicrosoft.com)). Copy the file (runtime ppkg tool) to a storage device.
  The Entra ID user for creating bulk token, and the package user should not have MFA enabled. To verify, you need to perform OOBE + Entra ID join on that user.

Recreate or synchronize the package user (created in Azure) to Ivanti Neurons for MDM.
:::
::::

Bulk enroll a device with a flash drive contained the provisioning package. You can also double-click on the existing device to perform post-OOBE experience. If the package failed to install in the first attempt, the second attempt also fails. Check if the new device is created in Ivanti Neurons for MDM and Entra ID belongs to the package user.
