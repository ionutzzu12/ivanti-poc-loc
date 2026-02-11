---
title: Connect Ivanti Neurons for MDM with Entra ID User Source
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

To work with Entra ID (Entra ID), you must configure Ivanti Neurons for MDM with details about your Microsoft Entra ID account. You require an existing and configured Microsoft Entra ID account. This solution requires no on-premise connector or LDAP.

This section contains the following topics:

- [**Use cases**](./Connect_Ivanti_Neurons_for_MDM_with_Entra_ID_User_Source.md)
- [**Using Entra ID**](./Connect_Ivanti_Neurons_for_MDM_with_Entra_ID_User_Source.md)
- [**Entra ID Settings**](./Connect_Ivanti_Neurons_for_MDM_with_Entra_ID_User_Source.md)

## Use cases

You can connect Ivanti Neurons for MDM with Entra ID for one of the following use cases:

- Work with Microsoft Office 365
- Set up Microsoft Entra ID, Microsoft ADFS, or another SAML 2.0 Identity Provider (IdP) for user authentication
- Set up Microsoft Entra ID as your user source
- Sync users from Microsoft Entra ID and get started. All users and groups in your Entra ID domain will be synced to your Ivanti Neurons for MDM instanceA notification is displayed in the **Notifications** page if there is an error in Entra ID sync due to the following reasons:\* Entra ID service is unreachable
  - All user attributes are not synchronized with Entra ID
  - Some user attributes are not synchronized with Entra ID
- Environments with multiple IdPs are currently not supported.
- If you are not using Microsoft Entra ID as your user source, you can use Local Accounts or source users from LDAP. This requires setting up an Ivanti Neurons for MDM connector to access LDAP resources on-premise.
- Using Microsoft Entra ID only for user authentication and using an on-premise LDAP for user directory is currently not supported.

## Using Entra ID

To use Entra ID, set up your Identity Provider for user authentication in one of the following methods:

- To use Microsoft Entra ID for both user source and user authentication, setup Entra ID as your IdP. Go to **Admin > Identity > Ivanti Neurons for MDM IdP Setup** and select **Entra ID** from the menu.
- To use Microsoft Entra ID for user source and to use ADFS for user authentication, setup ADFS as your IdP. Go to  **Admin > Identity >****On-Prem IdP Setup** and select ADFS from the menu.
- To use a SAML 2.0 IdP other than Entra ID and to use ADFS for user authentication, go to  **Admin > Identity >****Generic IdP Setup** and follow the instructions on the page.

For more information, see [**Configure Identity Provider**](./Configure_Identity_Provider.md).

## Entra ID Settings

This topic helps you configure the Entra ID settings.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Admin > Microsoft Azure > Entra ID User Source**.
:::

:::WorkflowBlockItem
Specify the following details:
:::

:::WorkflowBlockItem
1. **Entra ID Name**.
2. **Sync Interval** - Modify the frequency that Ivanti Neurons for MDM synchronizes user data from your Entra ID.
3. **Enable this Entra ID** - Use this option to enable or disable Entra ID instance.
4. Select **Automatically invite users imported from Entra ID** - Manage whether users imported from Entra ID to Ivanti Neurons for MDM are automatically invited to register via email.
5. Select **Managed Apple ID** - Choose to sync Managed Apple ID for the Entra ID users.\* **None**
   - **Pattern** -\* **User email address**
     - **userUPN**
     - (Optional) select the Include "appleid" subdomain option to avoid conflict with existing Apple IDs.
6. (Optional) Click **Add Custom Attribute** - Specify custom user attributes from your directory service that you want to apply to device management. Each attribute can then be referenced by $\{attributeName} in configuration fields that support variables. Use of this option requires consistent implementation of custom attributes across Entra ID servers. If an Entra ID server included in your implementation does not use this attribute, then features dependent on this attribute might not work as expected.
   Click **Save** after modifying the Entra ID settings.
:::
::::
