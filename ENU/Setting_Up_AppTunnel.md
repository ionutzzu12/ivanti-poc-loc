---
title: Setting Up AppTunnel
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

AppTunnel protects app data by providing app-by-app session security between each app container and the corporate network.

This section contains the following topics:

- [**Setting up Sentry to use AppTunnel with certificates**](./Setting_Up_AppTunnel.md)
- [**Uploading Sentry certificates**](./Setting_Up_AppTunnel.md)
- [**Setting up apps to use AppTunnel**](./Setting_Up_AppTunnel.md)
- [**About the AppTunnel service name**](./Setting_Up_AppTunnel.md)

## Setting up Sentry to use AppTunnel with certificates

When you first install Standalone Sentry, a self-signed certificate is also installed. Ivanti strongly recommends that you replace the default certificate with a publicly trusted third-party certificate.

**Prerequisites**

- AppTunnel depends on the latest supported version of Sentry. Complete the Sentry installation before starting the AppTunnel setup tasks.
- If you intend to use a SCEP identity:\* Add a local or [**external certificate authority**](./Certificate_Management.md). A Connector installation is required.
  - Add an App Identity Certificate Configuration. This is the dynamic distribution you will use when you configure AppTunnel.

You can configure ActiveSync and/or AppTunnel using X.509 certificates for authentication to use Sentry servers that are assigned to a profile.

**Procedure**

1. Go to **Admin > Sentry**.
2. Click **+ Add Sentry Profile**.
3. Click **ActiveSync and/or AppTunnel with certificates**.
4. Click **Next**.
5. Use the guidelines in the following table to complete the **Global Settings** page.| Table: Global Settings for Admin > Sentry             |                                                                                                                                                                                                                                                                                                                                                                                                      |
   \| ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| Setting                                               | **What To Do**                                                                                                                                                                                                                                                                                                                                                                                       |
   \| **Name**                                              | Enter a name that identifies this profile.                                                                                                                                                                                                                                                                                                                                                           |
   \| **Description**                                       | Enter a description that clarifies the purpose of this profile.                                                                                                                                                                                                                                                                                                                                      |
   \| **External Hostname and Port**                        | Enter the hostname and port for the Sentry.                                                                                                                                                                                                                                                                                                                                                          |
   \| **Device Authentication Mode**                        |                                                                                                                                                                                                                                                                                                                                                                                                      |
   \| **Use a single certificate for 2-factor auth**        | Select to use a single certificate for authentication. If you do not already have a [**certificate uploaded**](./Certificate_configuration.md), you can do so in the area displayed below the selected option.                                                                                                                                                                                          |
   \| **Select certificate**                                | To upload a group certificate required for device authentication:1) Click **Add**. The **Add Certificate** window is displayed.
   2\) Type the name of the certificate in the **Certificate Name** field.
   3\) Type the password protecting the PKCS12 file.
   4\) Click **Choose File** to upload the group certificate. Ensure that the file format is in .p7b, .p12, .pfx, .pem, .der, .crt or .cer file. |
   \| **Enable certificate revocation list (CRL)**          | Select to validate the certificates presented by the device against the Certificate Revocation List (CRL) published by the CA.                                                                                                                                                                                                                                                                       |
   \| **Default Unmanaged Devices Behavior**                |                                                                                                                                                                                                                                                                                                                                                                                                      |
   \| **Allow unmanaged devices to receive email and data** | Select if you do not want to block data access for devices that are not managed by Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                      |
6. Click **Next**.
7. In the **Sentry Server Configuration** page, configure the following fields:

| Table: Sentry Server Configuration for Admin > Sentry |                                                                |
| ----------------------------------------------------- | -------------------------------------------------------------- |
| Setting                                               | What To Do                                                     |
| **Listener protocol**                                 | Select any of the following protocol options:\* **HTTPS Only** |

:::Paragraph{listStyleType="disc" indent="2"}
**HTTP Only**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**HTTPS and HTTP**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
\| **Https Port**                                        | Enter the Https port number. This field will not be displayed if the Listener protocol is selected as HTTP Only.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
\| **Http Port**                                         | Enter the Http port number. This field will not be displayed if the Listener protocol is selected as HTTPS Only.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
\| **Sentry TLS Server Certificate/key**                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
\| **Use Sentry's self-signed cert**                     | Select to use a self-signed certificate created by the Ivanti Neurons for MDM service and sent to Sentry as a part of this profile. This certificate is used for communication between the Sentry and mobile devices.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
\| **Add**                                               | To upload your own certificate required for authentication:1) Click **Add**. The **Add Certificate** window is displayed.You will be able to see this option only when you unselect the **Use Sentry's self-signed cert** option.
:::

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
Type the name of the certificate in the **Certificate Name** field.
:::

