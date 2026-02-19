---
title: FileVault 2
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

**License:** Gold

FileVault 2 provides the ability to perform full XTS-AES 128 disk encryption on the contents of a volume.

When you Enable FileVault 2, the following settings are available for configuration:

| Category                | Settings                                            |
| ----------------------- | --------------------------------------------------- |
| FileVault User Settings | - Enable FileVault at SetupAssist**Default**: False |

- If true, and the payload is installed after enrolling with Ivanti Neurons for MDM in Setup Assistant, it requests the Setup Assistant to enable FileVault at setup time. Also, the system ignores all other keys in this payload, except for ShowRecoveryKey.**Prerequisite**:- Before you enable the file vault in the setup assistant, ensure that the **Await Device Configuration during Device Enrollment Setup** is enabled in the Device Enrollment Profile.
- Defer enabling FileVault until the designated user logs out
  - Always prompt user to enable FileVault
  - Maximum number of times a user can bypass enabling FileVault
    Do not request enabling FileVault at user logout time |
    \| Output Path                          | Enter the path to the location where the recovery key and computer information plist will be stored.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
    \| Personal Recovery Key                | \* Create a personal recovery key
- Display the personal recovery key to the user after FileVault is enabledThis option is visible only when **Create a personal recovery key** is enabled. By default the option is disabled.
- Enable Institutional Recovery Key: Using Keychain - if no certificate information is provided in this payload the keychain already created at /Library/Keychains/FileVaultMaster.keychain will be used.Select one of the following options:
  - Upload Certificate
  - Certificate
  - Use keychain on the Users System                                                                                                                                                                                                     |
    \| Rotate FileVault Key after \_\_ days | The admins can configure periodic rotation of FileVault keys for macOS devices to mitigate security risk of the deployed devices. Admins can set the rotation interval in terms of days.Only Personal Recovery Keys are rotated.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
