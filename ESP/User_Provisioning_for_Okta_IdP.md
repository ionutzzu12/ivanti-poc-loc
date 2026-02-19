---
title: User Provisioning for Okta IdP
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Establish a connection with Ivanti Neurons for MDM**](./User_Provisioning_for_Okta_IdP.md)
- [**Provision users and groups**](./User_Provisioning_for_Okta_IdP.md)
- [**Verify assigned user provisioning**](./User_Provisioning_for_Okta_IdP.md)
- [**Verify group provisioning**](./User_Provisioning_for_Okta_IdP.md)
- [**Edit Settings**](./User_Provisioning_for_Okta_IdP.md)
- [**Configure Custom/ Enterprise Attributes in SCIM User Provisioning**](./User_Provisioning_for_Okta_IdP.md)

## Establish a connection with Ivanti Neurons for MDM

After you create the users and groups on your **Okta** application, you can establish the connection between **Okta** and Ivanti Neurons for MDM.

**Procedure**

1. Log in to **Okta**.
2. Go to **Applications** > **Applications** > **Browse App Catalog**.
3. Search for **Add SCIM 2.0 Test App** (OAuth Bearer Token) and install the app.
4. Click on the app and go to **Provisioning** > **Integration**.
5. Click **Edit** and provide the base url and paste the generated token.
6. Click **Save**.
7. Go to **Provisioning** and click **Edit**.
8. Enable the necessary user actions and click **Save**.

## Provision users and groups

After the connection is established between **Okta** and Ivanti Neurons for MDM, you can provision users or groups.

**Procedure**

1. Go to **Assignments** > **Assign** > **Assign to People** or **Assign to Group**.
2. 2\. Select or search for an existing user or group and click **Assign**.
3. Repeat the process to add more **Users** or **Groups**.
4. Click **Done**.
5. Select the group and click **push Group by name** to save and sync the group.

## Verify assigned user provisioning

After an assigned user is provisioned on the Okta portal, verify the user provisioning on Ivanti Neurons for MDM administrative portal.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Go to **Users**tab under the main menu. The provisioned user will be present in the list of users on this page.

## Verify group provisioning

After a group is provisioned on the Okta portal, verify the provisioning on Ivanti Neurons for MDM.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Go to **Users** tab and click **User groups**. The provisioned group will be present in the list of the groups in this page.

## Edit Settings

This topic helps you configure the Okta settings.

**Procedure**

1. Go to **Admin&#x20;**>**&#xA0;Identity&#x20;**>**&#x20;User Provisioning Okta**.
2. Click **Edit Settings**.
3. Set **Automatically invite users imported from Okta** - Manage whether users imported from Okta to Ivanti Neurons for MDM are automatically invited to register via email.
4. (Optional) Click **Add Custom Attribute** - Specify custom user attributes from your directory service that you want to apply to device management. Each attribute can then be referenced by $\{attributeName} in the Configuration fields that support variables. Use of this option requires consistent implementation of custom attributes across Okta servers. If the Okta server that is included in your implementation does not use the custom attribute, the features that are dependent on the custom attribute might not work as expected. The **Attribute Type** column displays **IDP** attribute in the **Custom Attributes** table in the **Edit Settings** section.
5. Click **Save**&#xNAN;**&#x20;Changes** after modifying the Okta settings.

## Configure Custom/ Enterprise Attributes in SCIM User Provisioning

**Procedure**

1. Go to **Admin&#x20;**>**&#xA0;Identity&#x20;**>**&#x20;User Provisioning**.
2. Click **Edit Settings**.
3. Enter Custom Attribute (for example, custAttr1) and click **Save Changes**.
4. From the Okta Portal, click **Directory** > **Profile Editor**.
5. Click on **SCIM 2.0 Test App**&#xNAN;**(OAuth Bearer Token) User** app.
6. Click **Add Attribute**.
7. Add the following custom attribute values, for example: \* Display name (same custom attribute value that we provided in N-MDM, refer to step 3).
   - Variable Name : custAttr1
   - External Name: custAttr1
   - External namespace : **urn\:ietf\:params\:scim\:schemas\:extension\:ivanti**:&#x32;**.0\:User**
   - User Permission : (Read / Write)
8. Click **Save Attribute**.
9. Click **Profile Editor** > **Mappings**. You will see two sections for mappings (SCIM and Okta).
10. Map the custom attributes created in N-MDM to attributes defined in Okta, and save the mappings.
11. Go to **Users** and click on the required user.
12. Click **Profile** > **Edit** to edit the attributes.
13. Go to **Applications** > **SCIM 2.0 Test App (OAuth Bearer Token)** app.
14. Under the **Assignments** tab, click **Assign** and select **Assign to People**.The **Assign SCIM 2.0 Test App (OAuth Bearer Token) to People** window appears on the screen.
15. Select the required user and click **Assign**.
16. Click **Done**.

To verify the custom attribute and its mapping in Ivanti Neurons for MDM:

- Go to **Users** > **User** (any specific user) > **Attributes**. Make sure the mapped custom attribute for Okta is visible under the User attributes section.