:::Paragraph{listStyleType="decimal" listStart="3" indent="2"}
Type the password protecting the PKCS12 file.
:::

:::Paragraph{listStyleType="decimal" listStart="4" indent="2"}
Click **Choose File** to upload the certificate. Ensure that the file format is in .p12 file.
:::

:::Paragraph{listStyleType="decimal" listStart="5" indent="2"}
Click **Add**.All the uploaded TLS Server certificates (including those certificates uploaded from the Sentry main page and from other profiles) are displayed in the Sentry TLS Server Certificate/Key section. To select the TLS certificate required for authentication, click the radio button next to the certificate. |
\| **Add second certificate**                            | Select to enable the second certificate. Once the primary certificate expires, Sentry automatically switches to the reserve certificate without admin intervention.Tunnel already stores both certificates and can match either, ensuring uninterrupted connectivity.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
\| **Protocols**                                         | Select the required incoming and outgoing protocols.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
\| **Cipher suites**                                     | Ciphers are used in the SSL-encrypted communication with the Sentry. Strong ciphers are generally preferred. Weak ciphers might be required for older devices. Strong ciphers are selected by default. Select any additional ciphers you want to use. At least one cipher must be selected.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
Click **Next**.
:::

9. Add at least one of the displayed services.
10. Click **Save**.

Once a Sentry is registered, it is displayed in the Sentry page under the Unconfigured Sentry Servers section. To assign a profile for the Sentry, click **Assign** in the **Actions** column.

## Uploading Sentry certificates

Ivanti Neurons for MDM uploads TLS Server certificates and Group certificates when creating a Sentry profile. You can also upload these certificates from the **Sentry** page under the **Sentry Certificates** section.

Ivanti Neurons validates Sentry certificates upon upload, returning the following types of information depending on the conditions found in the certificates:

| Condition                                                                                                                             | Information type |
| ------------------------------------------------------------------------------------------------------------------------------------- | ---------------- |
| The leaf certificate does not contain a chain to any certificate authority or there is no certificate authority in the uploaded file. | Error            |
| There is no root certificate authority available.                                                                                     | Warning          |
| The root certificate authority has not signed off the intermediate certificate authority for the leaf certificate.                    | Warning          |

Ivanti Neurons for MDM also validates against the rules in [**this article**](https://support.apple.com/en-us/HT210176).

**Procedure**

1. In the **TLS Server Certificates** section, click **Add**. The **Add Certificate** window is displayed.
2. Type the name of the certificate in the **Certificate Name** field.
3. Type the password protecting the PKCS12 file.
4. Click **Choose File** to upload the group certificate. Ensure that the file format is .p7b, .p12, .pfx, .pem, .der, .crt or .cer.
5. Click **Add**. The uploaded certificate is displayed on the table.
6. To delete the TLS Server certificate, click on the Delete icon in the **Actions** column.

If the TLS Server certificate is used in any Sentry profile, you will not be able to delete the certificate. An error message will be displayed if the delete action is performed.

### Add Group certificates

**Procedure**

1. In the **Group Certificates** section, click **Add**. The **Add Certificate** window is displayed.
2. Type the name of the certificate in the **Certificate Name** field.
3. Type the password protecting the PKCS12 file.
4. Click **Choose File** to upload the group certificate. Ensure that the file format is .p7b, .p12, .pfx, .pem, .der, .crt or .cer.
5. Click **Add**.

To delete the uploaded Group certificate, click on the Delete icon in the **Actions** column.

### Edit the Sentry Root Certificate

As the administrator you have the option to edit the distribution of the Sentry Root Certificate configuration. You can also provide edit permission to the custom space administrator by delegating config to other spaces.

1. Go to **Configurations**.
2. Search for the **Sentry Root Certificate**.
3. Click the edit icon.
4. Select the checkboxes corresponding to the Devices or Device Groups to distribute the certificate. Alternatively, clear the checkboxes corresponding to the Devices or Device Groups.
5. Select one of the following options from the Distribution Summary section as applicable:\* **Do not apply to other spaces**
   - **Apply to devices in other spaces**
6. (Optional) Click the checkbox **Allow Space Admin to Edit the Distribution**.
7. Click **Save**.
8. A warning message appears. Click **Yes** to confirm.

## Setting up apps to use AppTunnel

For the latest Sentry instructions, visit [**Product Documentation**](https://help.ivanti.com#116) and click Sentry. Select the document appropriate to your version of Sentry.

## About the AppTunnel service name

An AppTunnel service defines the backend service that an AppConnect app tunnels to.

For the latest instructions, visit [**Product Documentation**](https://help.ivanti.com) and select the documents appropriate to your versions of [**Sentry**](https://help.ivanti.com/#116) and [**AppConnect**](https://help.ivanti.com/#103).
