---
title: Office 365 Auto Account Creation (macOS)
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:**

- Supported macOS devices.
- Recommended Microsoft Office 365 apps versions to be 16.13.x or later.

Configure user information and options to setup initial configuration for all Microsoft Office 365 applications.

This section contains the following topics:

- [**Creating a Office 365 Auto Account Creation configuration**](./Office_365_Auto_Account_Creation__macOS_.md)
- [**Office 365 Auto Account Creation settings**](./Office_365_Auto_Account_Creation__macOS_.md)

## Creating a Office 365 Auto Account Creation configuration

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **office** in the search field, and then click the **Office 365 Auto Account Creation** configuration.
4. Name and describe the configuration.
5. Enter the settings as described in the following Office 365 Auto Account Creation settings table.
6. Click **Next** to configure the distribution settings.
7. Click **Done**.

## Office 365 Auto Account Creation settings

| **Setting**                        | **What To Do**                                                                                               |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Office Activation Email Address    | Enter the user email address.                                                                                |
| Office Auto SignIn                 | Select to supress first-run windows. Only prompts user for required information such as O365 authentication. |
| Default to local Open Save         | Select to force the open/save panel to 'On My Mac' instead of 'Online Locations'.                            |
| Show what's new on Launch          | Select to display new feature information at the launch.                                                     |
| Visual Basic Macro Execution state | Select one of the following options:\* Disabled with warnings                                                |

- Disabled without warnings
- Enabled without warnings                                                                              |
  \| Disable Visual Basic External Dylibs  | Select to disable Visual Basic external dependencies.                                                                                                                                            |
  \| Allow Visual Basic To Bind System     | Select to allow the macros to use a DECLARE to bind to the system() OS API. This API allows the macros to execute arbitrary external processes and pass them arbitrary data on the command line. |
  \| Disable Visual Basic To Bind To Popen | Select to allow the macros to use a DECLARE to bind to the popen() OS API. This API allows the macros to execute arbitrary external processes and pass them arbitrary data on the command line.  |
  \| Disable Visual Basic Mac Script       | Select to allow the macros to invoke the Apple Script Visual Basic API.                                                                                                                          |
