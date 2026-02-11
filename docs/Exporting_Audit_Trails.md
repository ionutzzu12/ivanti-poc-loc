---
title: Exporting Audit Trails
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Audit Trails export is a feature which is used to export and upload all the audit trails information to a specific server location. The server should be accessible from the default port. Users can configure Audit Trail Export settings to get archives of Audit Trails automatically uploaded to a specific location on a daily basis.

Audit Trails export is supported on Linux-based and Windows-based SFTP servers.

To configure the settings for exporting Audit Trails:

1. Select **Admin > Infrastructure > Audit Trails**. The **Audit Trails** page is displayed.
2. In the **Audit Trails** page, click **ON** to enable the export of audit trails.
3. In the **Export** section, update the following fields:

| **Feature**       | **Description**                                                                                  |
| ----------------- | ------------------------------------------------------------------------------------------------ |
| **Export format** | Select any of the following format in which the Audit Trails data should be exported:\* **JSON** |

:::Paragraph{listStyleType="disc" indent="2"}
**CEF** (Common Event Format)The CEF log message contain the following default values:\* Version : CEF format version number. v25 is the current supported version.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Device Vendor: Ivanti Inc
:::

:::Paragraph{listStyleType="disc" indent="3"}
Device Product: Ivanti Neurons for MDM
:::

:::Paragraph{listStyleType="disc" indent="3"}
Device Version: Latest Ivanti Neurons for MDM version at the time of event generation.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Device Event Class ID: Entity ID unique per trail
:::

:::Paragraph{listStyleType="disc" indent="3"}
Name: Entity name and action per trail. Example: Promotion distribution configuration settings Create.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Severity: Specifies the importance of the event. Example: Low\.The CEF log message also includes extension fields which are a collection of the following key-value pairs:\* CS1 & CS1Label: Audit Trails meta data such as createdAt, entityType, entityName, and actionType.
:::

:::Paragraph{listStyleType="disc" indent="3"}
CS2 & CS2Label: Actor information.
:::

:::Paragraph{listStyleType="disc" indent="3"}
CS3 & CS3Label: Before action state.
:::

:::Paragraph{listStyleType="disc" indent="3"}
CS4 & CS4Label: After action state.In CEF export, if any of the fields(example: CS3 or CS4 keys) exceed the specified limitations, the actual value is replaced with the text "Value for this key exceeds mapped dictionary key allowed length". |
\| **Server**                 | Enter the name of the server to exporting Audit Trails.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
\| **User**                   | Enter the user name to login to the server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
\| **Password**               | Enter the server login password.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
\| **Server path**            | Enter the path of the server and ensure that the given path exists on the server. Example: /Users/Test/Export.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
\| **Key Exchange Algorithm** | Select the list of key exchange algorithms for exporting audit log for the outgoing SFTP configuration.The following key exchange algorithms are selected by default:\* **diffie-hellman-group-exchange-sha1**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**diffie-hellman-group14-sha1**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**curve25519-sha256**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**diffie-hellman-group-exchange-sha256** (selected by default)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
\| **Ciphers**                | Select the list of encryption ciphers for exporting audit log for outgoing SFTP configuration. The following encryption ciphers are selected by default:\* **aes128-ctr**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**aes192-ctr**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**aes256-ctr** (selected by default)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
\| **HMAC**                   | Select the list of HMAC algorithms for exporting audit log for the outgoing SFTP configuration.\* hmac-sha1 (selected by default)
:::

:::Paragraph{listStyleType="disc" indent="2"}
hmac-sha2-256
:::

:::Paragraph{listStyleType="disc" indent="2"}
hmac-sha2-512                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
The fields mentioned above will be in read-only mode if these fields are already configured. To edit the configured fields, you should click the **Edit** button. If the admin had already configured SFTP export, then after the upgrade all the Key Algorithms are selected.
:::

:::Paragraph{indent="1"}
Click **Test Connection and Save** to test the server connection and to save the Audit Trails export configuration.
The archived Audit Trails files are available in JSON format in a .zip file.
Verify the configuration settings in all the fields before saving the Audit Trails export settings,. An error message is displayed if any of the entered field values are invalid.
:::
