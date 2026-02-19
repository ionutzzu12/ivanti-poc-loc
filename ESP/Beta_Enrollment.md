---
title: Beta Enrollment
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM can automatically enroll devices remotely at a later time if the device is supervised and runs iOS 18, iPadOS 18, macOS 15 or later. If necessary, a supervised device can be removed from beta programs and restrict a user from enrolling manually. This removes the need for manual steps performed by the user and allows for a streamlined process throughout the beta testing lifecycle.

**Prerequisites**

- Device Enrollment is mandatory for Beta Enrollment. For more information about Device Enrollment, see [**Device Enrollment**](./Device_Enrollment.md).
- To offer AppleSeed for IT beta versions without the need for an Apple Account, an administrator in Apple Business Manager or Apple School Manager must sign in to the AppleSeed for IT portal, and accept the terms and conditions on behalf of their organization for the current beta period.

## Connecting Ivanti Neurons for MDM to Beta Enrollment

To use Ivanti Neurons for MDM as the MDM server for Beta Enrollment, setup Apple Business Manager or Apple School Manager server token in Ivanti Neurons for MDM.

**Beta Enrollment section**

| Name                           | Description                                                                         |
| ------------------------------ | ----------------------------------------------------------------------------------- |
| **Organization Name**          | Name of the organization.                                                           |
| **Last Sync**                  | Date and time at which the sync was performed.                                      |
| **Status**                     | Status of the sync.                                                                 |
| **Beta Enrollment Token Sync** | Click **Sync** to sync the newly available Beta enrollment tokens for beta updates. |
