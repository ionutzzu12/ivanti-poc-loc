---
title: Adding an API user for Cisco ISE operations
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

You can add an API user with the role "Cisco ISE Operations” that allows Cisco ISE to interact with the Cisco ISE APIs in Ivanti Neurons for MDM. After you create this user, you use this user's credentials from Cisco ISE to authenticate API calls into Ivanti Neurons for MDM. These APIs allow Cisco ISE to get device information; take actions on devices, for example, full wipe, corporate wipe, and pin lock; and send messages to devices.

The API user will not be able to log into the Admin portal. This user is for enabling API usage only.

Only the Super Admin of a tenant is assigned the Cisco ISE Operations role by default. The Super Admin must explicitly choose the other users in the system who must possess this role and assign it to them. Users, that are assigned the Cisco ISE Operations role can, in turn, assign the role to other appropriate users in the system.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Click the **Users** tab.
:::

:::WorkflowBlockItem
:inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/IA-eEKVjp8KA3yspAtolZ_r36addapiuser001.png" alt caption}
Click **Add**.
:::

:::WorkflowBlockItem
Select **API User**.
:::

:::WorkflowBlockItem
Complete the resultant form with the user's information:
:::

:::WorkflowBlockItem
- Email Address
- First Name
- Last Name
  The Username field displays the email address you entered. In most cases, you should not edit this default. See [**When to Edit a Username**](./Editing_a_Username.md).

If you want to change the display name for this user, edit the default text in the **Display Name** field.
:::

:::WorkflowBlockItem
Assign a password by entering it in the **Password** and **Confirm Password** fields.
:::

:::WorkflowBlockItem
Leave the **API Management Cisco ISE Operations** role selected in the **Assign Roles** section.
:::

:::WorkflowBlockItem
Click **Done** to add the user.
:::
::::

If you cannot perform tasks on the **Users** page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- System Management
- User Management
