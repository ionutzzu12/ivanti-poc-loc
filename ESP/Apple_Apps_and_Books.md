---
title: Apple Apps and Books
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**License distribution of apps across multiple Apple Apps and Books accounts in a space**](./Apple_Apps_and_Books.md)
- [**Device-based and user-based license distribution**](./Apple_Apps_and_Books.md)
- [**Using device-based license option**](./Apple_Apps_and_Books.md)
- [**Using user-based license option**](./Apple_Apps_and_Books.md)
- [**Adding a Apps and Books app to the catalog**](./Apple_Apps_and_Books.md)
- [**Adding Apps and Books accounts**](./Apple_Apps_and_Books.md)
- [**Updating a Apps and Books secure token**](./Apple_Apps_and_Books.md)
- [**Updating the priority of a Apps and Books account**](./Apple_Apps_and_Books.md)
- [**Deleting a Apps and Books secure token**](./Apple_Apps_and_Books.md)
- [**Distributing licenses for a Apps and Books app in the catalog**](./Apple_Apps_and_Books.md)
- [**Viewing app licenses per user**](./Apple_Apps_and_Books.md)
- [**Apps and Books license usage notifications**](./Apple_Apps_and_Books.md)
- [**Viewing Apps and Books license usage**](./Apple_Apps_and_Books.md)
- [**Revoking Apps and Books license for an app**](./Apple_Apps_and_Books.md)
- [**Apps and Books behavior for macOS and iOS devices**](./Apple_Apps_and_Books.md)
- [**Apps and Books license entitlement when a device moves spaces**](./Apple_Apps_and_Books.md)

**License:** Silver

The **Apple Apps and Books** screen is available only if you have set up Apple Apps and Books in your [**app catalog settings**](./Catalog_Settings.md). This screen shows the app licenses that have been purchased for Apple devices via the Apple Apps and Books and how many have been used. Use this screen to:

- select the Apps and Books apps that will be included in your catalog
- distribute licenses for Apps and Books apps

