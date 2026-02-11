---
title: Ivanti Bulk Enrollment
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

Administrator can enroll multiple Windows devices with generic user (via ppkg) that starts with prefix **windows-bulkenroll**, and later do the user assignment.

**Prerequisites:**

- On the Ivanti Neurons for MDM, create a user account with prefix as **windows-bulkenroll**. For example, **windows-bulkenroll**[**-user1@abc.com**](mailto:-user1@abc.com), **windows-bulkenroll**[**-user2@abc.com**](mailto:-user2@abc.com).

**Creating PPKG package with Windows Configuration Designer**

::::WorkflowBlock
:::WorkflowBlockItem
Download and install the **Windows Configuration Designer**.
:::

:::WorkflowBlockItem
Create new project.
:::

:::WorkflowBlockItem
Click on **Provision Desktop**.
:::

:::WorkflowBlockItem
Enter the name of the project, and select a path.
:::

:::WorkflowBlockItem
In the **Set up device** section, enter device name.
:::

:::WorkflowBlockItem
In the **Set up network** section, enter network name (to setup network, if needed or can be disabled).
:::

:::WorkflowBlockItem
In the **Account Management** section, select **Enroll in Local Admin**. Enter **User name** and **Password**, and click **Next**.
:::

:::WorkflowBlockItem
In the **Add applications** section, click **Next**.
:::

:::WorkflowBlockItem
In the **Add certificates** section, select **Switch to advanced editor**, and click **Proceed** > **Yes**.
:::

:::WorkflowBlockItem
Go to **RuntimeSettings** > **Workplace Enrollments**. Enter **UPN** (same user created on Ivanti Neurons for MDM in the prerequisites section). Select the following options: 
:::

:::WorkflowBlockItem
- AuthPolicy: OnPremise
- DiscoveryServiceFullUrl: Enter the Leo url
- Secret: Enter the Password
  Click **File** > **Save**.
:::

:::WorkflowBlockItem
Click **Export** > **Provisioning Package**.
:::

:::WorkflowBlockItem
Click **Next** on subsequent screens, and click **Build**.

The ppkg file is saved in the specified location.
:::
::::

**Provision device in OOBE mode with ppkg**

Provision the devices with the newly created ppkg package file from the above section. Once the device gets enrolled and checkin is successful, you will find the device entry on MDM server with the user that has prefix as **windows-bulkenroll**.

**Assign Device to User**

1. On the Devices page, click the user that has a prefix as **windows-bulkenroll**.
2. Click **Assign to User**. The Assign to User window opens.
3. Select or Search for the device from the list.
4. Select the required device.
5. Click **Assign to User**. The selected device will be assigned to the user.

When the user logs into the device for first time, the password change is must.

Assign to User option is available only for the Ivanti Bulk Enrolled devices.

Only device scope configurations and applications will work for the devices enrolled under this category. User scope configurations and applications are not supported.
