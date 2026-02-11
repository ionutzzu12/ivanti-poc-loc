---
title: Device Cleanup Settings
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Device cleanup automates device life cycle for unused devices. You can retire devices that have been out of contact for a number of days that you specify. You can delete devices that have been retired for a number of days that you specify. The Audit Trails page captures the Retire Device, Delete Device, and Delete Wiped Device settings.

The following table provides information about the Android devices that support device cleanup settings:

| Mode                                                           | Retire if Out of compliance | Delete Retired | Force Retire or Retire Pending | Delete Wiped | Delete Wipe Pending |
| -------------------------------------------------------------- | --------------------------- | -------------- | ------------------------------ | ------------ | ------------------- |
| Android Work Profile (Profile Owner)                           | **YES**                     | **YES**        | **YES**                        | **NO**       | **NO**              |
| Device Admin/ Work Profile on Company Owned Device             | **YES**                     | **YES**        | **YES**                        | **YES**      | **YES**             |
| Work Managed Device / Android Managed Device with Work Profile | **NO**                      | **NO**         | **NO**                         | **YES**      | **YES**             |

**Prerequisites**

You must have System Management Role permissions to access this setting.

## Retire Devices

**Procedure**

|   | 1. | Go to **Admin** > **System** > **Device Cleanup**. The Device Cleanup page opens. |
| - | -- | --------------------------------------------------------------------------------- |

|   | 2. | Select **Retire Device**. |
| - | -- | ------------------------- |

|   | 3. | Use the **Retire Devices** table to specify the details. |
| - | -- | -------------------------------------------------------- |

|   | 4. | Click **Show not checked-in device list**. Shows the list of devices that are not checked in for specified number of days. |
| - | -- | -------------------------------------------------------------------------------------------------------------------------- |

|   | 5. | Click **Retired Devices Now**, alternatively, you can schedule the device retirement. |
| - | -- | ------------------------------------------------------------------------------------- |

|   | 6. | The Ivanti Neurons for MDM administrative portal will retire the specified devices. |
| - | -- | ----------------------------------------------------------------------------------- |

|   | 7. | Click **Save** to save your setting. |
| - | -- | ------------------------------------ |

|   | 8. | (Optional) If you update the values you can click **Reset** to reset the settings back to the initial settings. |
| - | -- | --------------------------------------------------------------------------------------------------------------- |

### Retire Devices

| Field                                                             | Description                                                                                                                      |
| ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **Retire Devices That Have Been Not Checked-In More Than (Days)** | Days: 30 days is default, 365 days is maximum number of days allowed.                                                            |
| **Maximum Devices to Retire in Each Session**                     | Select 100, 500, or 1000 (Default - 100).                                                                                        |
| **Automatically Retire Devices on a schedule**                    | Select the check box to retire devices based on a preset schedule.                                                               |
| **Retire Schedule Configuration**                                 | Select one of the following options to set the frequency of retirements:\* **Daily -&#x20;**&#x53;et to retire devices everyday. |

- **Weekly -&#x20;**&#x53;pecify the day of the week to schedule the retirement.
- **Monthly -&#x20;**&#x53;et to retire devices the first day of every month. |

## Delete Retired Devices

**Procedure**

1. Go to **Admin** > **System** > **Device Cleanup**. The Device Cleanup page opens.
2. Select **Delete Retired Device**.
3. Use the **Delete Retired Devices** table to specify the details.
4. Click **Show retired devices list**. Shows the list of devices that are retired for the specified number of days.
5. Click **Delete Retired Devices Now**, alternatively, you can schedule the device deletion.
6. The Ivanti Neurons for MDM administrative portal will delete the specified devices.
7. Click **Save** to save your setting.
8. (Optional) If you update the values you can click **Reset** to reset the settings back to the initial settings.

### Delete Retired Devices

| Field                                                          | Description                                                                                                                   |
| -------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Delete the Devices That have Been Retired More Than (Days)** | Days: 30 days is default, 365 days is the maximum number of days allowed.                                                     |
| **Maximum Retired Devices to Delete in Each Session**          | Select 100, 500, or 1000 (Default - 100)                                                                                      |
| **Automatically Delete Retired Devices on a schedule**         | Select the check box to retire devices based on a preset schedule.                                                            |
| **Delete Schedule Configuration**                              | Select one of the following options to set the frequency of deletion:\* **Daily -&#x20;**&#x53;et to delete devices everyday. |

- **Weekly -&#x20;**&#x53;pecify the day of the week to schedule the deletion.
- **Monthly -&#x20;**&#x53;et to delete retired devices the first day of every month. |

### Delete Wiped Devices

**Procedure**

