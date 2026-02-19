---
title: Google Configuration
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

Google account configuration connects iOS 9.3.2 and visionOS 1.1 or Android 6.0+ devices, or supported newer versions,  to Google accounts. Android enterprise is required for Google accounts. The configuration can set up multiple Google email addresses and any other Google services the user enables after authentication.

**Procedure**

1. Go to **Configuration > +Add**.
2. Select the **Google Account** configuration.
3. Enter a name for the configuration.
4. Enter a description.
5. In the Configuration Setup section, specify the remaining settings as described in the following table:

| **Setting**                          | **What To Do**                                                                                                                                                                                                                             |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **iOS 9.3.2+\*\*\*\*, Android 6.0+** |                                                                                                                                                                                                                                            |
| Name                                 | Enter a name that identifies this configuration.                                                                                                                                                                                           |
| Account description                  | Enter the display name of the account.                                                                                                                                                                                                     |
| Account name                         | Enter the full name of the user for the account.                                                                                                                                                                                           |
| Email address                        | Enter the Google email address of the account.                                                                                                                                                                                             |
| Per-App VPN                          | **Prerequisite**: Configure Tunnel or any per-app VPN configuration before configuring per-app VPN in Google Account configuration.From the drop-down menu, select the pre-configured per-app VPN configuration.**Applicable to**: iOS 14+ |
| **iOS 10+**                          |                                                                                                                                                                                                                                            |
| **Communication Service Rules**      | Choose a default app to use to make audio calls to contacts within the Google system by selecting any of the following options:\* **From App Catalog & System Apps**: Search for apps by typing the first few letters of the app name.     |

:::Paragraph{listStyleType="disc" indent="2"}
**Enter Bundle ID (for Apple system apps only)**: Type the System App Bundle ID. Bundle ID must begin with 'com.apple'. |
:::

7. Click **Next**.
8. Select one of the following distribution options:\* All Devices
   - No Devices (default)
   - Custom
9. Click **Done**.

When a Google account configuration is applied to the device, Go client prompts the user to log in to Google.
