---
title: Certificate-based authentication
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDMsupports certificate-based authentication which allows administrators to log in using digital certificates and a tenant-specified (vanity) hostname. When enabled and configured, the administrators can log in using the digital certificates instead of the basic authentication (username and password).

This feature is disabled by default. Administrators should contact Support to enable this feature on their tenant(s). This feature is only available on NA3 cluster environments, and only if enabled by Support. Please ensure that you have your super admin user name and password tested and ready, because once certificate-based authentication is enabled, these credentials will be the only ones you can use to log in until you have successfully configured your vanity domain.

**Procedure**

1. In the **Admin** tab, select **Vanity Host Configuration**.
2. In the Vanity Host Configuration page, configure the following options:

| Setting                                | What To Do                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| -------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Create Vanity Domain                   | Type the name of the vanity domain. This is the domain name that may more closely align with your corporate identity and into which you can log in using digital certificates.                                                                                                                                                                                                                                                                                 |
| Upload Trusted issuing CA certificates | Click **Choose File** to select and upload the CA certificate that issues certificates to your administrators.To enable the certificate revocation check, select **Enable certificate status validation settings for this certificate** (optional).This option is enabled by default. Unselect this option to disable certificate revocation.Click **Add More** to add more certificates.Ensure that the certificate format is .p7b, .pem, .der, .crt or .cer. |
| Certificate Attribute mapping          | Certificate attribute mapping configures the mapping of the certificate identity elements to the account attributes of the admin.In the **From Certificate** field, select either of the following certificate elements:\* **NTPrincipalName**                                                                                                                                                                                                                 |

:::Paragraph{listStyleType="disc" indent="2"}
**RFC 822 Name**In the **To Variable** field, select any of the following account attributes of the admin:\* **UserUPN**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**$UserEmailAddress**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**$EDIPI**                                                   |
Click **Save**.It may take a few minutes for your vanity host to become accessible.
:::
