---
title: Login Window Configuration - macOS
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

**Procedure**

1. Login to Ivanti Neurons for MDM.
2. Go to **Configurations** > **Add Configurations**.
3. Click (or Select) **Login Window**.
4. In the **Name** field, enter a name for the login window configuration.
5. Click **+ Add Description** to add details.
6. Under the **Configuration Setup** section, provide the following fields:\* **Admin Host Info**: Enter the hostname or IP address or SystemVersion.
   - **Allow List**: List of user GUIDs or group GUIDs of users that the system allows users to log in. An asterisk ('\*') string specifies all users or groups.
   - **Auto Login Password**: Enter the password for auto-login.
   - **Deny List**: The list of user GUIDs or group GUIDs of users that the system disallows logging in. This list takes priority over the list in the 'AllowList' key.
   - **Login Window Text**: Enter the login window text.
   - Select the checkbox for additional options like:\* **Disable Console Access**
     - **Disable FDE Autologin (FileVault Disk Encryption)**
     - **Disable immediate Screen Lock functions**
     - **Hide administrator users when showing a user list**
     - **Show only network and system users**
     - **Hide Mobile Accounts**
     - **Show Network users**
     - **Disables the logout menu item**
     - **Disable power off when the user is logged in**
     - **Disable the restart menu item when the user is logged in**
     - **Disable Restart item**
     - **Show the name and password dialog**
     - Show other users – managed
     - Show input menu
     - Disable the shutdown button
     - Disable the Sleep button
     - Disable the shutdown menu button
7. Click **Done**.
