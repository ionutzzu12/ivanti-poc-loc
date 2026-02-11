---
title: Shared iPad devices for business
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Shared iPad devices for business is available for the Managed Apple IDs that are created in Apple Business Manager with iOS 13.4 or supported newer versions.

- Shared iPad devices enable businesses to share devices between multiple employees, while still providing a personalized experience.
- Employees can sign in with a Managed Apple ID to begin loading their data, including their mail accounts, files, iCloud Photo Library, app data, and more.
- The data is stored in iCloud, so employees can sign in to any Shared iPad device that belongs to the organization.

Shared iPad devices can be used in healthcare, retail, and industrial applications. For example, doctors and nurses can share one iPad device, as they can each securely access the user profile uniquely designed for them. In retail stores, front-line workers can be empowered with access to product information, resources, expertise to delight the customers and provide better shopping experiences.

How it works

- The iPad devices are added to Apple Business Manager, and are enrolled using an automated enrollment profile with the Shared mode on.
- Employees sign in to the Shared iPad device with a company-provided Managed Apple ID and password. Apple Business Manager administrator can manually create the accounts for the users or federate the account creation to an identity provider such as Entra ID.
- Each user can have their custom profile when they are logged into the Shared iPad device. Administrators can distribute apps based on the users role, responsibilities, and department.
- Users can log in as guest users on a Shared iPad device. The guest user log-in is enabled by default. A guest user need not sign in with a Managed Apple ID and password. The guest user login can be disabled by setting the **Allow Guest Session for Shared iPad** option to **False** in the [**iOS Restrictions**](./iOS_Restrictions.md) configuration.
- Go to Ivanti Neurons for MD&#x4D;**> Devices**, click on a Shared iPad device name, and click the **Users** tab to view the list of users on the device and their details (such as Managed Apple ID, Data Available in bytes, Data Used in bytes, Has Data to Sync to Ivanti Neurons for MDM).
- Go to the **Logs** tab, from the filters select the **Report User List** action to view additional user details.
- The guest user log-in in a Shared iPad device is different from the guest user management by Ivanti Neurons for MDM. By default, guest user account is disabled in Ivanti Neurons for MDM. To manage a guest user in a Shared iPad device, enable the guest user account.
- Screen recording is available from Control Center on Shared iPad devices.
- Ivanti Neurons for MDM supports a substitution variable for Managed Apple ID, `${managedAppleID}`. This system variable is displayed in the system attributes section and in the device attributes section.
- Ivanti Neurons for MDM restricts an administrator from changing the Managed Apple ID of resident user(s) who were logged in to the Shared iPad device in the past along with the currently logged in users. If you try to change the Managed Apple ID, an error message indicates that the user's Managed Apple ID cannot be changed since the user is using a Shared iPad device.
- In the case of [**Apple Apps and Books**](./Apple_Apps_and_Books.md), Apps and Books are installed on Shared iPad devices based on device-based licenses regardless of whether device-based licenses are selected or not.

Prerequisites

Ensure that the following prerequisites are met:

- A Shared iPad device requires Managed Apple ID. Administrators can manually create the accounts or federate to an identity provider such as Entra ID.
- The Shared iPad devices must contain iOS 13.4 or supported newer versions.
- The devices must be associated with Apple Business Manager accounts.
- The devices must contain storage of 32GB or more.

Note the following points:

- Ivanti Neurons for MDM restricts certain configurations, such as Passcode, for Shared iPad devices as Apple does not support them. Such configurations are not pushed to the devices (Devices > click a device name link > Configurations tab).
- The [**Passcode**](./Passcode_Configuration.md) configuration does not apply to the Shared iPad devices as they require Managed Apple IDs, which are associated with passwords and not passcodes. The Unlock action from the Ivanti Neurons for MDM administrative portal will not clear passcode on a Shared iPad device.
- Select either the Device Channel or the User Channel during the distribution of the [**iOS Restrictions configuration**](./iOS_Restrictions.md) to Shared iPad devices. You can distribute separate configurations and enforce restrictions that are applicable only to the device or the user channel.
- Ivanti Neurons for MDM verifies the expired accounts and retires the devices with expired accounts as owners. However, for a Shared iPad device, the device owner is the last logged-in user and may not be the legal owner. If an owners account expires, Ivanti Neurons for MDM excludes the Shared iPad devices from retiring .
- Go for iOS client is not supported for Shared iPad devices.
- Users cannot perform actions such as retire and wipe on Shared iPad devices. Only administrators can perform retire and wipe actions from the Ivanti Neurons for MDM administrative portal.
- Administrators cannot change the owner of Shared iPad device from the Ivanti Neurons for MDM administrative portal.
- Zero sign-on is not supported for Shared iPad devices.
- When the ListUsers command is enabled, all managed user IDs and their check-in time are displayed in the Device Enrollment (Part of Apple Business Manager) under the **Admin** tab.

## Configuring a Shared iPad device

You can set up a Shared iPad device and configure the settings.

**Procedure**

