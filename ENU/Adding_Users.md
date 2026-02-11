---
title: Adding Users
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Adding Users**](./Adding_Users.md)
- [**Adding multiple users**](./Adding_Users.md)
- [**Adding multiple users by uploading a file**](./Adding_Users.md)
- [**Adding an administrator**](./Adding_Users.md)
- [**Nobody user**](./Adding_Users.md)
- [**Viewing the device registration PIN information**](./Adding_Users.md)

You can add a single user or several users at a time. Once you have added many users, you might want to [**filter**](./Finding_and_Filtering_Users.md) the display to show only the ones you are interested in.

Other things you can do with users in this page include:

- [**assign**](./Assigning_Users_to_User_Groups.md) to/ [**remove**](./Removing_Users_from_User_Groups.md) from a user group
- [**send a message**](./Sending_a_Message.md)
- [**invite to register**](./Inviting_Users.md)
- [**assign roles**](./Assigning_Roles_to_Users.md)
- [**change a password**](./Changing_a_Password.md)
- [**delete**](./Deleting_a_User.md)
- [**generate a pin**](./Device_Registration_by_PIN_Generation.md)

All Device owner profiles are assigned a device account. Device accounts do not have any restrictions in the number of devices assigned to it. Work profiles (employee owned) are assigned user accounts.

## Adding a user

**Procedure**

1. Go to **Users**.
2. Click **+ Add** (top right).
3. Select **Single User**.
4. Complete the form with the user's information:\* Email Address
   - First Name
   - Last NameThe Username field displays the email address you entered. In most cases, you should not edit this default. For more information, see [**When to Edit a Username**](./Editing_a_Username.md)\* Display NameIf you want to change the display name for this user, edit the default text in the **Display Name** field.
5. If you want to assign a password, enter it in the **Password** and **Confirm Password** fields.
   - If you assign a password, you need to communicate it to the user for device registration.
   - If you do not assign a password, the user will need to create a password during device registration.
6. Select **Locale** from the drop-down list.
7. Enter **Managed Apple ID**. You can include "appleid" as a subdomain for Managed Apple ID to avoid any conflicts with existing Apple IDs. For example, [**user@appleid.yourdomain.com**](mailto\:user@appleid.yourdomain.com). The subdomain has to be a valid verified subdomain on Apple Business Manager.
8. The account cannot be updated with a different Managed Apple ID if there is an active User Enrolled device with the current account's Managed Apple ID.
   (Optional) Assign one or more user groups. Managed Apple ID cannot be updated when there is a device with status "Active" and "Retire Pending."
9. If you want to set up other features before inviting this user, clear the **Send this invitation now** option. Otherwise, the invitation email will be sent when you click **Done**.
10. Click **Done** to add the user.

For Android devices, Device accounts are designed for single-use managed devices where a single local service account can be used to enroll a large number of devices. While creating a new user, the Android enterprise device Account available under **Admin > Google > Android Enterprise** must be enabled. Device Accounts are enabled by default (Instead of User Accounts) for Device Owner Managed Google Play Account enrollments.

Select the checkbox **Android enterprise device Account** to enable Android Enterprise work managed device enrollments attached to this account to be automatically assigned a Google Device Account.

While editing a local or LDAP user for Android devices, the Android Enterprise Device Owner Managed Google Play Account devices associated with the user will be assigned Device Accounts on the next device check-in, provided the following conditions are met:

- The  feature is enabled by selecting the checkbox **Android enterprise Device Account**.
- The Go App version on the Android device is 47 and above.

## Adding multiple users

**Procedure** :

1. Go to **Users** .
2. Click **+ Add** (top right).
3. Select **Multiple Users**.
4. By default, you can enter email addresses **Manually** . Type or paste the email addresses of the users, separated by commas.
5. Example: [**jdoe@mycompany.com**](mailto\:jdoe@mycompany.com), [**jsmith@mycompany.com**](mailto\:jsmith@mycompany.com), [**tjones@mycompany.com**](mailto\:tjones@mycompany.com)
   If you want to set up other features before inviting this user, clear the **Send this invitation now** option.
6. Otherwise, the invitation email will be sent when you click **Done**.
   Click **Done** to add the users.

## Adding multiple users by uploading a file

**Procedure**:

1. Go to **Users**.
2. Click **+ Add** (top right).
3. Select **Multiple Users**.
4. Select **Upload CSV**.
5. Click **Download CSV Template**.
6. Edit the template with the following information for each user:\* user ID (required)
   - email address (required)
   - password
   - first name
   - last name
   - display name
   - user groups
   - custom attributes
7. This is the same information you enter when [**adding a single user**](./Adding_Users.md). Do not exceed 10,000 entries in the file.
   Save the file.
8. Drag it to the upload area or select **Upload CSV** to select the file.
9. Once the uploaded user information is displayed, make any necessary edits.
10. Click **Next** (lower right).
11. If you do not want to send invitations right away, select **Do not send invitations** .
12. Click **Done**.

## Adding an administrator

**Procedure** :

1. Click **Add** (top right).
2. Select **Single User** .
3. Complete the form with the user's information:\* Email Address
   - First Name
   - Last Name
4. The **Username** field displays the email address you entered.
   If you want to change the display name for this user, edit the default text in the **Display Name** field.
5. Assign a password in the **Password** field.
6. Enter the password again in the **Confirm Password** field.
7. Click **Done** to add the user.
8. Communicate the password to the person who will help manage devices.

## Nobody user

The nobody user is a default user that cannot be deleted. The service applies this user to devices that do not have associated users, such as retired devices.

## Viewing the device registration PIN information

While adding new users, the generated registration PIN information is displayed to admins if the Device Registration Authentication Type is set to PIN Only. This information can be useful to assist users with device enrollments.

- For single users, the PIN is displayed via the **Users > Invite User to Register** action and also in the PIN Info section of the User Details page.
- For multiple users, the PINs are displayed as a column in the User List page in addition to the PIN Status (Valid or Expired), PIN Issued, and PIN Expires columns.

If you cannot perform tasks on the **Users** page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md) :

- System Management
- User Management
