---
title: Tenant Suspension
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

Access to a tenant used with an evaluation license or a production license might be suspended by Ivanti Neurons for MDM. An Evaluation License might be suspended when the evaluation period expires or when the usage allowance has been exceeded. A Production License might be suspended when the subscription period expires or when the usage allowance has been exceeded. Ivanti Neurons for MDM will restore a suspended tenant when the license has been renewed or when additional licenses have been purchased, in case of an overage.

### When a tenant license is suspended:

- Existing registered devices continue to function normally.
- Administrators cannot log in to the Admin portal.
- New devices cannot be registered.
- API access to the tenant is blocked.
- End users can continue to access the Self-Service portal.

### Tenant Suspension Action and Error Messages

| Suspension Action                                             | Error                                                   | Error message displayed                                                                                                                                                                                                                                                                                                                              | Location                         |
| ------------------------------------------------------------- | ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| End Customer-integration API access is blocked.               | API Call fails.                                         | Access denied. Your Evaluation License has expired. Please renew your license to re-enable API access. Contact your System Administrator for details.                                                                                                                                                                                                | API error 401.                   |
| New devices are blocked from registering.                     | An error message is displayed on the enrollment screen. | Unable to register your device. The license for your system has expired. Please contact your system administrator for details. Previously enrolled devices will continue to operate normally.                                                                                                                                                        | Following password verification. |
| Administrator is blocked from logging in to the Admin portal. | An error message is displayed on the login screen.      | Unable to login. Your License has expired. Please renew your license to regain access to the Admin Portal and to enroll new devices. Devices that have been previously enrolled devices will continue to operate normally. Contact your sales representative to renew your licenses. Note that the Admin password expires after one year (365 days). | Following password verification. |
