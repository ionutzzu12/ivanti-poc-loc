---
title: Connecting Microsoft Azure to Ivanti Neurons for MDM
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Procedure

1. Log in to Ivanti Neurons for MDM and go to **Admin** > **Microsoft Azure**.
2. In the left navigational pane, click **Microsoft Azure** > **Device Compliance**.
3. Under the Connect Account section, provide the following details:\* Azure Tenant ID - Find in your Microsoft Azure instance.
   - Enrollment URL (Optional) - If the device is not MDM enrolled, device users will be pointed to this URL for enrollment. When configuring, use HTTPS format. If you host a page in your organization to redirect your device users for Enrollment information, add that link here.
   - Remediation URL (Optional) - If the device is not in compliance, device users will be pointed to this URL for remediation. When configuring, use HTTPS format. If you host a page in your organization to redirect your device users for Remediation information, add that link here.
4. Click Connect Account. The Azure Tenant Validation dialog box opens.

Tenants currently connected to Azure and wishing to add device compliance for macOS devices need to disconnect the account and then re-establish the connection.

1. In the Azure Tenant Validation dialog, click the link present in Step 1.
2. Log in.
3. Review the permissions and then click Accept.

If you log in and the page prompts you to log in again, close the browser tab/ window.

1. Return to Ivanti Neurons for MDM. In the Connect Azure Account dialog box, select the I have provided the consent check box. Click Confirm.

- To edit the account, click Edit Account.
- To disconnect the account, click Disconnect Account. For additional instructions, see [**De-provisioning of the Azure tenant**](./De-provisioning_of_the_Azure_tenant.md).
- All activity of adding, editing, and deactivating an account are recorded in the Logs.
