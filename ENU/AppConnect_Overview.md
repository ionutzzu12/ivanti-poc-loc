---
title: AppConnect Overview
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

AppConnect is a feature that containerizes apps to protect data on iOS and Android devices. Each AppConnect-enabled app becomes a secure container whose data is encrypted, protected from unauthorized access, and removable. Because each user has multiple business apps, each app container is also connected to other secure app containers. This connection allows the AppConnect-enabled apps to share data, like documents. Ivanti Neurons for MDM uses policies to manage the AppConnect-enabled apps.

For more information about AppConnect and how to configure and deploy AppConnect apps, see the *AppConnect Guide for Ivanti Neurons for MDM*.

## Status of Secure Apps

From the **Devices > Devices** page, click a device to view the **Overview** page. On this page, users can check the status of secure apps with the following information:

- **Secure Apps Status** - Indicates whether AppConnect is enabled or disabled.
- **Secure Apps Encryption Status** - Indicates whether AppConnect passcode is enabled or disabled.
- **Secure Apps Encryption Mode** - Indicates the encryption mode (such as AES 256).

In addition, these fields can be used:

- As filters (left pane) to narrow the device entries displayed when users are trying to find/filter devices.
- As rules while creating a dynamically managed device group.
- As distribution filters, which refine the devices that apps that will get distributed to based on defined rules.

For each secure app, administrators can review Container Policy and Configuration statuses (Installed, Applied, Sent, or Pending Install) in the **Configurations** tab of the device details page.
