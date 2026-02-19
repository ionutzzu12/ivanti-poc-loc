---
title: Configure Identity Provider
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

License::Variable\{key="PrimaryMI.license2" type="variable"}

Configure an identity provider (IdP) to authenticate users who wish to register devices with Ivanti Neurons for MDM, access this Admin Portal, or access the Self-Service Portal. An on-prem LDAP compatible user directory is required. Ivanti Neurons for MDM works with any SAML 2.0 compatible IdP. Microsoft Entra ID Authentication (Entra ID), Microsoft ADFS (Active Directory Federation Services), Okta, OneLogin, PingOne, and Ping Identity's PingFederate have been verified to work with Ivanti Neurons for MDM.

Previously, if you setup SAML auth/IdP, SAML authentication is used for both device registration and portal authentication. Now, a toggle button is provisioned to choose different authentication methods for Admin Portal access and Device Registration. The bypass toggle is applicable only for device registration.

During device registration, the administrator can bypass the identity provider option and provide the user with the option to authenticate using a PIN instead of authentication using the identity provider page.

## Overview

- If you are using Microsoft AD, or another on-premise LDAP directory, you will need to set up Connector to connect to and import users to Ivanti Neurons for MDM. Set up Connector or [**LDAP**](./Configuring_LDAP_server.md) if you have not done so already.
- When an IdP is added, user authentication automatically switches from LDAP to IdP.
- Only one IdP provider is allowed.
- In case your IdP becomes inaccessible, use the Ivanti Neurons for MDM Tenant Admin (TA) account to access this Admin Portal and troubleshoot. The TA is a Local account and does not require external authentication. The TA account is created when your Ivanti Neurons for MDM is provisioned and information provided to the technical contact of your organization, or equivalent. If you do not have your TA account information, contact your support representative.
- Ivanti Neurons for MDM supports Microsoft Entra ID (Entra ID) for authenticating users during registration of Windows 10 devices.Set the authentication type for your LDAP users using the tools provided by your IdP vendor. The authentication scheme of your IdP will take precedence over the Ivanti Neurons for MDM settings.Ivanti Neurons for MDM Authentication settings can be found here: **Users > User Settings > Device Registration Setting > Device Registration Authentication Type**.
- Apple Device Enrollment and Configurator device enrollments do not use IdP for user Authentication.
- To configure an identity provider to work for registering Apple Business Manager iOS and macOS devices, you must enable the **Enable Custom Enrollment** and the related **Ivanti Hosted webpage** settings found at **Admin > Apple > Device Enrollment >&#x20;***edit a device enrollment profile*. See [**Device Enrollment**](./Device_Enrollment.md) for more information:

::Image[]{src="Resources/Images/idp001.png" signedSrc="Resources/Images/idp001.png" size="32" caption alt isUploading="false" sha initialPath="Resources/Images/idp001.png" githubPath="Resources/Images/idp001.png" position="flex-start" indent="2"}

## IdP Set Up Types

The Ivanti Neurons for MDM Identity page guides you through the set up of the following types of IdP providers:

- **Ivanti Neurons for MDM IdP Setup**- Supported Ivanti Neurons for MDM IdP providers are Entra ID, OneLogin, Okta, and PingOne.
- **On-Prem IdP Setup**- Supported on-prem IdP providers are ADFS 3.0, PingFederate 8.2.1, and PingFederate 8.1.3.
- **Generic IdP Setup**- This is a generic set up path you can use if you are not using Microsoft ADFS, Okta, OneLogin, or PingFederate.

## Configuring an identity provider (IdP)

**Procedure**

1. Go to **Admin&#x20;**> **Identity** > **SAML Authentication**.
2. Click an identity provider set up type:\* **Ivanti Neurons for MDM IDP Setup**
   - **On-Prem IDP Setup**
   - **Generic IDP Setup**
3. Select a corresponding IdP. If you selected **Generic IDP Setup** in step 3, then skip this step and continue from step 5.
4. Follow the instructions on the screen that appear for your chosen IdP.
5. Click **Done**.

Administrators are allowed to single sign-on for up to 2 hours from their initial authentication with the IdP.

### Setting up tasks you may need to complete

Depending on your chosen IdP, you will be guided through the following associated pages and steps:

| **IdP**    | **Procedure** |
| ---------- | ------------- |
| - Entra ID |               |

- Okta
- OneLogin
- PingOne               | \* Generating a key to upload to your IdP.
- Logging into your IdP and uploading generated key.
- Exporting a metadata file from your IdP and importing it into Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| - ADSF 3.0
- PingFederate 8.2.1
- PingFederate 8.1.3 | \* Download the metadata file from Ivanti Neurons for MDM.
- Setting up a "Relying Party Trust" on ADFS or an “SP Connection” on PingFederate, and importing the Ivanti Neurons for MDM metadata file.
- Exporting the metadata file from your IdP and importing it into Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| - Generic IdP                                        | ::::WorkflowBlock

:::WorkflowBlockItem
Download the metadata file from Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Follow the instructions provided by your IdP vendor to configure your IdP server or service to communicate with Ivanti Neurons for MDM service as "Service Provider." This can include:
:::

:::WorkflowBlockItem
1. Uploading the metadata file from Step 1 above to your IdP. This configuration file contains the essential information that enables Ivanti Neurons for MDM, as a SAML 2.0 Service Provider, to communicate with your SAML 2.0 Identity Provider. The standard SAML 2.0 URLs, certificates and settings are included in the metadata file.Ivanti Neurons for MDM expects a SAML 2.0 compatible IdP to have the ability to import and process an XML metadata exported from a Service Provider.
2. Configuring your IdP to use RSA-SHA1 for signing SAML authentication requests. Information about the Signing Certificate used to verify the authentication requests is included in the metadata file downloaded in Step 1.
3. Configuring your IdP to include a username in the SAML responses sent to Ivanti Neurons for MDM. Specify the username in the \[Name Id] element of the SAML Response from IdP.
   Export a metadata file from your IdP and importing it into Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
(Optional) - Include username in SAML Authentication Request: To include the username of authenticating user in the authentication request and to remove an additional user input when authenticating with an IdP. If you enable this option, authentication failures may happen. If you are sure about IdP validation, select the **I understand the impact of this change** option and toggle the **Include Username in SAML Authentication Request** setting to **ON**.Ivanti Access is a validated IdP for this setting.
:::

\:::: |

## Enabling local users to bypass IdP authentication

When an IdP or Ivanti Neurons for MDM connectivity goes down and needs troubleshooting from the Ivanti Neurons for MDM side, certain administrators need the ability to login to Ivanti Neurons for MDM without reliance on external systems, such as, LDAP or IdP, for authentication. Only local users with system admin roles can bypass IdP authentication.

Create a list of local users to bypass IdP authentication.

**Procedure**

1. Click **Admin > Identity**.
2. Under the Local Users to Bypass IdP Authentication section, click **+Add Users**.
3. From the list displaying only the local users with system admin roles, select a few users.
4. Click **Save**.

To remove a user from the list of local users that bypass IdP authentication, click the remove icon next to the entry you want to delete.

If you cannot see the Identity page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- System Management
- System Read Only
