---
title: Enrolling to Zebra OTA service
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

When enrolled to the Zebra OTA(Over The Air) service you can enable the Zebra OTA configuration to receive and update the firmware details of Zebra devices registered with Ivanti Neurons for MDM.

Procedure

1. Go to **Admin > Infrastructure > Zebra OTA**. The **Zebra OTA Service** page is displayed.
2. Under the **Link to Zebra's OTA service**, click **Begin**.
3. Enter your Zebra OTA credentials to login and follow the steps to request an approval to avail the Zebra services.
4. Click **Complete Verification** to get the confirmation on the connection to the Zebra service. When the connection is confirmed, the status of the successful enrollment is displayed in the Zebra OTA Service page.

To revoke the enrollment, click **Revoke** under the **Actions** column. The **Revoke** action removes all Zebra OTA configurations from the existing configurations. To re-enroll with Zebra OTA, click **Refresh**. Refresh action has no impact on the existing configurations.

After enrollment, you can enable the Zebra firmware configuration which Go client receives and applies to Zebra devices (running on Android version 8.0 or supported newer versions) in Device Owner mode. When the configuration is applied, the firmware is downloaded and installed on the device as scheduled in the configuration. For more information on enabling the Zebra firmware configuration, see [**System Update Configuration**](./System_Update_Configuration.md).

On completion of firmware update, you can view the firmware update status on the Zebra device under the **System Update** column in the Devices page. The following are the possible status:

- **Unknown** - Not supported by client or OS
- **Current** - Device has the most current update available
- **Pending** - System update configuration is applied but the update has not been downloaded or applied
- **Downloading** - System update is being downloaded to the client
- **Available** - System update is currently available for the device
- **Error** - Error in download or installation.

The **Zebra Patch Version** column in the Devices page displays the Zebra patch information of the device.

The **Zebra Patch Version** is not supported for devices on Android 11 and later; only the **Zebra Full Upgrade** is supported.
