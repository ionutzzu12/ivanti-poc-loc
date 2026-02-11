---
title: Android Work Challenge
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topic:

- [**Creating the Android Work Challenge configuration:**](./Android_Work_Challenge.md)
- [**Configuration Setup settings**](./Android_Work_Challenge.md)

**License**: Silver

An Android Work Challenge configuration defines secure passwords for users to access the Work Profile data and apps. Requires Android Enterprise Work Profile.

Implementation notes:

- Administrators can apply a device password policy and a work profile password policy independently.
- Ivanti Neurons for MDM does not send this configuration to clients earlier than Android 7.0 because such devices do not support this feature.
  Ivanti Neurons for MDM only sends this configuration to devices with an Android Enterprise Work Profile.

## Creating the Android Work Challenge configuration:

**Procedure**

1. Click **Configurations**.
2. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/1eY47BPxjy-M-iw6cL9te_r43workchallenge001.png" alt caption}
   Click **+Add**.
3. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/K7oxFe1jRlndgiWeHVO_D_r43workchallenge002.jpg" alt caption}
   Type "work" in the search field.
4. Select the  **Android Work Challenge** configuration.
5. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/K6p79vSnALXY5l2NlC5dq_r44workchallenge003.png" alt caption}
   Enter a name for the configuration, and, optionally, a description.
6. Use the Configuration Setup fields to create the configuration. Refer to [**Configuration Setup settings**](./Android_Work_Challenge.md) for details on the settings.
7. Click **Next ->**.
8. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/lLSBELnpAQlnVE-ltXrqG_r43workchallenge004.png" alt caption}
   Enable the configuration if desired.
9. Configure distribution settings, to all devices, no devices, or to a custom set of devices.
10. Click **Done**.

## Configuration Setup settings

| **Setting**                                        | **What To Do**                                                                                         |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Name                                               | Enter a name that identifies this configuration.                                                       |
| Description                                        | Enter a description that clarifies the purpose of this configuration.                                  |
| Enable any lock method                             | Allow user choice of any lock method, including pattern unlock. Overrides all other passcode settings. |
| Minimum passcode length                            | Select a minimum passcode length, from 4 to 16 characters.                                             |
| Allow simple values                                | Enable to allow the passcode to contain repeating, ascending, or descending character sequences.       |
| Require alphanumeric value                         | Enable to require the passcode to contain at least one letter and one number.                          |
| Complex character and element type characteristics | Configure complex character and element type requirements, ranging from:\* None                        |

- Minimum of 1 non-alphanumeric character
- Minimum of 2 non-alphanumeric characters
- Minimum of 3 non-alphanumeric characters
- Minimum of 4 non-alphanumeric characters |
  \| Fingerprint unlock                                 | Enable to allow users to unlock their devices with their fingerprint.                                                                                                                                                                                     |
  \| Maximum passcode age                               | Configure a maximum password age, from none to 730 days.                                                                                                                                                                                                  |
  \| Auto-lock                                          | Select a time period after which the device auto-locks. Times range from never to fifteen minutes.                                                                                                                                                        |
  \| Passcode history                                   | Specify the number of unique passcodes required before passcode reuse is allowed, ranging from none to 50 passcodes.                                                                                                                                      |
  \| Maximum number of failed attempts                  | Select the maximum number of failed attempts. **WARNING: Ivanti Neurons for MDM wipes devices for which the user exceeds the maximum number of password attempts!**                                                                                       |
