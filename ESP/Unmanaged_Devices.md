---
title: Unmanaged Devices
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Blocking a device**](./Unmanaged_Devices.md)
- [**Unblocking a device**](./Unmanaged_Devices.md)
- [**Clearing a device from the device list**](./Unmanaged_Devices.md)

**License**: Silver

If you have set up Sentry email access control, any unregistered devices that access your email system are called unmanaged devices. You define whether unmanaged devices should have access to email by default when you [**set up a Sentry**](./Sentry.md). You can then manually allow or block email access for these devices.

The Unmanaged Devices page is updated every 5 minutes. Therefore, changes in management are not immediately reflected.

## Blocking a device

**Procedure**

1. Select the device.
2. Select **Actions > Block**.

The device remains blocked until you select **Actions > Allow** or **Actions > Delete**.

## Unblocking a device

**Procedure**

1. Select the device.
2. Select **Actions > Allow**.

The device continues to have access to email until you select **Actions > Block** or **Actions > Delete**.

## Clearing a device from the device list

**Procedure**

1. Select the device.
2. Select **Actions > Delete**.

The next time the device attempts to access your email system, it will reappear on this list, and you will need to repeat any Block or Allow action you previously applied to the device.
