---
title: Time Server
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** macOS 10.12.4 and supported newer version.

Create Time Server configuration to allow devices to connect to custom time servers.

## Creating a Time Server configuration

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **time** in the search field, and then click the **Time Server** configuration.
4. Enter a name and describe the configuration.
5. Specify **NTP Server**.
6. Specify **Time Zone** string in Olson Time Zone ID format (for example, Pacific / Midway). To get the Olson Time Zone format, run the `"/usr/sbin/systemsetup -listtimezones`" command on the administrator's macOS device.
7. Click **Next** to configure the distribution settings.
8. Click **Done**.
