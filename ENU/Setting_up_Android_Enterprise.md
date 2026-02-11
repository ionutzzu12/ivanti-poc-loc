---
title: Setting up Android Enterprise
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topic:

- [**Supported Devices**](./Setting_up_Android_Enterprise.md)
- [**Connecting Ivanti Neurons for MDM with Android Enterprise**](./Setting_up_Android_Enterprise.md)
- [**Getting Your Android Enterprise Credentials**](./Setting_up_Android_Enterprise.md)
- [**Adding your Android Enterprise MDM Token to Ivanti Neurons for MDM**](./Setting_up_Android_Enterprise.md)
- [**Synchronizing user between Ivanti Neurons for MDM and Google**](./Setting_up_Android_Enterprise.md)
- [**Active Directory/LDAP Users**](./Setting_up_Android_Enterprise.md)
- [**Local Users**](./Setting_up_Android_Enterprise.md)
- [**Deploying Android Enterprise to Supported devices**](./Setting_up_Android_Enterprise.md)
- [**Retiring Registered Devices**](./Setting_up_Android_Enterprise.md)
- [**Deploying the device**](./Setting_up_Android_Enterprise.md)
- [**Confirming Deployment**](./Setting_up_Android_Enterprise.md)
- [**Deploying Android Enterprise Apps**](./Setting_up_Android_Enterprise.md)
- [**Configuring Business Apps**](./Setting_up_Android_Enterprise.md)

**License**: Silver

Android Enterprise is a program offered by Google that enables mobility administrators to:

- Separate work and personal data
- Secure and manage enterprise apps
- Control system apps (such as Camera and Gallery)
- Centrally provision and configure apps in the Android Enterprise container
- Prevent data loss (screen capture)

You can configure Ivanti Neurons for MDM as the UEM server that manages Android Enterprise. Android Enterprise requires at least Android 3.0. There are two supported configurations of Android Enterprise, Device Owner and Managed Profile – Employee Owned.

## Supported Devices

Ivanti Neurons for MDM currently supports Android Enterprise only on devices that are running Android 5.0 and have Android Enterprise enabled by the manufacturer. Android Enterprise is required for Kiosk mode on devices running Android 5.0.

**Prerequisite**

If you have not already registered your domain with Google, you must first sign up for the program on the Google website:

