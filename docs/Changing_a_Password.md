---
title: Changing a Password
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Changing password from the Users tab**](./Changing_a_Password.md)
- [**Applying password to never expire**](./Changing_a_Password.md)
- [**Removing the password to never expire setting**](./Changing_a_Password.md)

If a user has a System Management role, then only a Superuser or currently logged-in user can see the **Change Password** option.

You can change your Ivanti Neurons for MDM password. You can also change the password for another user if you have the permission.

**Procedure**

1. Click the Account icon (upper right).
2. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/08LhZiAB_dSZjKJZn2Gjp_usericon.png" alt caption}
   Select **Change Password** from the pull-down menu.
3. Enter your current password.
4. Enter your new password.
5. Enter your new password again.
6. To set the password to not expire, select **Set Password to Never Expire**.Setting the password to never expire overrides the **Password Expiration Period** defined under Users > User Settings > Password Complexity Setting.
7. Click **Done**.To reset local account password to expire, unselect **Set Password to Never Expire**. After the option is unselected, a pop-up window shows the previous password expiration date applied to the user.

## Changing password from the Users tab

**Procedure**

1. Go to **Users**.
2. Click the display name for the user.
3. Click **Edit** (upper left). The **Authentication Required** window opens. Administrators (who are either local users or LDAP users) are required to authenticate by entering the administrator password before editing the user.
4. Enter your administrator password and click **Authenticate**.When multiple incorrect entries of the password are entered and if it crosses the 'Failed Logins Threshold limit' set in the 'Password Complexity Settings', the account will be locked and you will be logged out from the current session.
5. Enter the current password in the **Current Password** field.This field will not be displayed if you are changing the password for another user.
6. Enter the new password in the **Change Password** field.
7. Confirm the new password.
8. Click **Save** (upper left).

## Applying password to never expire

1. Go to **Users**.
2. Select one or more users.
3. Click **Actions**.
4. Select **Assign Password Never Expire**. The **Set Local Account Password to Never Expire** window is displayed.
5. Click **Submit**.

## Removing the password to never expire setting

1. Go to **Users**.
2. Select one or more users.
3. Click **Actions**.
4. Select **Remove Password Never Expire**. The **Remove Local Account Password Never Expire** window is displayed.
5. Click **Submit**. After this setting is removed, the previous password expiration date will be applied to the users.
