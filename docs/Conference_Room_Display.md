---
title: Conference Room Display
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** tvOS 10.2 and supported newer version.

This configuration will turn on the Conference Room Display mode on Apple TV. Conference Room Display mode locks Apple TV into that mode, to prevent other types of usage.

Beginning with tvOS 10.2, you can set supervised Apple TV devices to Conference Room Display mode. Conference Room Display locks scoped Apple TV devices to a black wallpaper screen and downloads a default screen saver, unless a background image and screen saver are manually defined in the Apple TV device settings. This mode can also display a message as configured in the Conference Room Display configuration.

The Conference Room Display configuration can be deployed automatically and apps can install while devices are in this mode. A device set to Conference Room Display mode that reboots will automatically resume locked screen without first showing the Home screen.

If an Apple TV device is running in Single App Mode or if Single App Mode is deployed with Conference Room Display, Conference Room Display will override Single App Mode. In addition, if an Apple TV device is connected to a network via Ethernet, Conference Room Display will not automatically display a Wi-Fi network to join for AirPlay sharing. This instruction can be displayed on the screen using the Custom Message field of the Conference Room Display configuration.

## Creating a Conference Room Display configuration

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **conference** in the search field, and then click the **Conference Room Display** configuration.
4. Enter a name and describe the configuration.
5. Specify the **Custom Message**. This is the custom message displayed on the screen in Conference Room Display mode.
6. Click **Next** to configure the distribution settings.
7. Click **Done**.