[**https://admin.google.com.**](https://admin.google.com/)

During the process you will:

- Claim a domain (must match the domain for user email addresses)
- Receive a token
- Download a JSON client ID

Both items are required when you set up Android Enterprise on Ivanti Neurons for MDM.

After the process, you will receive an email containing instructions for verifying that you own the domain you claimed.

**If the company has already used its domain name** to sign up for Google Apps for Work, see [**https://support.google.com/work/android/answer/6174062**](https://support.google.com/work/android/answer/6174062) for information on enabling Android Enterprise.

## Connecting Ivanti Neurons for MDM with Android Enterprise

Once you have signed up for Android Enterprise, set up Ivanti Neurons for MDM as the UEM server.

## Getting Your Android Enterprise Credentials

**Procedure**

1. Go to **Admin > Android Enterprise**.
2. Click **Google Developers Console**.
3. Click the first displayed link to go to the Google Developers Console.
4. Select **Create a project** from the drop-down menu.
5. Enter a name for the project.
6. Accept the terms of service.
7. Click **Create**.
8. Click **API** .
9. Select **APIs**.
10. Type **emm** in the Search field to find the Google Play EMM.
11. Click the **Google Play EMM API** link.
12. Click **Enable API**.
13. Click **Credentials**.
14. Select **Service account**.
15. Click **Create** to save the JSON file.

## Adding your Android Enterprise MDM Token to Ivanti Neurons for MDM

**Procedure**

1. Log into [**https://admin.google.com.**](https://admin.google.com/)
2. Click **Security**.
3. If you do not see Android Enterprise Settings, click **Show More**.
4. Select **Android Enterprise Settings**.
5. Under **Manage enterprise mobility management provider**, copy the MDM token.
6. Return to the Ivanti Neurons for MDM portal.
7. Click **Done**.
8. In box 2, paste the MDM token you just copied.
9. In the **Domain** field, enter the domain you claimed with Google.
10. Click **Choose File** and upload the JSON file you downloaded.
11. Click **Connect**.The message **Connected to Google** displays when the connection is successful.
12. In box 3 click **Authorize** to indicate that you want to give Ivanti Neurons for MDM access to your Google user data.
13. Click **Accept**.The message **Connected to Users** displays in the Ivanti Neurons for MDM portal.

## Synchronizing user between Ivanti Neurons for MDM and Google

Before you deploy Android Enterprise to Android users managed by Ivanti Neurons for MDMIvanti Neurons for MDM, each user must have a corresponding record on the Google Admin Portal. The steps required for synchronizing the user information between Ivanti Neurons for MDM and the Google Admin Portal depend on whether you have set up an integration with your organization’s directory services (AD/LDAP).

## Active Directory/LDAP Users

If you have set up an AD/LDAP integration with Ivanti Neurons for MDM, then you must use Google Apps Directory Sync set up an AD/LDAP integration with the Google Admin Portal. See [**https://support.google.com/a/answer/106368?hl=en**](https://support.google.com/a/answer/106368?hl=en) for more information.

## Local Users

If you created only local users in Ivanti Neurons for MDM and do not intend to integrate it with a directory service, then complete the following steps to synchronize those users with the Google Admin Portal:

**Procedure**

1. Log into the Google Admin Portal at [**https://admin.google.com**](https://admin.google.com/).
2. Click **Users**.
3. Click the **Add user** or **Add multiple users** icon in the lower right corner.
4. For each Ivanti Neurons for MDM user that will use Android Enterprise, add a Google user with the same username and email address as the Ivanti Neurons for MDM user.
5. In the Ivanti Neurons for MDM portal for each Ivanti Neurons for MDM user that was just added to the Google Admin Portal\:a. Click the username link in the Users tab to display the user's details.b. Select **Sync the User with Google User Directory**.c. Click **Sync with Google User Directory**.d. Confirm that Google Status is listed as Enabled.

## Deploying Android Enterprise to Supported devices

Two configurations are required for deploying Android Enterprise:

- The Android Enterprise: Work Profile on Company Owned Device configuration enables Android Enterprise.
- A Lockdown & Kiosk configuration defines the Android Enterprise restrictions to apply.

## Retiring Registered Devices

In BYOD scenarios, moving from Device Admin to Android Enterprise Work Profile on Company Owned Device does not require a retire and re-enroll of devices. A device wipe or retire is required only for moving from Device Admin to Device Owner mode.

When you select a device enrolled in Device Owner / Enhanced Profile Owner / Company-Owned Personally Enabled modes for Retire action, a pop-up appears on the screen indicating that the "Retire command is not supported for devices which are organizationally owned."

## Deploying the device

**Procedure**

1. In the Ivanti Neurons for MDM portal, go to **Configurations**.
2. Click **Android Enterprise: Work Profile**.
3. Click **Edit**.
4. Click **Next**.
5. Select **All Devices** or **Custom**.
6. If you selected  **Custom**, search for and select the device groups that should receive the Android for Work settings.
7. Click **Done**.
8. Click **Back to list** (upper left corner).
9. Click **+Add**.
10. Click **Lockdown & Kiosk: Android Enterprise**.
11. In the **Name** field, enter text that identifies the configuration.
12. Under **Choose Lockdown Type**, select **Work Profile**.
13. Select the lockdown settings you want to apply to the target devices.
14. Click **Next**.
15. Select **All Devices** or **Custom**.
16. If you selected Custom, search for and select the device groups that should receive the Android Enterprise settings.
17. Click **Done**.

You cannot make changes to the resulting profile once it has been deployed. Instead, you need to create a new Android Enterprise configuration and deploy it.

## Confirming Deployment

You can confirm that Android Enterprise has been deployed in the following ways:

- Under **Users > Users**, find the entry for a user, and then check that the **Google Status** is **Enabled**.
- Under **Devices > Devices,** click the link for a device, and then check that status for **Android Enterprise** is **Enabled**.

**Google Status** for a user should be listed as **Enabled**. If it is not Enabled, then the user will not be able to register devices.

For enterprises that are not GSuite subscribers, managed Google Play Accounts method allows users to be enrolled with Android Enterprise. If Android Enterprise was set up as managed Google Play Accounts, then the user is not shown as **Google Status: Enabled** until after an Android Enterprise device is registered. See [**Managed Google Play Accounts**](./Managed_Google_Play_Accounts__Android_Enterprise_Accounts_.md) for more information about managed Google Play Accounts.

## Deploying Android Enterprise Apps

Any app developed for Android Enterprise may include options that you can configure through Ivanti Neurons for MDM.

**Procedure**

1. In the Ivanti Neurons for MDM portal, go to **Apps >App Catalog**.
2. Find the app in the Google Play Store.
3. Click the app entry.
4. Accept permissions on behalf of Android Enterprise users.
5. Click **Next**.
6. Select a distribution option.
7. Expand **Advanced Options & App Configuration**.
8. Use the following guidelines to complete the options:

| Setting                                      | Description                                                                                                                                                                                                                                                             |
| -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Install on Device**                        | Select this option to start installation immediately after registration. The user will be prompted to confirm installation of the app except when the device is a Samsung Knox device and the silent installation option below has been selected.                       |
| **Do not show app in end user App Catalog**  | Select this option if you do not want the user to see the app in the app catalog on the device.                                                                                                                                                                         |
| **Silently install on Samsung Knox devices** | Select this option if you do not want the user prompted to confirm installation on Samsung Knox devices.                                                                                                                                                                |
| **Set App Install Priority**                 | For Android Enterprise apps you can prioritize downloading of specific apps before other apps. For example, you can prioritize the download of Tunnel and Email apps before other non-critical apps. The following are the available priority level options:\* **High** |

:::Paragraph{listStyleType="disc" indent="2"}
Medium (selected by default)
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Low**This setting is applicable for In-House, Public, Private, and Web apps. The in-house apps are installed via the client and the public and private are installed via Google. The app priority is applied only to those apps that are installed via the same channel. |
\| **Install only when connected to Wi-Fi**     | Select this option to install the app only when the device is connected to the Wi-Fi.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
\| **Install only when charging**               | Select this option to install the app only when the charging of the device is in progress.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
\| **Install only when idle**                   | Select this option to install the app only when the device is in idle (not actively used by the user).                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
\| **Auto-launch on install**                   | Select this option to launch an app automatically after installation. This functionality is available only if the app is newly installed on the device and not for a version update.                                                                                                                                                                                                                                                                                                                                                                                               |
Click **Next**.
:::

10. Select a promotion option.
11. Click **Done**.

## Configuring Business Apps

Android Enterprise apps are available in the Business Apps section of the app catalog, including the following apps:

- [**Divide Productivity**](./Deploying_Divide_Productivity_with_Android_Enterprise.md)
- Email+
- Tunnel
- Gmail
