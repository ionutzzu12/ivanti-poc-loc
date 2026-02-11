---
title: Prioritizing Configurations
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

If you select multiple device groups for a configuration, then multiple configurations of the same type might be assigned to a given device.When configurations of the same type are applied to the same device, the defined priority determines which configuration is applied. The configuration with the highest priority has the lowest number. For example, the configuration with priority 1001 has a higher priority than the configuration with priority 1002. The service assigns numbers automatically.

WIFI priority cannot be applied to the device and is exempted from the priority.

This option is available only if the page contains two or more configurations of the same type and if a single space is selected in the drop-down list. You can change the priority of configurations.

**Procedure**

1. Go to **Configurations**.
2. With no configuration selected, select **Actions > Prioritize configs**.If **Actions** is not displayed, then you do not have multiple configurations of a type that requires priorities.
3. Use the arrows to move the configurations so that the one that should have the highest priority appears at the top.
4. A lock icon indicates that the configuration priority cannot be changed without editing the All Devices distribution setting in the configuration.
   Click **Save**.Prioritization can be done up to 400 configurations.

If you cannot see the Configurations page, it might be that you do not have the required permissions. You need one of the following roles:

- DeviceManagement
- DeviceReadOnly
