---
title: User Provisioning for Entra ID IdP
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Establish a connection with Ivanti Neurons for MDM**](./User_Provisioning_for_Entra_ID_IdP.md)
- [**Provision assigned users and groups**](./User_Provisioning_for_Entra_ID_IdP.md)
- [**Provision all users and groups**](./User_Provisioning_for_Entra_ID_IdP.md)
- [**Verify assigned user provisioning**](./User_Provisioning_for_Entra_ID_IdP.md)
- [**User Provisioning for Entra ID IdP**](./User_Provisioning_for_Entra_ID_IdP.md)
- [**Edit Settings**](./User_Provisioning_for_Entra_ID_IdP.md)
- [**Configure Custom and Enterprise Attributes**](./User_Provisioning_for_Entra_ID_IdP.md)
- [**Migration considerations - Entra ID User Source to User Provisioning SCIM**](./User_Provisioning_for_Entra_ID_IdP.md)
- [**Migration considerations - LDAP to User Provisioning SCIM**](./User_Provisioning_for_Entra_ID_IdP.md)
- [**Important Notes - SCIM&#xA0;**](./User_Provisioning_for_Entra_ID_IdP.md)

## Establish a connection with Ivanti Neurons for MDM

After you create the users and groups on your Entra ID Enterprise application, you can establish the connection between Entra ID and Ivanti Neurons for MDM.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Log in to the Entra ID portal.
:::

:::WorkflowBlockItem
Go to **Enterprise Application** > Click **+ Create your own application**. The Create your own application window opens.
:::

:::WorkflowBlockItem
Specify the name of your app (**Default: Non-gallery**) and click **Create**. For example, Ivanti Neurons for MDM User Provisioning.
:::

:::WorkflowBlockItem
Go to **Provisioning** > **Edit provisioning** > **Admin Credentials**.
:::

:::WorkflowBlockItem
Copy and paste the Target SCIM URL from the Ivanti Neurons for MDM admin portal in the **Tenant URL** field in the Entra ID portal.
:::

:::WorkflowBlockItem
Copy and paste the Token from the Ivanti Neurons for MDM in the **Secret Token** field in the Entra ID portal.
:::

:::WorkflowBlockItem
Perform one of the following steps:
:::

:::WorkflowBlockItem
- Select **Sync only assigned users and groups**. For more information, see Provision assigned users and groups
- Select **Sync all users and groups**. For more information, see Provision all users and groups.Select the Sync All Users and Groups option for migrating users.
  Click **Test Connection**. A pop-up with a green check confirms the connection.
:::

:::WorkflowBlockItem
Click **Save**.
:::

:::WorkflowBlockItem
Expand **Mappings** from the **Provisioning** page on the Entra ID portal.
:::

:::WorkflowBlockItem
Click **Provision Entra ID Users**. The Attribute Mapping page opens.
:::

:::WorkflowBlockItem
Click **Delete** to delete the unsupported attributes.
:::
::::

## Provision assigned users and groups

After the connection is established between Entra ID and Ivanti Neurons for MDM, you can provision users or groups.

When provisioning groups, Entra ID does not add members of the nested groups to the selected group. Entra ID adds immediate members and group names to the group only and not the subgroup members during the sync process.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. In the application go to **Users and groups** > click **+ Add User/Group**. The Add Assignment page opens.
3. Search for the user or group from the **Search** field, click **Select**, and then **Assign**. The Users and Groups page opens.
4. Select the corresponding user or group checkbox.
5. Click **Provisioning** and then click **Start Provisioning**. The details of the successful configuration are displayed.

## Provision all users and groups

After the connection is established between the Entra ID and Ivanti Neurons for MDM, you can provision users or groups.

**Procedure**

- Click **Provisioning** and then click **Start Provisioning**. The page opens with the details of the successful provision and the user will be provisioned to Ivanti Neurons for MDM.

## Verify assigned user provisioning

After an assigned user is provisioned on the Entra ID portal, verify the provisioning on the Ivanti Neurons for MDM administrative portal.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Go to the **Users** tab under the main menu. The user that was provisioned will be present in the list of the users in this page.The provisioning process may take up to an hour.

## Verify group provisioning

After a group is provisioned on the Entra ID portal, verify the provisioning on Ivanti Neurons for MDM.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Go to the **Users** tab > **User groups**. The group that was provisioned will be present in the list of the groups in this page.The provisioning process may take up to an hour.

## Edit Settings

This topic helps you configure the Entra ID settings.

**Procedure**

1. Go to **Admin > Microsoft Azure > User Provisioning Entra ID**.
2. Click **Generate Token** and copy the token.
3. Refresh the page. The Entra ID Settings page opens.
4. Click **Edit Settings**.
5. Set **Automatically invite users imported from Entra ID** - Manage whether users imported from Entra ID to Ivanti Neurons for MDM are automatically invited to register via email.
6. Set **Managed Apple ID** - This option is disabled by default. Click the toggle button to turn it ON and sync Managed Apple ID for the Entra ID users.\* **User email address**
   - (Optional) select the Include "appleid" subdomain option to avoid conflict with existing Apple IDs.
7. (Optional) Click **Add Custom Attribute** - Specify custom user attributes from your directory service that you want to apply to device management. Each attribute can then be referenced by $\{attributeName} in configuration fields that support variables. Use of this option requires consistent implementation of custom attributes across Entra ID servers. If an Entra ID server included in your implementation does not use this attribute, then features dependent on this attribute might not work as expected. The **Attribute Type** column displays **IDP** attribute in the **Custom Attributes** table in the **Edit Settings** section.
8. Click **Save\*\*\*\*Changes** after modifying the Entra ID settings.

## Configure Custom and Enterprise Attributes

**Procedure**

1. Go to **Admin&#x20;**>**&#xA0;Identity&#x20;**>**&#x20;User Provisioning**.
2. Under **Edit Settings**, click **+Add Custom Attribute**.
3. Enter a name in the **Attribute Name** field (for example, custAttr1) and click **Save Changes**. The attribute is listed and available on **Admin** > **System** > **Attribute** page. The attribute is denoted as IdP attribute and you can only perform Delete action.
4. Log in to the **Entra ID** portal.
5. Go to **Home** > **Enterprise Application** > Click on the SCIM application.
6. Click **Provision Entra ID Users** from the **Mappings** section.
7. Select the **Show advanced options** check box.
8. Click **Edit attribute list for customappsso**.
9. Enter a new entry for the custom attribute that you created in the Ivanti Neurons for MDM UI.
10. Add the schema for the Custom/ Enterprise (Department) attribute as follows\:Custom attribute - **urn\:ietf\:params\:scim\:schemas\:extension\:ivanti**:&#x32;**.0\:User:\<custAttr1> -&#x20;**&#x52;efer to step 3.Enterprise attribute - **urn\:ietf\:params\:scim\:schemas\:extension\:enterprise**:&#x32;**.0\:User\:department**
11. Click **Save changes**.
12. Click **Add New Mapping** and select the Source and Target attributes from the drop-down menu.
13. Click **Ok** and **Save Mapping**.
14. Go to **Home** > **Enterprise Application** > Click on the SCIM application > **Users and groups**.
15. Click User name. The Profile Page opens.
16. Verify whether the value associated with the attribute appears on the Profile page.
17. (Optional) Click on the SCIM application > Provisioning > Provision on demand, search for the specific user, and click Provisioning. To validate the new attribute mappings performed in the previous steps.
18. Log in to the Ivanti Neurons for MDM administrative portal.
19. Go to **User** > **Users**.
20. Select the user, click the **Attributes** tab, and verify the attribute value. The attribute is mapped for the specific user.

### Migration considerations - Entra ID User Source to User Provisioning SCIM

- When migrating from Entra ID User Source to User Provisioning Entra ID (SCIM), select Sync All Users and Groups.
- After users and groups are updated with a SCIM Entra ID source, return to the Azure Provisioning page in Azure and set the specific users and groups to be managed by User Provisioning Entra ID using the Sync only assigned users and groups option.
- When the sync is complete, you can remove the users and groups that are not defined in Azure from the Ivanti Neurons for MDM Users and Groups lists.
- When the migration starts, the Entra ID User Source page is accessible in a read-only state.

### Migration considerations - LDAP to User Provisioning SCIM

**Prerequisites**:

:::Paragraph{listStyleType="decimal" indent="2"}
**Enable this LDAP Server** option is selected by default. This option must be deselected before migration.
:::

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
Create an Enterprise App in Entra ID , Add the Synced LDAP Users/Group (Same LDAP Users/Groups present in Ivanti ) to SCIM App. Start Provisioning.
:::

**Key considerations for LDAP to SCIM Migration**

- LDAP does not capture all information for synchronized users/groups, while SCIM logs user/group events in Audit Logs.
- LDAP user with custom attribute has the Type defined ldap, where as for SCIM, it is IdP. So, when the users with custom attribute are migrated from LDAP to SCIM, the corresponding IdP custom attribute should be created in SCIM App and the users will be migrated . When the user wants to update the ldap custom attribute later, the ldap.custom attribute value will not be updated in MDM after migration. The IdP attribute value will be updated.
- Migrate LDAP users who are associated with one or multiple custom attributes, specifically "ldap.custAttr1," indicating the registration of the LDAP device and the configuration (Identity Certificate Configuration) pushed to the device with the SAN Type corresponding to the value of the LDAP custom attribute.
- Migrate a LDAP User where Managed Apple Id associated with email Address - So, before Migration from LDAP to SCIM, if the user wants to persist the value of LDAP user's managed Apple Id, the Managed Apple Id in SCIM setting must be enabled and the settings must be saved.
- When LDAP User is removed in LDAP server , the user is still active but No sync flag is set to true for that particular synced LDAP User. In case of SCIM, When one provisioned user is deleted , the user status is disabled.
- Once SAML is configured for the Identity Provider (IdP) for SCIM users, all users from various sources like Local and LDAP will be authenticated through SAML. Only local users can be added to an exception list to bypass the IdP authentication flow. This configuration can be managed in the SAML page under **Admin** > **Identity** > **SAML**.
- Once SAML is configured for the migrated IDP (SCIM) users, device registration can be bypassed (not via IDP) for other users from different sources such as Local and LDAP. This can be managed under **Users** > **User Settings**.
- In LDAP, Users, Groups, and OU are supported, whereas In SCIM, Users and Groups are supported, but not OU.
- Nested group provisioning process is not supported in SCIM.

### Important Notes - SCIM 

- Email address is a mandatory field for provisioning and migrating users or members.
- SCIM provides one way provisioning from Microsoft Entra ID to Ivanti Neurons for MDM. Ivanti Neurons for MDM does not offer any sync options. If you delete a SCIM provisioned group or user from Ivanti Neurons for MDM, ensure that you also remove the user or group from Microsoft Entra ID.
- You can use one attribute (source or target) only once in the SCIM application mapping window in Microsoft Entra ID. The same source cannot be mapped twice to a specific target attribute.
- Inactive users cannot be provisioned or migrated to Ivanti Neurons for MDM using SCIM.
- Currently, Ivanti Neurons for MDM does not support SCIM event notification.
- Migration or provisioning duration depends on the number of users or groups involved.
- Microsoft Azure controls the provisioning interval and it is about approximately 40 minutes or more.
- During re-provisioning, Microsoft Entra ID will only retry the entries that failed. You can download the provision logs to verify the users that have succeeded or failed provisioning from Microsoft Entra ID.
- Duplicate groups from different sources are not allowed in SCIM.
- When a provisioned user is hard deleted from Microsoft Entra ID, the user is disabled in Ivanti Neurons for MDM.
- When a provisioned user group is deleted from Microsoft Entra ID, the group is deleted in Ivanti Neurons for MDM and the independent members that belong to the deleted group are disabled and are associated to All Users Group.
- When a provisioned member of a provisioned group is hard deleted in Microsoft Entra ID, the member is disabled in Ivanti Neurons for MDM however, the member is still associated to the group in Ivanti Neurons for MDM.
- When an attribute (Enterprise attribute or custom attribute) mapping is removed from an app, the removed attribute value is still reflected in Ivanti Neurons for MDM.
- When a user attribute of a provisioned user is updated with blank or empty value, the updated attribute value is not reflected in Ivanti Neurons for MDM.
- If the user attributes FName and LName (name.formatted) are blank during migration or update from Microsoft Entra ID to SCIM, the migration or update fails.
- If you delete a user in Entra ID, the corresponding SCIM API does not delete the user permanently but performs a soft delete and changes the user status from active to inactive. If you want to permanently delete the user, log in to Ivanti Neurons for MDM administrative portal and manually delete the inactive/ disabled user.
- When a local user already exists in Ivanti Neurons for MDM with a certain user ID, a similar user with the same user ID will be provisioned from Entra ID to MDM, the user source will be updated from Local to SCIM Entra ID.
- Entra ID with "Entra ID Premium P1" subscription has the privilege to provision the required group to be assigned and provisioned.
