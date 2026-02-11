---
title: Roles Management
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Roles are packaged groups of permissions that allows granting a set of permissions to an administrative user, while limiting their access to control specific areas of functionality. Ivanti Neurons for MDM provides a set of system roles that can be assigned (or edited) and a facility to create custom roles. Starting from Neurons for MDM 118 you can search for specific permission based on the category and all the options that are associated with the specific role or permission in the UI are displayed. A tool tip is displayed for the permissions that are added as dependent permissions.

The Roles Management page and the associated options are hidden for converged tenants who have access to both Ivanti Neurons for UEM and Ivanti Neurons for MDM.

There are two kinds of permissions available, and therefore two kinds of roles:

- **Space-specific roles** - The permissions are Space-specific, and therefore apply in a specific Space only. Examples are Device Management, App Management in a Space.
- **Cross-Space roles** - The permissions are, by nature, applicable to all roles. Examples are tenant-level settings such as MDM Certificates, App Catalog Settings.

## Creating a custom role

You can create a custom cross-Space or Space-specific roles. When you select a permission, the dependent permissions will be selected automatically. Accordingly, a user assigned with a custom role can only perform the specific actions (such as retire, wipe) that are available when the user visits the Devices page or the Device Details page.

When you apply the View User Registration PIN custom role, users can view the PIN of other users that have the same access level or with lesser privileges and the users cannot create PINs for other users.

The newly created custom role can not be assigned to anyone automatically. The tenant super admin needs to assign it to the required admin users who can later assign the same to other users as needed.

**Procedure**

1. Go to **Admin&#x20;**>**&#x20;Roles Management**.
2. Click **+Add Custom Role**.
3. In the **Create Role** page, enter the **Name** of the new role.
4. (Optional) add a description for the new role.
5. Under **Role Type**, select one of the following role types:\* **Cross-Space Role**
   - **Space-Specific Role**
6. Under **Permissions**, select the required granular permissions.
7. See the following table for Admin and User permissions.
   Click **Save**.

The following table lists the permissions, roles, and attributes you can use to create a custom role:

| **Role Type**        | **Permissions Category** | **Granular Permissions** |
| -------------------- | ------------------------ | ------------------------ |
| **Cross-Space Role** |                          |                          |
| **Admin**            |                          |                          |
|                      | Manage Custom Attributes | - Add Custom Attribute   |

- Delete Custom Attribute
- Edit Custom Attribute
- View Custom Attribute                                                                                                                                                                                                                                                                                                                                                                                                               |
  \|                         | Support Administrators          | \* Add Support Admins
- Delete Support Admins
- Disable Support Admins
- View Support Admins and Show Login History                                                                                                                                                                                                                                                                                                                                                                                             |
  \|                         | Certificate Authority           | - Add Certificate Authority
- Delete Certificate Authority                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \|                         | Connector                       | \* Add Connector Logs
- Delete Connector Logs
- View Connector
- Update Connector                                                                                                                                                                                                                                                                                                                                                                                                                               |
  \|                         | LDAP Management                 | - Add User/Group/OU
- Add Server
- Browse Server
- Delete Server
- Search Server
- Sync Server
- Remove User/Group/OU
- View ServeAll LDAP permissions in this section require View Connector permission. It will be automatically selected in the Connector section when you select any of these LDAP permissions.                                                                                                                                                                                            |
  \|                         | Licensing Management            | View Licenses                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \|                         |                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| **Users**               |                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \|                         | User Management Actions         | \* View User
- Update User
- Send Message to User
- Append/Assign Roles to User
- Create User
- Delete User
- Invite User
- View User Registration PIN                                                                                                                                                                                                                                                                                                                                                          |
  \|                         | Assign Custom User Attribute    | - Delete Attribute
- View Attribute
- Add/Edit Attribute                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
  \|                         | User Groups                     | \* View User Group
- Edit User Group
- Append/Assign Roles to User Group
- Create User Group
- Delete User Group                                                                                                                                                                                                                                                                                                                                                                                                |
  \|                         | Report Management               | - Create Report
- Edit Report
- Run Report
- Delete Report Record
- View Report
- Delete Report
- Download Report Record                                                                                                                                                                                                                                                                                                                                                                                       |
  \| **Devices**             |                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \|                         | Bulk Enrollment                 | \* Create Bulk Enrollment
- Update Bulk Enrollment
- Assign User to Bulk Enrollment
- View Bulk Enrollment
- Delete Bulk Enrollment                                                                                                                                                                                                                                                                                                                                                                             |
  \| **Space-Specific Role** |                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| **Devices**             |                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \|                         | Device Actions                  | - Assign Device to User
- Clear Device Activation Lock
- Delete Device
- Disable Device Lost Mode
- Enable Device Lost Mode
- Device Force Checkin
- Lock Device
- Unlock Device
- Device Force Logout
- Reinstall Device System Apps
- Restart Device
- Schedule iOS Device Updates
- Relinquishing Device Ownership
- Retire Device
- Cancel Retire Device
- Shutdown Device
- View Device
- Wipe Device
- Cancel Wipe Device
- Update Device OS Version
- Bulk Assign Via Upload
- Start TeamViewer Session |
  \|                         | Assign Custom Device Attributes | \* Add/ Edit Device Custom Attribute
- Delete Device Custom Attribute
- View Device Custom AttributeAll Assign Custom Device Attribute permissions in this section require Device Read permission. It will be automatically selected in the Device Actions section when you select any of these Assign Custom Device Attribute permissions.                                                                                                                                                                     |
  \|                         | Device Configurations           | - Exclude Profile
- Push Profile
- Push Excluded Profile
- Retry Install on Error                                                                                                                                                                                                                                                                                                                                                                                                                              |
  \|                         | Device Groups                   | \* Add Device Group
- Delete Device Group
- Edit Device Group
- View Device Group                                                                                                                                                                                                                                                                                                                                                                                                                               |
  \|                         | Bulk Enrollment                 | - Create Bulk Enrollment
- Update Bulk Enrollment
- Assign User to Bulk Enrollment
- View Bulk Enrollment
- Delete Bulk Enrollment                                                                                                                                                                                                                                                                                                                                                                             |
  \|                         | App Inventory                   | \* View App Inventory                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| **Configurations**      |                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \|                         | Configurations                  | - View/ Export Configs
- Edit/ Prioritize Configs
- Add/ Clone Configs
- Delete Configs                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| **Policies**            |                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \|                         | Policies                        | \* View Policies
- Edit/ Prioritize Policies
- Add/ Clone Policies
- Delete Policies                                                                                                                                                                                                                                                                                                                                                                                                                            |

|   |
| - |
|   |

To edit a role, go to Admin, Roles Management page and click the edit icon under **Actions** against the name of the role. A user cannot edit a cross-space role to a space-specific role and vice versa.

**Related topics**:

- To assign a custom role to a user, see [**Assigning Roles**](./Assigning_Roles_to_Users.md).
- See [**User Roles**](./User_Roles.md) for a list of default roles.
- [**Using Custom Reports**](./Using_Custom_Reports.md)
