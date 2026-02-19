---
title: Catalog Settings
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Changing Apple App Management settings**](./Catalog_Settings.md)
- [**Setting Default App Store Region**](./Catalog_Settings.md)
- [**Enabling/disabling iOS app updates**](./Catalog_Settings.md)
- [**Enabling/disabling application ratings and reviews**](./Catalog_Settings.md)
- [**Uploading or updating an iOS/macOS Apps and Books sToken (License: Gold)**](./Catalog_Settings.md)
- [**Removing an iOS/macOS Apps and Books sToken from your Ivanti Neurons for MDM service**](./Catalog_Settings.md)

In the **Apps** > **Catalog Settings** page, configure the preferences you want to apply across all the applications in your App Catalog. You can do the following:

- Include app updates during device check-in
- Prevent backup to iCloud and iTunes (iOS only)
- Set default app store region (Apple and Microsoft)
- Remove iOS apps when the device is un-enrolled
- Enable Ivanti Neurons for MDM "Ratings and Reviews"
- Upload iOS and macOS Apps and Books tokens (requires Gold license)

## Changing Apple App Management settings

These settings will apply to all apps unless an app management configuration has been created for individual apps.

::::WorkflowBlock
:::WorkflowBlockItem
Select or clear one or more of the following check boxes:
:::

:::WorkflowBlockItem
- **Update apps during device checkin** (selected by default)
- **Prevent backup to iCloud and iTunes**
- **Remove apps on un-enrollment**
  Click **Save**.
:::
::::

## Notifications

::::WorkflowBlock
:::WorkflowBlockItem
Click the drop-down list under **Generate system notification when new app versions are available from Apple App store and Google Play Store**, and select one of the following options:
:::

:::WorkflowBlockItem
- **Once a week**
- **Once a day**
  Click the drop-down list under **Generate End-User Notifications for new app updates available in AppCatalog**, and select one of the options:
- **Once a week**
- **Once a day**
:::
::::

## Setting Default App Store Region

In the App Catalog settings, set default region for Apple and Microsoft app stores.

1. In the Default App Store Region section:\* Select **Apple App Store Region**.
   - Select **Microsoft App Store Region**.
2. Select or clear the option to use the last selected App Store region as the default region for each administrator. If this option is selected, then the app store region will be set as whichever region was last selected by each administrator and it will override the previous settings. If this is the first time an administrator is using this feature, then the default app store regions will be set to the previous settings in this procedure.
3. Click **Save**.

## Enabling/disabling iOS app updates

::::WorkflowBlock
:::WorkflowBlockItem
Select or clear **Update apps during device checkin.**
:::

:::WorkflowBlockItem
- By default, this option is selected.
- When cleared, any device checkin (including a force checkin by the admin) does not include app updates.
- However, the user can manually update the app by clicking the Force checkin action on the device app catalog.
- New app installations and all other configurations and settings will be updated during the device checkin.
  Click **Save**.
:::
::::

For a managed app, the admin can click the **Update** button on the app details page to manually update the app to the latest version from the App Store.

On a user's device, the user can click the **Force Checkin** button on the App Catalog menu to let the device checkin and let the app updates occur along with other configurations and updates.

These settings together allow end-users to choose when their apps get updated:

- Wait until connected to Wi-Fi to avoid data charges.
- Avoid being locked-out, at the wrong time, while the app updates.

## Enabling/disabling application ratings and reviews

This will allow users to rate and review the applications and for other users to read those reviews.

1. Select or clear **Enable Ratings and Reviews in the end user app catalog**.
2. Click **Save**.

The format of the Apps and Books sToken has changed. Instead of a character string in previous releases, it is now a character string stored in a text file in the vpptoken file format. Upload this file directly to the admin console for processing. The Apps and Books account page has been updated to display the Apps and Books organization name and expiration dates.

## Uploading or updating an iOS/macOS Apps and Books sToken (License: Gold)

1. Select **Add Apps and Books sToken**.
2. Enter a name for the sToken file in the **Alias Name** field.
3. Drag and drop the sToken file to the specified area or click **Choose File** to navigate to the sToken file.
4. Click **Save**, or if you are updating an sToken file click **Update**.
5. Go to the [**Apple Apps and Books**](./Apple_Apps_and_Books.md) page to view the apps associated with this token.

If Apps and Books tokens were reserved for individual users in a previous release of Ivanti Neurons for MDM, you must verify that the tokens are still reserved for those users and reserve them again if needed.

## Removing an iOS/macOS Apps and Books sToken from your Ivanti Neurons for MDM service

You can revoke an app that is no longer needed by a user, and reassign it as needed. If the app was deployed as a managed app with MDM for iOS/macOS, the you have the option of removing the app and all data immediately.

1. Select an app to remove.
2. Click **Delete**.A warning dialog appears.
3. Optionally, you can give the user a 30-day grace period to:\* Save their data.
   - Buy a personal copy of the app.
   - Transfer Apps they installed by this Apps and Books account to their personal accounts to continue use.

If you cannot perform tasks on the **Catalog Settings** page, it might be that you do not have the required permissions. You need the following [**role**](./User_Roles.md):

- App & Content Management
