---
title: Create Autonomous Single App Mode Configuration
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

The Autonomous Single App Mode configuration lets you ensure that only specific applications run on a device. Even if the user attempts to launch a different application, the configuration launches only the specific application.

Procedure

1. Go to **Configurations&#x20;**>**&#x20;Add&#x20;**>**&#x20;Autonomous Single App Mode**.
2. Use the following guidelines to define the app and related settings.

| **Setting**             | What To Do                                                                                                                                                                                                                              |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                | Enter a name that identifies this configuration.                                                                                                                                                                                        |
| **Description**         | Enter a description that clarifies the purpose of this configuration.                                                                                                                                                                   |
| **Configuration Setup** | **Bundle Identifier** - (Required) The unique bundle identifier. If two dictionaries contain the same BundleIdentifier value but a different TeamIdentifier value, this will be considered an error and the profile won't be installed. |
|                         | **Team Identifier** - (Required) The developer's team identifier, used when the app was signed.                                                                                                                                         |
| Click **Next**.         |                                                                                                                                                                                                                                         |

4. In the **Distribution** screen, select the groups to receive this configuration.
5. Click **Done**.