For more information about distributing apps with Apps and Books, see the Ivanti Community article, [**Ivanti Neurons for MDM: How to Distribute Apps with VPP**](https://forums.ivanti.com/s/article/MobileIron-Cloud-How-to-Distribute-Apps-with-VPP-3465).

Apple Books may not be available in all countries or regions. In order to distribute licenses for apps via Apple’s Apps and Books you must enter the sToken provided by Apple.

## License distribution of apps across multiple Apple Apps and Books accounts in a space

- If the same app exists in multiple Apps and Books accounts, then the license will be distributed from the account in the order of priority of the accounts.
- If the same app exists in multiple Apps and Books accounts, and if the app license in the Apps and Books account with higher priority is exhausted, then the app would be distributed a license from the next prioritized account only if the user or the device is present in the license distribution list of the next prioritized account.
- A license will not be revoked and re-assigned on changing the priority of the Apps and Books accounts. The app would be distributed a license from the first account. If the licenses are exhausted in the first account, the app would be distributed a license from the next prioritized account, and so on.
- A user has an option to revoke all licenses of an app from the App Catalog page. This action would revoke the license of that app from all available Apps and Books accounts.
- Reserved licenses have precedence over priority of the Apps and Books accounts.

## Device-based and user-based license distribution

Whether the license for an app is Device-based or User-based depends on how you assign it. When assigning an app license to a device, it becomes a device-based license. When assigning an app license to a user, it becomes a user-based license.

A license is distributed when installing a Apps and Books app to a device, or when a token is issued for that app. If no licenses are available for the app, the user has the option of installing and paying for the app themselves. If a user has already been assigned a user-based license for the requested Apps and Books app, the app is installed using the existing user-based license, rather than the Apps and Books license.

In the case of [**Shared iPads**](./Shared_iPad_devices_for_business.md), Apps and Books are installed based on device-based licenses regardless of whether device-based licenses are selected or not.

## Using device-based license option

With device-based licenses, the users need not enroll in Apps and Books. The required apps will install automatically. Corporate supervised devices do not need to deal with an IT owned Apple ID.

During device check-in, the device is identified by the serial number and the required app is installed if there are licenses available. If no licenses are available the app is not installed. If a license for an app is reserved, then a device based license assignment will not occur at app installation.

Application updates for Apps deployed using Device based Apps and Books licensing are controlled by the administrator.

To control how an app will be updated, in **Apps > App Catalog** navigate to the **App Configurations/Install On Device** tab. You will be able to select an immediate update that will occur at the next device check-in, or you can choose to have the app update automatically when new versions become available.

**Important:** Before assigning a device-based license to a business to business (B2B) or productivity app, confirm the app is eligible for device-based licensing with the app developer.

## Using user-based license option

A user-based license remains valid for that user if they have to move from one device to another in case the device is lost or stolen or the user upgrades to a new device. With user-based licenses, the user must first enroll into Apple Apps and Books. Enrolling is a manual action that the end user must complete in the App Catalog. Required Apps and Books apps won’t be installed on the device until the user enrolls in the Apps and Books.

If the app is a required Apps and Books app and the license distribution is user-based:

- Required app install will not occur if the user is not enrolled in the Apps and Books program.
- Required apps may be installed if the user is enrolled in the Apps and Books program and a license is available.
- If the user is enrolled in Apps and Books, but there are no licenses available then the app will not be installed.

## Adding a Apps and Books app to the catalog

**Procedure**

1. Go to **Apps > App Catalog**.
2. Select an app and click **Add to Catalog**. Click **Next**.
3. Optionally, add a description of the app. Click **Next**.
4. Select a distribution option. Click **Next**.
5. Click the **App Configuration** tab.
6. Optionally, select **Install on device**. This configuration option installs the app without prompting the user on supervised iOS devices.
7. Select other configuration options if needed.

In the Apps and Books secure token info page, the following token details are displayed:

- Created date
- Location (if the token contains this information)
- Expiry date

## Adding Apps and Books accounts

Ivanti Neurons for MDM allows adding multiple Apps and Books accounts by adding multiple Apps and Books secure tokens in a single space.

Perform the following steps to add a Apps and Books secure token in a space:

1. Go to **Apps > Apple Apps and Books**.
2. Click **+ Add Apps and Books sToken**.
3. Enter a name and choose a token file.
4. Optionally, deselect the **Automatically distribute Apps and Books apps to all users** option. This option is selected by default, in which case the All Users group is used to distribute the FCFS licenses.
5. Optionally, select the **Clear all data from previous Apps and Books License** option to remove all app licenses associated with this token.
6. Click **Save**.

After the account is added, a list of all added Apps and Books accounts is displayed in the table.

## Updating a Apps and Books secure token

**Procedure**

1. Go to **Apps > Apple Apps and Books**.
2. Click the Apps and Books account name.
3. In the Token tab, click **Update sToken** (.stoken file).
4. Enter the token name and choose a token file.
5. Optionally, deselect the **Automatically distribute Apps and Books apps to all users** option. This option is selected by default, in which case the All Users group is used to distribute the FCFS licenses.
6. Optionally, select the **Clear all data from previous Apps and Books License** option to remove all app licenses associated with this token.
7. Click **Update**.

From the Token tab, click **Resync Apps and Books License Usage Information** to perform a full sync of all app and license information from Apple Apps and Books service. This action is only necessary if the license allocation information in Ivanti Neurons for MDM is not accurate. This inaccuracy may occur due to inconsistencies in Apple Apps and Books APIs.

## Updating the priority of a Apps and Books account

Administrators can assign a priority for each Apps and Books account in a space depending on which the licenses would be consumed. The priorities of the Apps and Books accounts are used to have a predictable license distribution system and resolve conflicts when a user or a device is eligible to receive a license from multiple Apps and Books accounts for the same app.

**Procedure**

1. Go to **Apps > Apple Apps and Books**.
2. Click **Edit Priority** against the required Apps and Books account name.
3. In the Edit Priority window, select a new priority.
4. Click **Save**.

## Deleting a Apps and Books secure token

Removing a Apps and Books secure token is irreversible and destructive. When a token is removed:

- Apps that have reserved tokens will have their tokens removed.
- Apps that were paid for will remain in the catalog and users can pay for them on their own.
- Apps that were installed by end users via the corporate Apps and Books account will need to transition to personal accounts if the users wish to use them. Users have a 30-day grace period to do so.

**Procedure**

1. Go to **Apps > Apple Apps and Books**.
2. Click the Apps and Books account name.
3. In the Token tab, click **Delete**.
4. In the Apps and Books Secure Token Delete window, select the **Yes, Delete the Apps and Books Secure Token** option to confirm.
5. Click **Delete**.

## Distributing licenses for a Apps and Books app in the catalog

1. Select **Apps > Apple Apps and Books** from the main menu.
2. A list of Apps and Books accounts is displayed. Under each account, a list of apps purchased through the Apps and Books program is displayed.
   Select an app and click **Distribute Licenses**.
3. Choose a distribution option, **First-come, first-served**, **Reserved**, or **Disallowed** in the Apps and Books Licenses section.

## Viewing app licenses per user

You can view license preference for your users by using the License Usage tab.

1. Click the **Users** tab
2. Select a user.
3. Click the **License Usage** tab.
   A list of apps is displayed with their Apps and Books License type and license assignment details.

To view the license usage for each app per user:

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Users** in the Ivanti Neurons for MDM main menu.
:::

:::WorkflowBlockItem
Select a user.
:::

:::WorkflowBlockItem
The **Devices** tab is displayed by default.

Click on the **License Usage** tab.

A list of all the apps installed on the user's device is displayed including the license status. The serial number for the device is listed in the Apps and Books License Type column for device based licenses.

- App name
- Version of the app
- Cost of the app
- Date the app was assigned
- Apps and Books license type
- Actions (License status.)
- Platform Information for License details.
:::
::::

You can also view the Apps and Books license usage for each app:

1. Go to **App > App catalog** in the Ivanti Neurons for MDM main menu.
2. Select an app.
3. Click on the **Apps and Books Licenses** tab if present.
4. Click an account name. Only apps purchased through the Apps and Books program will be displayed in this tab.
   A separate tab for each Apps and Books license type is displayed.

| **License type and log**                                                                                             | **Description**                                                                               |
| -------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| First Come First Served (FCFS)  - You have the option to select which user groups will receive this type of license. | - User Requested Apps - Apps the user chooses to install. A User based License is the default |

:::Paragraph{listStyleType="disc" indent="2"}
Required Apps - Apps that are required and are installed by Admin configuration using the **Install on Device** setting. These apps use Device based licenses by default. |
\| Reserved                                                                                                             | Reserved licenses have priority over FCFS licenses. Here you can select the users or devices to have a Reserved license for the app.                                                                                                                                      |
\| Disallowed                                                                                                           | Enter the users who are not allowed to have a license for this app. The user can still install the app, but they must purchase it.                                                                                                                                        |
\| Activity Log                                                                                                         | Displays the user, the type of Apps and Books license assigned to them, the date it was assigned, and the latest action taken on the license.                                                                                                                             |
:::

To view the detailed license usage for each app per device:

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Devices** in the Ivanti Neurons for MDM main menu.
:::

:::WorkflowBlockItem
Select a device.
:::

:::WorkflowBlockItem
Click on the **Installed Apps** tab.
:::

:::WorkflowBlockItem
A list of all the managed apps installed to the selected device is displayed including the license status.

- App Name
- Version of the app
- Platforms supported
- Source of the app
- Size of the app
- Apps and Books license type
- App reported (installed) date for iOS apps
  Search the installed apps for the device as follows:- App Name
- Bundle or Package ID
:::
::::

## Apps and Books license usage notifications

Apps and Books notifications help you track Apps and Books license usage. The notifications thresholds are defined as:

- An information notification is issued when over 50% of the licenses have been used.
- A warning notification is issued when 70 to 80% of the licenses have been used.
- A Critical notification is issued when 90 to 100 % of the licenses have used.
- Notifications are cleared when the usage drops below 50%.

To view license information for each app:

::::WorkflowBlock
:::WorkflowBlockItem
Click **Apps > Apple Apps and Books**.
:::

:::WorkflowBlockItem
License Information is displayed including:

- Name of the app.
- Cost of the license.
- Number of licenses available.
- Number of redeemed licenses.
  Go to **Dashboard > Notifications** to view details of a license notification.
:::

:::WorkflowBlockItem
The Notifications page is displayed.

Click on the notification title to see the details. See [**Dashboard**](./Dashboard.md) for the available notifications.
:::
::::

### Apps and Books license usage notifications

| **Trigger**   | **Severity** | **Notification Type** | **Component Type** |
| ------------- | ------------ | --------------------- | ------------------ |
| 50% Redeemed  | Info         | License Usage         | Apps and Books     |
| 70% Redeemed  | Warn         | License Usage         | Apps and Books     |
| 80% Redeemed  | Warn         | License Usage         | Apps and Books     |
| 90% Redeemed  | Alert        | License Usage         | Apps and Books     |
| 100% Redeemed | Alert        | License Usage         | Apps and Books     |

## Viewing Apps and Books license usage

The license usage details specific to a user is displayed in the license usage table in the license column.

1. Click an app.
2. Click the **License Usage** tab.
3. Enter a user name in the search field.

## Revoking Apps and Books license for an app

Apps and Books Licenses are revoked when a:

- Device is inactive (retired or wiped).
- Apps and Books app is deleted.
- Device based license is revoked when the device is retired.
- Apps and Books token is deleted.

To revoke a Apps and Books license for an app:

1. Select the app under **Apps > App Catalog**.
2. Click the **Apple Apps and Books&#x20;****Licenses** tab if present.
3. Perform one of the following tasks:1) Click **Revoke All Licenses** to revoke all licenses from all users or devices.
   2\) Click the **Activity Log** tab. Use the **Actions** column to revoke individual licenses on a per user or per device basis.

