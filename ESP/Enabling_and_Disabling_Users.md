---
title: Enabling and Disabling Users
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Enabling and disabling local users**](./Enabling_and_Disabling_Users.md)
- [**Enabling and disabling LDAP users**](./Enabling_and_Disabling_Users.md)

The local and LDAP users can be in enabled or disabled status. Based on their status, you can create [**custom policies**](./Custom_Policy.md) using the User Enabled condition and setting an action for the condition in the rule builder. For example, there can be a custom policy rule to retire the devices that belong to disabled local/LDAP users.

## Enabling and disabling local users

By default, when a local user is created, the user is in enabled state.

**Procedure**

1. Go to **Users**.
2. Click the display name for the local user.
3. Click **Edit**. The **Authentication Required** window is displayed.
4. Enter your administrator password and click **Authenticate**.When multiple incorrect entries of the password are entered and if it crosses the 'Failed Logins Threshold limit' set in the 'Password Complexity Settings', the account will be locked and you will be logged out from the current session.
5. Select or deselect the **Enabled** option to enable or disable the local user respectively.
6. Click **Save**.

## Enabling and disabling LDAP users

You can enable or disable LDAP users only for Microsoft Active Directory. In Microsoft Active Directory, when you open the properties for a user account, click the **Account** tab, and then either select or clear the check boxes in the **Account** options dialog box, numerical values are assigned to the **UserAccountControl** attribute. The value that is assigned to the attribute tells Windows which options have been enabled. After you assign a value to the UserAccountControl attribute, the user status will reflect after LDAP sync with Ivanti Neurons for MDM.

Following are the possible values you can assign:

- 512 - Enabled.
- 514 - Disabled.
- 66048 - Enabled, password never expires.
- 66050 - Disabled, password never expires.

### View user accounts

**Procedure**

|   | 1. | Click **Start**. |
| - | -- | ---------------- |

|   | 2. | Go to **Programs**. |
| - | -- | ------------------- |

|   | 3. | Go to **Administrative Tools**. |
| - | -- | ------------------------------- |

|   | 4. | Click **Active Directory Users and Computers**. |
| - | -- | ----------------------------------------------- |

For more information, see [**https://support.microsoft.com/en-in/help/305144/how-to-use-the-useraccountcontrol-flags-to-manipulate-user-account-pro**](https://support.microsoft.com/en-in/help/305144/how-to-use-the-useraccountcontrol-flags-to-manipulate-user-account-pro).

You can view and edit the attributes by using either the Ldp.exe tool or the Adsiedit.msc snap-in. Only experienced administrators should use these tools to edit Active Directory. Both tools are available after you install the Support tools from your original Windows installation media.
