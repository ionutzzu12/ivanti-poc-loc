---
title: Setting up Kiosk Mode for Android
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Launching Kiosk Mode remotely**](./Setting_up_Kiosk_Mode_for_Android.md)
- [**Exiting Kiosk Mode**](./Setting_up_Kiosk_Mode_for_Android.md)

License: Silver

Kiosk Mode for Android devices enables you to restrict use of a device to specific apps. You might use Kiosk Mode to set up devices for employees who will use only work-specific apps.

When preparing Android devices for Kiosk mode or Device Owner with Kiosk mode, you will need to [**create a Allowlist of apps**](./App_Control_Configuration__Control_Which_Apps_Are_Installed_Per_Device.md) that you want to be available to users in Kiosk Mode. For devices using Device Owner you can add apps to the allowed apps list by dragging and dropping to arrange the apps in the order they should appear in the Kiosk Mode launcher when configuring the app. See [**Lockdown & Kiosk configuration**](./Lockdown___Kiosk__Android_Device_Admin_Mode.md) for more information.

**Prerequisites**

Before you configure Kiosk Mode for Android devices, ensure that you have performed the following tasks:

- Installed the Go on the devices.
- Configured the app catalog with the apps that your kiosk configuration will need.
- Distributed the app catalog to the devices that will run in Kiosk Mode.SonimXP5S devices do not support Kiosk mode.
- Installed the apps that your kiosk configuration will need.
- (Optional) Set up [**Android kiosk branding**](./Admin___Android_Kiosk_Branding.md).

Kiosk mode is supported on Android 5.1 and 6.0. Non- Samsung Knox must be placed in Device Owner mode to prevent the use of undesired applications.

**Important:** Some devices have features which can cause the device to draw over the screen or otherwise create an escape from Kiosk Mode. The People Edge feature of the Samsung Galaxy S6 Edge is an example of such a feature. We recommend that these types of features be turned off by an administrator before the device is deployed.

**Procedure**

1. Go to **Configurations**.
2. Click **+Add**.
3. Click **Lockdown & Kiosk: Android Device Admin Mode**.
4. In the **Create Settings** screen, complete at least the **Kiosk Mode Settings** section.
5. In the **Distribution** screen, select the device groups to receive this configuration.
6. Click **Done**.
7. For non-Samsung devices, continue with the following steps:1) Go to **Devices** > **Devices**.
   2\) Select the devices you want to enable for kiosk mode.
   3\) Select **Actions\*\*\*\*Force Check-in**.
   4\) On the devices, tap the **Kiosk Mode** button.
   5\) Press the **Home** button on the device.
   6\) If a **Choose Launcher** dialog appears, tap **Go Kiosk Launcher** and select **Always**. This step is necessary to ensure that the proper launcher will be used for this feature. Otherwise, the user would be prompted to select a launcher.

## Launching Kiosk Mode remotely

**Procedure**

1. Go to **Devices > Devices**.
2. Add the Kiosk Mode column to the display.
3. Select devices that have Kiosk mode enabled, but are not currently in Kiosk mode.
4. Select **Actions > Enter Kiosk Mode**.

## Exiting Kiosk Mode

You can exit Kiosk Mode on the device if you set a PIN in the configuration.

**Procedure**

1. Tap the **Settings** icon.
2. Select **Exit Kiosk Mode**.
3. Tap in the **Kiosk PIN** field when prompted.
4. Enter the kiosk PIN.

You can exit Kiosk Mode for a specific device from the portal:

**Procedure**

1. Go to **Devices > Devices**.
2. Display the details for the device.
3. Select **Actions > Exit Kiosk Mode**.

You can also use the following methods to exit Kiosk Mode:

- Delete the configuration
- Disable the configuration
- Remove the device group from the configuration
