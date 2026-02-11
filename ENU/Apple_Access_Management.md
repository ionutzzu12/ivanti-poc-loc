---
title: Apple Access Management
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

**Prerequisites**:

- Verify and lock the domain on Apple Business Manager or Apple School Manager.
- Configure at least one MDM server from the Apple Business Manager or Apple School Manager organizations, where managed apple IDs are present in the Ivanti Neurons for MDM.

Signing-in to Managed Apple ID allows organizations to control which Apple services and features users can access.

In Apple Business Manager or Apple School Manager, **Allow Managed Apple Account on** setting controls where users can sign in with their Managed Apple IDs. The administrators can configure this setting to restrict sign-in to managed or supervised devices, or allow it on any of the devices.

- **Any device** (default): Users can sign in with their Managed Apple IDs on any device, regardless of whether it's managed by an MDM solution.
- **Managed devices only**: Users can only sign in on devices managed by an MDM solution that supports the Get Token endpoint.
- **Supervised devices only**: Users can only sign in on devices that are supervised (and managed) by an MDM solution that supports the Get Token endpoint.

These settings are a part of the broader "Access Management" for Apple Services within Apple Business Manager and Apple School Manager.

With enhanced security, restricting sign-in to managed or supervised devices can improve data security by ensuring that work-related data is only accessible on controlled devices.

Managed Apple Account Login will fail if zero or multiple Device Enrollment MDM server organizations are present in the **Device Enrollment** tab and the administrator sets the **Allow Managed Apple Account on** setting present under **Access Management** > **Apple Services** is set to "Supervised Devices Only" or "Managed Devices Only" in Apple Business Manager or Apple School Manger.

The devices will fail to log in if the **Managed Apple** account is not present in the Ivanti Neurons for MDM Device Enrollment MDM server.
