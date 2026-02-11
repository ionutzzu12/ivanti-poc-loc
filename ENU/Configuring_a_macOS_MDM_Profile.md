---
title: Configuring a macOS MDM Profile
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

The macOS MDM configuration defines access limits for Ivanti Neurons for MDM. The macOS MDM configurations are individually provisioned, for devices provisioned one by one.

Procedure

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Go to **Configurations**.
3. Select the macOS MDM configuration you want to edit.
4. Click the pencil (edit) icon to edit the configuration.
5. Use the following guidelines to make changes:

| **Setting**                                                           | What To Do                                                                                                                                                                                                                                                                                      |
| --------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Allow device lock and passcode removal                                | Uncheck to prevent enforcement of a passcode compliance configuration.                                                                                                                                                                                                                          |
| Allow device erase                                                    | Uncheck to prevent enforcement of a device wipe action.                                                                                                                                                                                                                                         |
| Allow query of Network information (phone/SIM numbers, MAC addresses) | Uncheck to exclude the device from networking information reporting.If this option is unchecked, then the device list view and device detail view will show N/A for the network information that is no longer reported. Also, the roaming policy will not be enforceable for affected devices.  |
| **Profile Removal Password**                                          |                                                                                                                                                                                                                                                                                                 |
| Password to remove Profile                                            | Specify a password. The user will be prompted to enter the password while deleting a profile from the device.                                                                                                                                                                                   |
| Click **Done**.                                                       |                                                                                                                                                                                                                                                                                                 |

Your changes apply only to the devices that are provisioned after you make the change.
