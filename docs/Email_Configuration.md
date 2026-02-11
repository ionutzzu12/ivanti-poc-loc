---
title: Email Configuration
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

An email configuration sets up POP or IMAP email on devices.

## Email settings

| **Setting**         | **What To Do**                                                                                                                                                                                                                                                                                                                                                                                           |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                | Enter a name that identifies this configuration.                                                                                                                                                                                                                                                                                                                                                         |
| Description         | Enter a description that clarifies the purpose of this configuration.                                                                                                                                                                                                                                                                                                                                    |
| Account Description | Enter the text you want to use to identify this email account.                                                                                                                                                                                                                                                                                                                                           |
| Account Type        | Select IMAP or POP. If you select IMAP, you can also enter the path prefix. The internet service provider (ISP) can give you information on which type of account is available. A prefix is generally required when all IMAP folders are listed under the Inbox. ISPs that require prefixes usually provide information on the specific prefix to configure.                                             |
| User Display Name   | Enter the text you want to use to identify email account user. Note that the user can set this value on the device, as well.                                                                                                                                                                                                                                                                             |
| Email Address       | Enter a variable to specify the email address for the account.                                                                                                                                                                                                                                                                                                                                           |
| Allow Move          | Select if you do not want to prevent email from being moved from this account.                                                                                                                                                                                                                                                                                                                           |
| Enable S/MIME       | Select to turn on support S/MIME encryption. Then, you can select signing and encryption certificates.Requires certificate caching. Make sure that caching is enabled in the Certificate Authority being used by Identity Certificate's configuration.\*\*iOS 10.3+:\**Select one of the following options for the&#x20;****S/MIME signing****&#x20;and&#x20;****S/MIME encryption****&#x20;fields:* Off |

- On
- User SelectiOS 12.0+:\* Enable user to override S/MIME signing settings
- Enable user to select S/MIME signing identity
- Enable user to override S/MIME encryption settings
- Enable user to select S/MIME encryption identity**Enable S/MIME per-message signing and encryption** if required. |
  \| Allow Mail Drop     | Select to allow Mail Drop for this account. Mail Drop enables the user to send email with large attachments by storing the attachment in iCloud and placing a link to it in the email. For more information on Mail Drop go to: [**https://support.apple.com/**](https://support.apple.com/)                                                                                                                                                                                                                                                                                                                                                                                         |
  \| Per-App VPN         | The ability to associate a number of different per- app VPN profiles on Mail domains is supported by Apple. IMAP and POP3 email configurations are now supported over per-app VPN.**Prerequisite**: Configure Tunnel or per-app VPN configuration before configuring per-app VPN in email configuration.From the drop-down menu, **Select Per-App VPN config**.                                                                                                                                                                                                                                                                                                                  |

### Incoming Mail

| **Setting**          | **What To Do**                                                                                                                         |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| Mail Server and Port | The internet service provider (ISP) can give you this address.                                                                         |
| User Name            | Enter the user name for accessing the incoming mail server. This often the same as the email address. Your ISP can provide the format. |
| Authentication Type  | Select the authentication type defined by the ISP.                                                                                     |
| Password             | Enter the password for accessing the incoming mail server.                                                                             |
| Use SSL              | Select to use only the secure socket layer for communications between the device and the server.                                       |

### Outgoing Mail

| **Setting**                        | **What To Do**                                                                                                                                                                                           |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Mail Server and Port               | The internet service provider (ISP) can give you this address.                                                                                                                                           |
| User Name                          | Enter the user name for accessing the outgoing mail server. This often the same as the email address. Your ISP can provide the format.                                                                   |
| Authentication Type                | Select the authentication type defined by the ISP.                                                                                                                                                       |
| Password                           | Enter the password for accessing the outgoing mail server.                                                                                                                                               |
| Outgoing password same as incoming | Select if SMTP authentication uses the same password as POP/IMAP.                                                                                                                                        |
| Use Only in Mail                   | Select if you want this configuration used only by the email client. Other apps that send email, including apps that send content using the native email client, are not able to use this configuration. |
| Use SSL                            | Select to use only the secure socket layer for communications between the device and the server.                                                                                                         |
