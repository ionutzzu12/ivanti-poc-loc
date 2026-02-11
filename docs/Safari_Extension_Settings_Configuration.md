---
title: Safari Extension Settings Configuration
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM enables the management of Safari Extensions on supervised iOS and macOS devices. The administrators can effectively manage Safari Extensions for standard and private browsing.

Applicable to:

- iOS 18.0 Supervised through the most recently released version as supported by Ivanti Neurons for MDM.
- macOS 15.0 Supervised through the most recently released version as supported by Ivanti Neurons for MDM.

**Procedure**

1. Go to **Configurations** > **+Add**.
2. Search and select the **Safari Extension Settings** configuration.
3. Configure the **Safari Extension Settings** settings as per the following table:| **Setting**            | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                |
   \| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   \| Name                   | Enter a name that identifies this configuration.                                                                                                                                                                                                                                                                                                                                                                               |
   \| Description            | Enter a description that clarifies the purpose of this configuration.                                                                                                                                                                                                                                                                                                                                                          |
   \| Extension ID           | Enter the composed extension identifier. For example, “*Identifier (TeamIdentifier)*.”Enter “\*” for all extensions.To generate this string, use code sign *-dv \<path\_to\_appex>*. The browser extension is located in the plug-ins folder inside the app bundle. The expected format is "*Identifier (TeamIdentifier)*." For extensions that are not available on macOS, the app developer should provide this information. |
   \| Extension State        | Select one of the following options:\* **Allowed**: The user can turn on or off the extension.
   - **Always On**: The extension is always “On” for the user.
   - **Always Off**: The extension is always “Off” for the user.                                                                                                                                                                                                        |
     \| Private Browsing State | Select one of the following options:\* **Allowed**: The user can turn on or off the extension in Private Browsing.
   - **Always On**: The extension is always “On” for the user even during Private Browsing.
   - **Always Off**: The extension will not be available.                                                                                                                                                              |
     \| Allowed Domains        | Enter the domain or sub-domain values to grant the Safari Extension access.You can enter multiple domain or sub-domain values.The Allowed Domain settings are not applicable on the device if you enter "\*" in the Extension ID field.                                                                                                                                                                                        |
     \| Denied Domains         | Enter the domain or sub-domain values to restrict the Safari Extension access.You can enter multiple domain or sub-domain values.The Denied Domain settings are not applicable on the device if you enter "\*" in the Extension ID field.                                                                                                                                                                                      |
4. Click **+Add** to add multiple **Extensions**.
5. Click **Next** to configure the distribution settings.
6. Select one of the distribution options to set up the **Safari Extension Settings** configuration. For more information about configuring distribution options, see [**Working with Configurations**](./Working_with_Configurations.md).
7. Click **Done**.