- For iOS devices, Apple allows a 30-day grace period for Apps and Books apps after the Apps and Books license is revoked. Therefore, the Apps and Books app remains installable.
- For macOS devices, after the Apps and Books license is revoked, the app still remains on the device.

To revoke a Apps and Books license for a user:

1. Click an app.
2. Click the **License Usage** tab.
3. Click the **Revoke License** link for the user whose access to the license should be removed.

Apps and Books licenses are automatically revoked if the user is deleted or the user removes the MDM profile from the device.

### Apps and Books Authentication Error Notifications

Some authentications errors might occur when using the Apple Apps and Books service. These Apps and Books Authentication errors notifications are:

| **Error Notification**       | **Action**                                               |
| ---------------------------- | -------------------------------------------------------- |
| Invalid Authentication Token | Upload a valid Apps and Books sToken                     |
| Expired Token                | Generate a new token online using your company's account |
| The sToken has been revoked  | Upload a valid Apps and Books                            |
| Login required               | Log into the Apps and Books service                      |

## Apps and Books behavior for macOS and iOS devices

### Apps and Books for iOS

| **Action**                                               | **Device-based License**                                    | **User-based License**                                      |
| -------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| Remove Apps and Books app from distribution for user     | App is uninstalled on user's device                         | App is uninstalled on user's device                         |
| Un-Delegate Apps and Books app                           | App is uninstalled from all devices in non-default space(s) | App is uninstalled from all devices in non-default space(s) |
| Deleting Apps and Books app from default or custom space | App is uninstalled from all devices                         | App is uninstalled from all devices                         |

