---
title: FAQs
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

This section lists some of the common FAQs you might have when using the ChromeOS devices on Ivanti Neurons for MDM.

- How does Chromebook management differ from other OS?
- Google allows only LDAP User Group-based distribution of configurations as of now and the administrator should ensure when working with configurations or apps, distribution is based on LDAP user groups. Local user groups and Device Groups are not supported for ChromeOS device management.
  What licensing do I need with Ivanti for managing ChromeOS devices?
- ChromeOS devices should have licenses such as Chrome Enterprise Upgrade or Chrome Education Upgrade. These can be purchased from resellers as part of hardware or as standalone licenses. Refer to Google documentation for more information. To get started with Chrome device management, Secure UEM (Unified Endpoint Management) licensing is required with Ivanti.
  Will Mobile Threat Defense (MTD) or a similar solution be available? Do I need a separate license for MTD?
- This is not available currently in the product, please refer to current limitations. We will provide more information on changes with feature capability via FAQ and release announcements.
  Why do the configs and apps tab not have details as is the case for other devices?
- Since configurations are distributed to User Groups and not applied based on the user logged in, at present the configurations are not shown in device details. Apps follow the same logic of distribution and have the same limitation. We will provide more information on changes with these limitations via FAQ and release announcements.
  How many configurations are currently supported for ChromeOS?
- With ChromeOS, we have reduced the number of configuration tiles available and have reduced the admin tasks associated with the configuration. We refer to this configuration as “ChromeOS Blueprint”. ChromeOS Blueprint supports close to 700 configurations on these devices. Refer to Google’s documentation for configuration options.
  How is it easy to manage one configuration for all devices?
- The administrators can simply clone an existing configuration and modify it (if required) for their respective user groups. You don’t have to start from scratch.
  How do I add VPN configuration to Chrome devices?
- This can be done using the Android apps, and not using native VPN.
  Do device actions such as Retire and Wipe work on these devices?
- Chromebooks in Enterprise are always managed by an organization and data on such a device is considered completely organizational. With this in mind:
  - Retire is blocked
  - Wipe is allowed
  - Lock is allowed
  - Unlock is allowed
  - Other actions – are not supported

:::Paragraph{indent="1"}
Which Chromebooks, in terms of hardware are supported by Ivanti?
:::

- Devices supported by Google Cloud device management solutions are inherently expected to be supported by Ivanti. Ivanti does not currently publish a list of specific hardware supported by Ivanti’s solution.
  Which version of Chrome OS is supported?
- Google Cloud supports only the latest stable version of ChromeOS and Ivanti’s support follows the model supported by Google due to the nature of backend integrations.
  Can you list the current limitations since this is the very first launch of this capability?

With new Chrome OS support, we are working hard towards providing capabilities that our customers are eagerly waiting for. Below are some limitations that admins should take notice of:

- Chrome OS extensions (browser apps) are not currently supported (as “apps”) for distribution.
- Managed app config for Android apps is not currently supported.
- Wi-Fi configuration API was recently released and is not currently supported.
- Certificate distribution is currently not supported.
- Distributing Ivanti Go (previously known as MobileIron Go) Android app is currently not supported.
- Ivanti Tunnel (VPN) app is currently not supported.
- Spaces and space delegation is currently not supported.
- Mobile Threat Defense solution is currently not supported.
- Ivanti’s Zero Sign-on solution is supported on these devices, categorized as unmanaged devices.
- Policy actions are not fully supported.
