---
title: Samsung Phone Restrictions Configuration
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

[**Configurations**](./Configurations.md)

Samsung Phone restrictions configuration allows you to set call restrictions and exceptions in Samsung devices. These restrictions limits the phone numbers that users can make or receive.

**Applicable to:** All Samsung devices with Knox SDK 2.0+.

To configure Samsung Phone restrictions:

1. In the **Configuration** tab, click **+Add**.
2. Select **Samsung Phone Restrictions** configuration. The **Samsung Phone Restrictions Configuration** page is displayed.
3. In the **Name** field, type an appropriate name for the configuration.
4. Click the +**Add Description** link to add a description for the configuration.This field is optional.
5. In the **Configuration Setup** section, configure the following options:|                         |                                                                                                                                                                                                                          |
   \| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   \| **Option**              | **Description**                                                                                                                                                                                                          |
   \| **Incoming Calls**      |                                                                                                                                                                                                                          |
   \| **Blocked numbers**     | Click the Add icon to add numbers and Java regular expressions to define restrictions on incoming calls.                                                                                                                 |
   \| **Allowlisted numbers** | Click the Add icon to add numbers and Java regular expressions to define allowed numbers out of a larger set of blocked numbers for incoming calls.This option will not have any effect if there are no blocked numbers. |
   \| **Outgoing calls**      |                                                                                                                                                                                                                          |
   \| **Blocked numbers**     | Click the Add icon to add numbers and Java regular expressions to define restrictions on outgoing calls.                                                                                                                 |
   \| **Allowlisted numbers** | Click the Add icon to add numbers and Java regular expressions to define allowed numbers out of a larger set of blocked numbers for outgoing calls.This option will not have any effect if there are no blocked numbers. |
6. Click **Done** to push the setting to the selected devices.When the device is retired, all the call restrictions are removed from the device.
