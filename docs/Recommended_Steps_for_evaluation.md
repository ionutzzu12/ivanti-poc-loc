---
title: Recommended Steps for evaluation
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

The following steps are recommended to validate a solution:

1. Create a separate OU (User Group) which has a test user in your directory source (example, Active Directory). This will avoid any impact to active Organizational Units.
2. Sync users between Ivanti, Google, and directory source (LDAP). Verify that the “test OU” is available in User Groups.
3. Integrate Ivanti Neurons for MDM with Google as highlighted in steps above.
4. Create ChromeOS Blueprint Configuration and distribute this only to the “test OU” User Group.
5. Boot up a Chromebook (out of box or previously registered). Ensure it is available in the Devices list.
6. Verify that the ChromeOS Blueprint settings are available on the device.
7. Follow similar steps for Android app distribution.
