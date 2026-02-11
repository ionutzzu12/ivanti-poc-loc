---
title: Advanced Android Passcode and Lock Screen
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

The Advanced Android Passcode and Lock Screen configuration for Android devices enables you to keep your devices secure. This configuration is applied on devices to set device passcode and Work Profile on Company Owned Device passcode setting.

When this configuration is applied to a device, any Passcode configuration or Work Challenge configuration if they exist, will not be applied to the device.

For Work Profile and Work Profile on Company-Owned devices, the Passcode Quality is deprecated on Android 12+ devices for the device-level passcode. Also, the existing Passcode Quality settings are automatically translated to Password Complexity settings by the Go app if the admin has not enabled the Password Complexity setting.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Configuration > +Add**.
:::

:::WorkflowBlockItem
Select **Advanced Android Passcode and Lock Screen** configuration.
:::

:::WorkflowBlockItem
Enter a name and description for the configuration.
:::

:::WorkflowBlockItem
In the **Configuration Setup** section, configure the following settings:
:::

:::WorkflowBlockItem
\\

\\

| **Setting**                                                                                                                                                                                                                                                                                       | **What To Do**                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Device Passcode**                                                                                                                                                                                                                                                                               |                                                                                                                                                                             |
| **Require Device Passcode**                                                                                                                                                                                                                                                                       | Switch the toggle switch to **ON**.                                                                                                                                         |
| \*\*Passcode complexity (Android v12.0+)\*\*The **Passcode complexity** setting has higher priority than the **Passcode Quality** setting. When the **Require Device Passcode** option is toggled to ON and the **Passcode complexity** is set, the **Passcode Quality** setting will be ignored. |                                                                                                                                                                             |
| **Enable Passcode complexity**                                                                                                                                                                                                                                                                    | Switch the toggle switch to **ON** and select one of the following options:\* **None** - To avoid using any pattern or PIN or alphanumeric or alphabet sequence complexity. |

- **Low** - To set a passcode with a pattern or numeric with minimum 4 digits.
- **Medium** - To set a passcode with one of the following options: Numeric (with minimum 4 digits) or Alphabetic (with minimum 4 characters) or Alphanumeric (with minimum 4 characters).
- **High** - To set a passcode with one of the following options: Numeric (with minimum 8 digits) or Alphabetic (with minimum 6 characters) or Alphanumeric (with minimum 6 characters).                                                                                                                                                                                                                                                                                                                                                                                |
  \| **Passcode Quality**                                                                                                                                                                                                                                                                          | Select the passcode quality from the following drop-down list options:\* **Biometric** - Allows biometric unlock methods, such as face recognition.
- **Something** - Requires a passcode but doesn't set a type restriction.
- **Numeric** - Requires a passcode that includes at least numeric characters.
- **Numeric Complex** - Requires a passcode that includes at least numeric characters and has no repetition (example, 4444) or ordered sequences (example, 1234).
- **Alphabetic** - Requires a passcode that includes at least alphabetic or other symbol characters.
- **Alphanumeric** - Requires a passcode that includes at least numeric and alphabetic (or other symbol) characters.
- **Complex** - Requires a passcode that includes a numeric, alphabetic, and special character.                                                                                                                                                                                                                      |
  \| **Minimum Length**                                                                                                                                                                                                                                                                            | Move the slider to specify the minimum length of a passcode to prevent the user from creating short and insecure passcode. Number ranges between 4 to 16.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| **Passcode Lifecycle**                                                                                                                                                                                                                                                                        | Enter the values for the following fields:\* **Expiration** - Specifies the expiration of passcode in days.
- **History Length** - Specifies the number of passcodes before a user can re-use any given passcode.
- **Max Failed Attempts** - The maximum number of times the user can enter an incorrect passcode before corporate data is wiped from the device.
- **Inactivity Timeout** - Enter the maximum time a user may choose to be inactive before a session timeout.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
  \| **Manage Keyguard features**                                                                                                                                                                                                                                                                  | Enable the required keyguard features from the following checkbox options:\* Enable fingerprint
