---
title: Managing Apple devices in lost mode
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Enabling lost mode**](./Managing_Apple_devices_in_lost_mode.md)
- [**Performing lost mode actions**](./Managing_Apple_devices_in_lost_mode.md)
- [**Disabling lost mode**](./Managing_Apple_devices_in_lost_mode.md)

**Applicable to:** iOS 10.3+ Supervised devices

You can place a supervised device in lost mode through Ivanti Neurons for MDM. This means you report the device as lost to Apple servers, allowing you to retrieve the last recorded location of the device, as well as disable lost mode if the device is found.

## Enabling lost mode

You can report a lost device to Apple servers by placing the device in lost mode. After you have placed a device in lost mode:

- If the device is retired, you cannot disable lost mode.
- If the device is wiped, you cannot locate or track the device.

**Procedure**

1. Go to **Devices**.
2. Select the checkbox for the device.
3. Select **Actions** > **Common** > **Enable Lost Mode**.
4. Alternatively, navigate to the **Device Details** page by selecting the device name link. Click the action icon of the device and select **Enable Lost Mode**.

## Performing lost mode actions

After the lost mode is enabled, you can perform the following actions from the Lost Device Mode section:

- Push Message/Phone Number to iPhone
  - Enter a message to be displayed on the locked screen of the lost device.
  - Enter a contact number to be displayed on the locked screen of the lost device. If someone finds the device, they can call the number to report it.
    Lock Device
- **Refresh Device Location**If the device is wiped, you will not be able to locate the device.
- **Play Lost Mode Sound**Sound will play until the device is removed from lost mode or a user disables the sound on the device.
- **Refresh location**The **Refresh Location** option is added to **Lost mode** to view device location. The following details are displayed:\* **Latitude**: The latitude of the device location.
  - **Timestamp**: The time and date Timestamp from the payload is displayed.
  - **Longitude**: The longitude of the device location.

## Disabling lost mode

If a device in lost mode is retrieved, or the lost mode was enabled in error, you can disable lost mode.

If the lost device is retired from Ivanti Neurons for MDM, disabling lost mode will not work.

**Procedure**

1. Go to **Devices**.
2. Select the checkbox for the device.
3. Select **Actions** > **Common** > **Disable Lost Mode**.
4. Alternatively, navigate to the **Device Details** page by selecting the device name link and select **Lost Device Mode: Enabled** > **Disable Lost Mode**.