### Apps and Books for macOS

| Action                                                   | Device-based License                                                  | **User-based License** |
| -------------------------------------------------------- | --------------------------------------------------------------------- | ---------------------- |
| Remove Apps and Books app from distribution for user     | App does not get uninstalled on user's device                         | NA                     |
| Un-Delegate Apps and Books app                           | App does not get uninstalled from all devices in non-default space(s) | NA                     |
| Deleting Apps and Books app from default or custom space | App does not get uninstalled from all devices                         | NA                     |

## Apps and Books license entitlement when a device moves spaces

When a device moves to a new space, the Apps and Books license that is assigned to the device or the device owner is revoked. A new Apps and Books license is assigned depending on the availability in the new space.

The following are the Apps and Books license entitlement scenarios:

| Scenario                                                                                                                                                                                         | Entitlement                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| A Apps and Books license is assigned to a device or a device owner in the source space and a Apps and Books license for the same app is available in the destination space.                      | Assign a license from the Apps and Books token in the destination space. |
| A Apps and Books license is assigned to a device or a device owner in the source space and no Apps and Books license for the same app is available in the destination space.                     | Revoke the license from the Apps and Books token in the source space.    |
| No Apps and Books license is assigned to a device or a device owner in the source space and a Apps and Books license for any installed Apps and Books app is available in the destination space. | Assign a license from the Apps and Books token in the destination space. |

If you cannot perform tasks on the **App Categories** page, it might be that you do not have the required permissions. You need one of the following [**role**](./User_Roles.md):

- App & Content Management