- Enable secure camera
- **Enable all notifications**Applicable for device owner mode.
- Enable all trust agentsApplicable for device admin and device owner mode only.
- **Enable iris scan**Applicable to Android 9.0+ or Samsung only.
- **Enable face unlock**Applicable to Android 9.0+ or Samsung only.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| **Manage Smart Lock (Android 6.0 +)**                                                                                                                                                                                                                                                         | Switch the toggle switch to **ON** to manage Smart Lock configuration.Enable the required Smart Lock configuration from the following checkbox options:\* Enable Bluetooth unlock
  - Disable audio/video devices
  - Disable computer devices
  - Disable health devices
  - Disable Imaging devices
  - Disable miscellaneous devices
  - Disable networking devices
  - Disable peripheral devices
  - Disable phone devices
  - Disable toy devices
  - Disable uncategorized devices
  - Disable wearable devices
    **Enable NFC unlock**
  - Enable unsecure tag
  - Enable secure tag
    **Enable places (location)**
  - Enable custom places (other than Home)
    **Enable face unlock (including Samsung face unlock)**
- Enable on-body unlock
- Enable Voice unlock                                                                                                                                                                                                                                                 |
  \| Work Profile Passcode (Challenge) (Android 7.0+)                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| **Require Work Profile Passcode (Challenge)**                                                                                                                                                                                                                                                 | Switch the toggle switch to **ON**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| **Passcode complexity (Android v12.0+)**                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \| **Enable Passcode complexity**                                                                                                                                                                                                                                                                | Switch the toggle switch to **ON** and select one of the following options:\* **None** - To avoid using any pattern or PIN or alphanumeric or alphabet sequence complexity.
- **Low** - To set a passcode with a pattern or numeric with minimum 4 digits.
- **Medium** - To set a passcode with one of the following options: Numeric (with minimum 4 digits) or Alphabetic (with minimum 4 characters) or Alphanumeric (with minimum 4 characters).
- **High** - To set a passcode with one of the following options: Numeric (with minimum 8 digits) or Alphabetic (with minimum 6 characters) or Alphanumeric (with minimum 6 characters).                                                                                                                                                                                                                                                                                                                                                                                |
  \| **Passcode Quality**                                                                                                                                                                                                                                                                          | Select the passcode quality from the following drop-down list options:\* **Biometric** - Allows biometric unlock methods, such as face recognition.
- **Something** - Requires a passcode but does not set a type restriction.
- **Numeric** - Requires a passcode that includes at least numeric characters.
- **Numeric Complex** - Requires a passcode that includes at least numeric characters and has no repetition (example, 4444) or ordered sequences (for example, 1234).
- **Alphabetic** - Requires a passcode that includes at least alphabetic or other symbol characters.
- **Alphanumeric** - Requires a passcode that includes at least numeric and alphabetic (or other symbol) characters.
- **Complex** - Requires a passcode that includes at least numeric, alphabetic, and special character.                                                                                                                                                                                                          |
  \| **Passcode Lifecycle**                                                                                                                                                                                                                                                                        | Enter the values for the following fields:\* **Expiration** - Specify the expiration of passcode in days.
- **History Length** - Specifies the number of passcodes before a user can re-use any given passcode.
- **Max Failed Attempts** - The maximum number of times the user can enter an incorrect passcode before corporate data is wiped from the device.
- **Inactivity Timeout** - Enter the maximum time a user may choose to be inactive before a session timeout.
  **Strong auth Timeout** (Applicable only for Android 8.0+ devices in Profile Owner, Device Owner, and Managed Device with Work Profile) - Specifies the time duration (in minutes) after which unlocking a device with a secondary authenticaton (Fingerprint, Biometrics) will timeout. This field is applicable only if **Biometric** or **Something** is selected as a **Passcode Quality** option.
  The minimum limit is 60 minutes and the maximum limit is 4320 minutes. If the field is set to blank, nothing is set to the device. |
  \| **Manage Keyguard features**                                                                                                                                                                                                                                                                  | Enable the required keyguard features from the following checkbox options:\* Enable fingerprint
- Enable secure camera
- Enable all trust agents
- Enable iris scanApplicable to Android 9.0+ or Samsung only.
- **Enable face unlock**Applicable to Android 9.0+ or Samsung only.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  Click **Next**.
:::

:::WorkflowBlockItem
Select one of the following distribution options:
:::

:::WorkflowBlockItem
- All Devices
- No Devices(default)
- Custom
  Click **Done**.
:::
::::
