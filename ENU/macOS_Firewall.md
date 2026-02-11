---
title: macOS Firewall
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

**License:**&#x47;old

macOS Firewall manages the Application Firewall settings that are accessible in the Security Preferences pane on macOS devices.

**Applicable to**: macOS 12.3+

- **Allow built-in software to receive incoming connections** - If true, allows the built-in software to receive incoming connections.
- **Allow downloaded signed software to receive incoming connections** - If true, allows downloaded signed software to receive incoming connections.

**Applicable to**: macOS 12.0+

- **Enable logging** - If true, enables logging
- **Specify the type of logging**\* **Throttle**
  - **Brief**
  - **Detail**

**Applicable to:** macOS 10.12+

When you click **Enable Firewall**, you can select one or more of the following options:

- **Block All Incoming** - Select to prevent all sharing services from receiving incoming connections on macOS devices, such as screen sharing or file sharing. The following system services may still receive incoming connections:\* configd, which implements DHCP and other network configuration services
  - mDNSResponder, which implements Bonjour
  - racoon, which implements IPSec
- **Enable Stealth Mode** - Select to prevent macOS devices from responding to probing requests. Managed macOS devices still answer incoming requests for authorized apps, while ignoring unexpected requests, such as ICMP (ping).
- **Applications** - The list of applications with connections controlled by the firewall. Select specific apps for which you want to receive incoming connections on macOS devices.

Select **Add+** to add a row to the list of apps. Select the cell under **Bundle ID** to select the app whose incoming connections you want to explicitly allow. Select the check box in the **Allow Connections** cell to allow incoming connections from the selected app.

- The configuration must exist in a system-scoped profile. If more than one profile contains this configuration, then the most restrictive union of settings will be used.
  The **Automatically allow signed downloaded software** and the **Automatically allow built-in-software** options are not supported. However, both the options will be forced ON when this configuration is available.
  The Administrator can enable the stealth mode by specifying a device that cannot be discovered by the ping command.