1. Go to **Admin** > **System** > **Device Cleanup**. The Device Cleanup page opens.
2. Select **Delete Wiped Device**.
3. Use the **Delete Wiped Devices** table to specify the details.
4. Click **Show wiped devices list**. Shows the list of devices that are retired for the specified number of days.
5. Click **Delete Wiped Devices Now**, alternatively, you can schedule the wiped devices deletion.
6. The Ivanti Neurons for MDM administrative portal will delete the specified devices.
7. Click **Save** to save your setting.
8. (Optional) If you update the values you can click **Reset** to reset the settings back to the initial settings.

### Delete Wiped Devices

| Field                                                    | Description                                                                                                                         |
| -------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **Delete Devices That have Been Wiped More Than (Days)** | Days: 30 days is default, 365 days is the maximum number of days allowed.                                                           |
| **Maximum Wiped Devices to Delete in Each Session**      | Select 100, 500, or 1000 (Default - 100)                                                                                            |
| **Automatically Delete Wiped Devices on a schedule**     | Select the check box to delete wiped devices based on a preset schedule.                                                            |
| **Delete Wiped Schedule Configuration**                  | Select one of the following options to set the frequency of deletion:\* **Daily -&#x20;**&#x53;et to delete wiped devices everyday. |

- **Weekly -&#x20;**&#x53;pecify the day of the week to schedule the deletion.
- **Monthly -&#x20;**&#x53;et to delete wiped devices the first day of every month. |

## Delete Wipe Pending Devices

**Procedure**

1. Go to **Admin** > **System** > **Device Cleanup**. The Device Cleanup page opens.
2. Select **Delete Wipe Pending Device**.
3. Use the **Delete Wipe Pending Devices** table to specify the details.
4. Click **Show wipe pending devices list**. Shows the list of devices that are due to be wiped for the specified number of days.
5. Click **Delete Wipe Pending Devices Now**, alternatively, you can schedule the pending devices for deletion.
6. The Ivanti Neurons for MDM administrative portal will delete the specified devices.
7. Click **Save** to save your setting.
8. (Optional) If you update the values you can click **Reset** to reset the settings back to the initial settings.

### Delete Wipe Pending Devices

| Field                                                               | Description                                                                                                                                |
| ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Delete the Devices That have Been Wipe Pending More Than (Days)** | Days: 30 days is default, 365 days is the maximum number of days allowed.                                                                  |
| **Maximum Wipe Pending Devices to Delete in Each Session**          | Select 100, 500, or 1000 (Default - 100)                                                                                                   |
| **Automatically Delete Wipe Pending Devices on a schedule**         | Select the check box to delete wiped devices based on a preset schedule.                                                                   |
| **Delete Wipe Pending Schedule Configuration**                      | Select one of the following options to set the frequency of deletion:\* **Daily -&#x20;**&#x53;et to delete wipe pending devices everyday. |

- **Weekly -&#x20;**&#x53;pecify the day of the week to schedule the deletion.
- **Monthly -&#x20;**&#x53;et to delete wipe pending devices the first day of every month. |

## Retire the Retire Pending Devices

**Procedure**

1. Go to **Admin** > **System** > **Device Cleanup**. The Device Cleanup page opens.
2. Select **Retire the Retire Pending Device**.
3. Use the **Retire the Retire Pending Devices** table to specify the details.
4. Click **Show retire pending device list**. Shows the list of devices that are due to be retired for the specified number of days.
5. Click **Force Retire the Retire Pending Devices Now**, alternatively, you can schedule the pending devices to retire.
6. The Ivanti Neurons for MDM administrative portal will retire the specified devices.
7. Click **Save** to save your setting.
8. (Optional) If you update the values you can click **Reset** to reset the settings back to the initial settings.

### Retire the Retire Pending Devices

| Field                                                                           | Description                                                                                                                               |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Retire the Retire Pending Devices That have not checked-in more than (Days)** | Days: 30 days is default, 365 days is the maximum number of days allowed.                                                                 |
| **Maximum Retire Pending Devices to Retire in Each Session**                    | Select 100, 500, or 1000 (Default - 100)                                                                                                  |
| **Automatically Retire the Retire Pending Devices on a schedule**               | Select the check box to retire the retire pending devices based on a preset schedule.                                                     |
| **Retire the Retire Pending Schedule Configuration**                            | Select one of the following options to set the frequency of deletion:\* **Daily -&#x20;**&#x53;et to retire the pending devices everyday. |

- **Weekly -&#x20;**&#x53;pecify the day of the week to schedule the pending devices for retirement.
- **Monthly -&#x20;**&#x53;et to retire the pending devices the first day of every month. |
