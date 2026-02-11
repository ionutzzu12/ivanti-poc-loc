---
title: Self-Service Portal
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

The invitation to register includes a link to the Self-Service Portal. End users can use this portal to do the following tasks:

- Lock
- Unlock
- View Location (if enabled in the [**Privacy configuration**](./Privacy_Configuration.md))
- Wipe
- Retire
- Change account info (name, password, email address)
- Force Check-in
- Add encryption and signing certificates

To register additional devices, end users click the registration portal link displayed in the Self-Service Portal.

If end users misplace the URL for the Self-Service Portal, send them to [**https://mydevices.mobileiron.com/user/login.html**](https://mydevices.mobileiron.com/user/login.html). For iOS users, consider creating a [**Web Clip configuration**](./Create_a_Web_Clip_Configuration.md) for the Self-Service Portal.

## Uploading signing and encryption certificates

You can allow your end users to upload their email signing and encryption certificates in the Self-Service Portal within the User Provided Certificates configuration. This setting can be configured using the User Provided Certificates configuration. When configured, the end users can upload their email signing and encryption certificates.

1. In the **My Certificates** tab, click **Add Certificate**. The **Add certificate** window is displayed.
2. Update the following fields:|                       |                                                                                                                                                                                                                                                                                                                          |
   \| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   \| Field name            | Description                                                                                                                                                                                                                                                                                                              |
   \| Certificate Type      | Select the type of certificate to be uploaded. The options are:\* **Encryption certificate**
   - **Signing Certificate**These options are created from the Ivanti Neurons for MDM Admin Portal. See [**Identity Certificate Configuration**](./Identity_Certificate.md) for more information. |
     \| Certificate to Upload | Click **Choose File** to select the certificate file to be uploaded.Ensure that the file is in PKCS12 format.                                                                                                                                                                                                            |
     \| Password              | Type the password used for the file.                                                                                                                                                                                                                                                                                     |
3. Click **Upload**.

After uploading, you can view the list of certificates in a table displaying the following details.

| Field name       | Description                                                                               |
| ---------------- | ----------------------------------------------------------------------------------------- |
| Certificate Name | Specifies the type of certificates either **Encryption** or **Signing**.                  |
| Issued By        | the details of the certificate issued.                                                    |
| Uploaded On      | The date when the certificate was uploaded.                                               |
| Expiration Date  | The expiry date of the certificate.                                                       |
| Actions          | You can perform the following actions:\* **Edit Certificate** - edit certificate details. |

- **Clear Private Key** - deletes the private key from the certificate package(PKCS#12).
- **Delete Certificate** - deletes the certificate from the Ivanti Neurons for MDM server. |

When the user uploads a certificate configuration, the server re-pushes the configuration that is using the certificate.

Delete and Clear private key by a user will not re-push the configurations.