1. Go to **Admin&#x20;**>**&#x20;Apple&#x20;**>**&#x20;Device Enrollment**.
2. Add the device to Apple Business Manager by enrolling the device using an automated device enrollment profile. For information about this procedure, see [**Device Enrollment**](./Device_Enrollment.md).
3. In the Device Enrollment settings, enable:\* **Supervised Mode**.
   - **Multi-User Mode** under **Shared iPad device for business**.
4. (Optional) Create a local user account. The device will be registered to this user. The authentication as this user happens only once during the registration.
5. Reset the Shared iPad.The registration process starts only after the reset. It takes a few minutes for the device to be registered and configured as a Shared iPad device.
6. The legal owner is assigned to the user account who registered the device. The administrator can change the legal owner from the **Devices** page.
7. On the device login screen, enter the Managed Apple ID credentials of the user.\* Similar to macOS devices, you can push configurations on Shared iPad devices through both device and user channels.
   - The user substitution variables are not substituted for configurations (including the Managed App configuration) pushed in the device channel.
   - If the logged in user in a Shared iPad device is not a managed user- the Managed Apple ID does not belong to any user in the Ivanti Neurons for MDM administrative portal, the device is not assigned to anyone. The users will not be managed - the administrator cannot push user channel configurations from Ivanti Neurons for MDM.
   - By default, the default guest user created by Ivanti Neurons for MDM is disabled. When a guest user logs in, the device is not assigned to any user and the user is not managed. If the guest user has to be managed, the default guest user created by Ivanti Neurons for MDM must be enabled and the device is assigned to the default guest user after the guest user logs in. The user can then be managed.
   - The device owner information is displayed in the Ivanti Neurons for MDM > **Devices** page and in the device logs (device details page > **Logs**).

## Managing legal owners for Shared iPads

You search and view the legal owners of the Shared iPad devices using their email IDs from the device listing page. You can change the legal owners of the Shared iPad devices by reassigning the existing legal owners to the new legal owners. If the legal owner of a non-Shared iPad device is reassigned, Ivanti Neurons for MDM ignores the assignment.

Procedure

1. Go to **Devices**.
2. Click the gear icon to select and add the **Legal Owner** column to the devices list page.
3. Select the Shared iPad devices.
4. Click **Actions > Assign to Legal owner**.

## Sending an email to the legal owner of a Shared iPad device

You can send emails to the legal owner of a Shared iPad device.

**Procedure**

1. Go to **Devices**.
2. Click the name of the Shared iPad device.
3. Click the **email** icon.
4. Compose the email.
5. Click **Send**.

## Using the Multi-User Mode attribute

You can use the Multi-User Mode attribute of the Shared iPad devices in Ivanti Neurons for MDM.

**Procedure**

1. In the **Devices** page, use the **Multi-User Mode** attribute.
2. Click **Advanced Search** and create a rule to find the devices using the **Multi-User Mode** attribute.
3. In the **Devices > Device Groups** page, create a dynamic device group for the Shared iPad devices using the **Multi-User Mode** attribute. For example, you can use this group as a distribution filter to distribute configurations.
4. In the **Policies** page, create a custom policy for the Shared iPad devices using the **Multi-User Mode** attribute.
5. In the **Apps > Distribution\*\*\*\*Filter**, use the **Multi-User Mode** attribute to limit the number of applications available for installation.

- Ivanti Neurons for MDM does not support multi-user mode for Apple School Manager devices. It is not recommended to enable the setting and push the Device Enrollment profile to Apple School Manager devices.
- The Multi-user Secure Sign-In for iOS configuration is not applicable to Shared iPad devices.

## Deleting users from a Shared iPad device

You can delete a user or multiple user accounts from the Shared iPad devices. In the User list tab, the **Active** label is displayed for the currently logged in user. The Delete option is not applicable for the currently logged in user on the Shared iPad device. Users can be deleted from the **Devices** or the **Users** tab.

**Deleting users from the Devices tab**

**Procedure**

1. Go to the **Devices** tab > **Device Details**.
2. Go to the **Users** tab. The list of users are displayed.
3. Click **Delete All Users**.
4. Click the "**-**" minus sign to delete specific users.\* (Optional) In the **Delete User** window, select **Force delete user even if the data sync to Ivanti Neurons for MDM is pending** option and click **Yes**.
   Selecting **Force Delete user even if the data sync to Ivanti Neurons for MDM is pending** will force delete the user even if the data is not already synced to the Ivanti Neurons for MDM administrative portal.

**Deleting users from the Users tab**

**Procedure**

1. Go to the **Users** tab.
2. Select a user or multiple users, go to the **Actions** drop-down menu, click **Delete**. A confirmation message appears. After you confirm the delete user command is issued to the devices.
3. Go to **Device logs** in the device details and verify that the Delete user command is sent to the selected users of the Shared iPad device.

## Logging out users from a Shared iPad device

The administrator can log out users from a Shared iPad device.

**Procedure**

1. In the **Devices** page, select a Shared iPad device.
2. Select **Force Logout** from the **Actions** menu. A pop-up prompts for confirmation on logging out users from the Shared iPad device.
3. Click **OK** to approve the force logout.
