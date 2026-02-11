---
title: macOS Software Update Rules Configuration
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

Administrators can configure the software update policy of a device by defining the [**macOS Software Update Rules**](./macOS_Software_Update_Rules_Configuration.md).

Applicable to: macOS 10.7+

Procedure

1. Go to Configurations > +Add.
2. Type macOS in the search field, and then click the macOS Software Update Settings configuration.
3. Enter a Name and Description of the configuration.
4. Select the required configurations from [**macOS Software Update Rules**](./macOS_Software_Update_Rules_Configuration.md).
5. Click Next.
6. Select Enable this configuration option.
7. Select one of the following distribution options:\* All Devices
   - No Devices (default)
   - Custom.
8. Click Done.

## macOS Software Update Rules

Admins can select from the list of rules as follows:

Users cannot change these settings when these rules are applied on the device.

- Allowing pre-release software installation.
- Automatically:\* Check for updates
  - Download new updates when available
  - Install macOS updates
  - Install app updates from app store
  - Install system data files and security updates.
- Restrict App installations to admin users.
- Option to add URL of the software update catalog (unsupported on macOS 11+).
