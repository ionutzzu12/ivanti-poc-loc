---
title: User Provisioning with SCIM
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**User Provisioning**](./User_Provisioning_with_SCIM.md)
- [**Generate a token from Ivanti Neurons for MDM**](./User_Provisioning_with_SCIM.md)
- [**Change the Token Status**](./User_Provisioning_with_SCIM.md)
- [**View the Token Status from Audit Trials**](./User_Provisioning_with_SCIM.md)
- [**Configure Attributes in SCIM Provisioning**](./User_Provisioning_with_SCIM.md)

## User Provisioning

User Provisioning uses the SCIM protocol to synchronize an IdP with Ivanti Neurons for MDM and allows for partial user and group sync. User Provisioning uses the SCIM protocol to automatically create and update user and group objects sourced from an IdP to Ivanti Neurons for MDM. Just like the current integration with Entra ID and Okta, the users and groups provisioning process is automated; if changes are made to the user or group in IdP, the same changes are reflected in Ivanti Neurons for MDM.

Since the username value is unique in Ivanti Neurons for MDM, the User Principal Name attribute cannot be updated in IdP if the user is already provisioned.

## Generate a token from Ivanti Neurons for MDM

To start User Provisioning for an IdP, generate a token and the target URL from Ivanti Neurons for MDM.

Ensure that you save the token and the target URL.

A maximum of 2 tokens can be generated any time.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Go to **Admin&#x20;**>**&#x20;Identity&#x20;**>**&#x20;User Provisioning**.
3. Select Identity Provider (IdP) from the dropdown list.
4. To generate a new token, click **Generate**. A notification message appears, click **Generate**. A new page opens with details of the Token and the Target SCIM URL.
5. Click **Copy** to copy either the token or the SCIM URL.
6. Refresh the page. The **User Provisioning**page displays the Token Status table.

## Change the Token Status

You can change the state of an existing token.

**Procedure**

1. Click the **Select** drop-down menu on the **User Provisioning Entra ID** page.
2. Click **Select** and make the following changes to the token:\* **Set to Active**
   - **Set to Inactive**
   - **Renew**
   - **Remove**

## View the Token Status from Audit Trials

You can view the logs of actions / events that took place on a SCIM token from the Audit Trials section. The SCIM token can have one of the following statuses:

- SCIM Token Created - A SCIM token has been created.
- SCIM Token Enabled - The SCIM token has been enabled.
- SCIM Token Disabled - The SCIM token has been disabled.
- SCIM Token Renewed - The SCIM token has been renewed.
- SCIM Token Deleted - The SCIM token has been deleted.

The DETAILS column also lists the SCIM vendor name (IDP) such as Azure, Okta, etc. which makes it easy to communicate with Ivanti Neurons for MDM.

## Configure Attributes in SCIM Provisioning

This section describes how to create custom and enterprise attributes for an IdP during user provisioning.

## Mapping attributes

After the connection is established, you can map the attributes between IdP and Ivanti Neurons for MDM. Ivanti Neurons for MDM supports the following user attributes:

### Core attributes

- id
- userName
- displayname
- active
- givenName
- familyName
- emails
  For Entra ID IdP, external IdP is supported.

### List of attributes for which update operation is allowed

- displayName
- emails
- givenName
- familyName
- active
- urn\:ietf\:params\:scim\:schemas\:extension\:ivanti:2.0\:User
- urn\:ietf\:params\:scim\:schemas\:extension\:enterprise:2.0\:User

### Custom attribute

**Schema** - urn\:ietf\:params\:scim\:schemas\:extension\:ivanti:2.0\:User:\<CustomAttribute123Name>

### Enterprise attribute

Currently only the Department attribute is supported.

**Schema** - urn\:ietf\:params\:scim\:schemas\:extension\:enterprise:2.0\:User\:department
