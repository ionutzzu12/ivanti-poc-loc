---
title: Authenticate
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:**

- macOS 10.13 and supported newer version.
- Windows 10 and supported newer version.

Use the Authenticate configuration to provide password-less authentication for cloud services and/or desktop logins. Each device will have only one Authenticate configuration.

**Prerequisites**

- Zero Sign-On license is required.
- Ivanti Neurons for MDM should be registered with Access (Access profile should be configured).
- After configuring the Authenticate configuration, you cannot de-register Access profile as the Access profile will be referenced by the Authenticate configuration.
- If the Access profile has any changes, re-distribute the Authenticate configuration to the macOS devices. For Windows devices, copy and use the new CLI values in the new apps.

## Creating a Authenticate configuration

Procedure

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **auth** in the search field, and then click the **Authenticate** configuration.
4. Name and describe the configuration.
5. Select a **Desktop Identity Certificate** from the drop-down list.
6. Select one or both of the following OS option(s):\* macOS
   - Windows
7. For macOS:1) In the Custom Data region, click **+ Add** to add keys and string values for custom data to be pushed to the devices.
   2\) Click **Next** to configure the distribution settings.
   3\) Click **Done**.
8. For Windows 10 devices, this configuration helps in generating Command-Line arguments for the Authenticator MSI app for Windows as follows:1) Click **Done** to complete the Authenticate configuration.
   2\) From the **Configurations** page, view the Authenticate configuration to copy the displayed command line text. This text is required when distributing the Authenticate app for Windows devices.

When the Authenticate configuration is applied to Windows devices, the configuration stays in Pending Install state. You can ignore this as there will be no impact on the functionality.
