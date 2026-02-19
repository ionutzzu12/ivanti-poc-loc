---
title: User Roles
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

User roles determine the pages users can see in Ivanti Neurons for MDM and the things users can do. The following table lists the roles you can assign and what they mean.

| **Role**                 | **Description**                                                                                                     | **Space-Specific** |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------- | ------------------ |
| System Management        | Allows an administrator to manage tenant-level settings such as MDM Certificates, App Catalog Settings and more.    | No                 |
| System Read Only         | Allows an administrator to view tenant-level settings such as MDM Certificates, App Catalog Settings and more.      | No                 |
| User Management          | Allows an administrator to add and remove users, assign roles and add users to user groups.                         | No                 |
| User Read Only           | Allows an administrator to view users and user groups as well as the apps and content catalogs.                     | No                 |
| Device Management        | Allows an administrator to manage device groups, configurations and policies as well as perform all device actions. | Yes                |
| Device Read Only         | Allows an administrator to view device groups, configurations and policies.                                         | Yes                |
| App & Content Management | Allows an administrator to add, distribute and remove Apps and Content.                                             | Yes                |
| App & Content Read Only  | View data in Users, Apps, Content, including AppConnect tasks                                                       | Yes                |
| Device Actions           | Allows an administrator to initiate device actions, such as:\* Force Check-in                                       |                    |

- Lock
- Unlock
- Send Message
- Retire
- Wipe****You must select Device Read Only  before selecting Device Actions. Otherwise, users will not have the expected permissions. | Yes                |
  \| LDAP User Import and Invite          | Allows an administrator to register LDAP Users and send invitation(s) to register device(s)                                                                                                                                                                | No                 |
  \| Cisco ISE Operations                 | Allows an administrator to invoke API(s) required for Cisco ISE integration.                                                                                                                                                                               | No                 |
  \| Scheduled Task Management            | Allows an administrator to create and manage Scheduled Task(s) for various administrative operations.                                                                                                                                                      | No                 |
  \| Common Platform Services (CPS)       | Allows an administrator to use Common Platform Services.                                                                                                                                                                                                   | No                 |
  \| Low User Impact Migration Management | Allows an administrator to manage Low User Impact Migration settings.                                                                                                                                                                                      | No                 |
  \| Custom Device Enrollment             | Allows an administrator to enroll a device using custom device enrollment.                                                                                                                                                                                 | No                 |
  \| Edit Microsoft Graph                 | Allows an administrator to edit Microsoft Graph API settings used for Office 365 Apps protection.                                                                                                                                                          | No                 |
  \| View Microsoft Graph                 | Allows an administrator to view Microsoft Graph API settings used for Office 365 Apps protection.                                                                                                                                                          | No                 |
  \| Send/Cancel Wipe                     | Allows an administrator to send a Wipe command to a device or cancel an issued Wipe command before it is executed.                                                                                                                                         | No                 |
  \| Manage Access Integration            | Allows an administrator to manage Access integration.                                                                                                                                                                                                      | No                 |
