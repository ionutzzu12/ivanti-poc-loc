---
title: eSIM Configuration
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

eSIM configuration configures cellular network on the devices with the RefreshCellularPlans Command. Administrators must obtain the eSIM carrier URL before mapping the cellular network to the device.

Applicable to: iOS, iPadOS, and Windows 11

Procedure for iOS and iPadOS devices

1. Go to Configurations >**+Add**.
2. Type eSIM in the search field, and then click the eSIM configuration.
3. Enter a Name and Description of the configuration.
4. Click on iOS/iPadOS.
5. Type the Carrier URL.
6. Click Next.
7. Select Enable this configuration option.
8. Select one of the following distribution options:\* All Devices
   - No Devices (default)
   - Custom
9. Click Done.

Procedure for Windows 11 devices

1. Go to Configurations >**+Add**.
2. Type eSIM in the search field, and then click the eSIM configuration.
3. Enter a Name and Description of the configuration.
4. In the Choose OS section, click on Windows.
5. In the Configuration Setup section, type the Carrier URL in Server Name textbox (in FQDN format).\* Is Discovery Server - Select to mark the server as discoverable.
   - Auto Enable - Select to enable the profile on the device once downloaded.
6. Click Next.
7. Select Enable this configuration option.
8. Select one of the following distribution options:\* All Devices
   - No Devices (default)
   - Custom
9. Click Done.

Reset eSIM to factory state (only for Windows 11 devices)

This option is available under the Device Details section of all devices. Clicking this option deletes all the eSIM profiles downloaded on the device.

**Important Notes - Applicable only for Windows eSIM Configuration**

- When an Ivanti Neurons for MDM enrolled device is wiped & re-enrolled; the old record of this device (with the status as Wiped) should be deleted from the Devices page to avoid provisioning issues with the eSIM configuration, onto this re-enrolled device.
- Repushing the same configuration to a device which already has downloaded the profiles, fails to download the profiles again. If the admin wants the device to download the profiles afresh, reset the eSIM module to factory state first and then push / repush of the eSIM configuration is recommended.
- When an eSIM configuration is provisioned successfully on a device; before retiring the device, admin should perform the eSIM wipe action, to ensure the downloaded eSIM profiles are erased from the device.
- Removal of the eSIM configuration will just delete the configuration from the device. If any eSIM profiles were discovered, downloaded, and activated on the device, such eSIM profiles will remain active until an eSIM wipe is performed.
- Performing an eSIM wipe action removes all the downloaded eSIM profiles from the device. However, the eSIM configuration which is in Installed state remains intact on the device. Admin needs to undistribute the eSIM configuration to remove the configuration from the device.
