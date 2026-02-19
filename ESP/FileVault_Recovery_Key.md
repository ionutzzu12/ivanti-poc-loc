---
title: FileVault Recovery Key
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

**License:** Gold

FileVault Recovery Key configuration determines redirecting and escrowing the FileVault recovery keys to a corporate server.

Exclude and Re-push of File Vault Recovery Key configuration is disabled as a macOS device stops sending recovery key on re-pushing the configuration.

You can set the following options:

| **Setting**                                         | **Description**                                                                                                                                       |
| --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                                                | Enter a name that identifies this configuration.                                                                                                      |
| Description                                         | (Optional) Enter a description that clarifies the purpose of this configuration.                                                                      |
| Configuration settings for macOS \< 10.13           |                                                                                                                                                       |
| Store Recovery key to Ivanti Neurons for MDM Tenant | Select to enable Ivanti Neurons for MDM to store the keys on your tenant. When needed, the key can be decrypted from the Device Details page.         |
| Redirect URL to Server                              | Enter the following settings:\* Enter **Redirect URL** to which FDE recovery keys should be sent instead of Apple. The URL must begin with https\://. |

- Select a Certificate from the dropdown list. Only PKCS1 format certificate is supported. |
  \| Configuration settings for macOS 10.13+             |                                                                                                                                                                                                                                                 |
  \| Location                                            | (Required) Enter a short description of the location where the recovery key will be escrowed. This text will be inserted into the message the user sees when enabling FileVault.                                                                |
  \| Device Key                                          | (Optional) Enter a string to be included in the help text if the user appears to have forgotten the password.                                                                                                                                   |
