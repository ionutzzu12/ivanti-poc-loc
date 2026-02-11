---
title: Deploying Divide Productivity with Android Enterprise
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

Divide Productivity is a PIM app you can deploy to Android Enterprise devices.

1. Go to **Apps > App Catalog**.
2. Under **Business Apps**, click **Divide Productivity**.
3. Enter additional categories or a description.
4. Click **Next**.
5. Accept the displayed permissions.
6. Click **Next**.
7. Select a distribution option.
8. Expand **Advanced Options & App Configuration**.
9. Use the following guidelines to enable options:

| Setting                                   | What To Do                                                                                                                                                                                                                                |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Blocks the user from uninstalling the app | Select to prevent the end user from uninstalling the app when it has been silently installed.                                                                                                                                             |
| Mail Address                              | Use variables to define the email address to associate with the app.                                                                                                                                                                      |
| Password                                  | Use variable to define the password for the email account. If you leave this field empty, the user will be prompted for the password.                                                                                                     |
| Host                                      | Enter the host name of the mail server to use. Enter the fully qualified domain name of the ActiveSync server. If you are using a Standalone Sentry, enter its fully qualified domain name (FQDN) instead.Example\:mySentry.mycompany.com |
| Server Type                               | Select the type of mail server.                                                                                                                                                                                                           |
| Username                                  | Use variables to define the username for the email account.                                                                                                                                                                               |
| Is SSL Required                           | Select if you want secure communication using https to the server that you specified in the Host field.                                                                                                                                   |
| Trust All Certificates                    | Select only if you want the app to automatically accept untrusted certificates.Typically, you select this option only when working in a test environment.                                                                                 |
| Default Email Signature                   | Enter the default email signature for all emails.that the end user can change this at any time. Once the device user changes it, later changes to this field have no effect.                                                              |
| Email Max Attachment Size                 | Enter the maximum size to be allowed for attached files.                                                                                                                                                                                  |
| Enable Task                               | Select to synchronize tasks.                                                                                                                                                                                                              |
| Login Certificate Alias                   | Enter the alias for the login certificate.                                                                                                                                                                                                |
| Smime Signing Certificate Alias           | Not currently supported.                                                                                                                                                                                                                  |
| Smime Encryption Certificate Alias        | Not currently supported.                                                                                                                                                                                                                  |
| Advanced Options                          |                                                                                                                                                                                                                                           |
| Install on Device                         | Select to prompt the user to install the app.                                                                                                                                                                                             |
| Silently install on Samsung Knox devices  | Select to install the app automatically on Samsung Knox devices.                                                                                                                                                                          |
| Do not show app in end user App Catalog   | Select if you do not want the app to appear in the app catalog on the device.                                                                                                                                                             |
| Select a promotion option.                |                                                                                                                                                                                                                                           |

11. Click **Done**.
