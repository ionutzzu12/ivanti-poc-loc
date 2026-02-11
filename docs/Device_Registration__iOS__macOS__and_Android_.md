---
title: Device Registration (iOS, macOS, and Android)
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Installing the management profile manually**](./Device_Registration__iOS__macOS__and_Android_.md)
- [**Sending an invitation (iOS, macOS, and Android)**](./Device_Registration__iOS__macOS__and_Android_.md)
- [**Instructing end users to download the app (iOS and Android)**](./Device_Registration__iOS__macOS__and_Android_.md)

Most users start by registering a device. You can use any of the following approaches to start the registration process:

- Send an invitation to one or more end users (iReg registration)
- Instruct end users to download the Go (in-app registration)

If iOS and macOS device MDM enrollment fails with the *Profile Installation Failed The SCEP server returned an invalid response*. error, the device user must re-initiate the device enrollment process from the beginning. This happens mostly when the device user takes longer time than expected to complete the iOS and macOS device MDM enrollment process after the profile is downloaded on the device. Please contact Ivanti support for further clarifications.

Ivanti Neurons for MDM supports the user-level management of a single user (local user or registered Active Directory (AD) user) on macOS devices. Administrators can manage devices for the users, apply device profiles and user profiles, and consequentially use App Store, app distribution, configurations, and policies (including Apps\@Work, restrictions, security).

To manage macOS devices with AD user, the AD user needs to be the user that is logged in during registration. Any other non-registered user cannot view the registered-user specific profiles (for example, identity certifications, VPN). However, device-level configurations can be viewed and used by any logged-in user.

The end [**user must have an account**](./Users.md) in Ivanti Neurons for MDM before you can start the device registration process. For LDAP users, that means a [**Connector**](./Connector.md) and an [**LDAP server**](./Configuring_LDAP_server.md) must be set up, and the user must be imported from the LDAP server. For local users, that means [**adding a user**](./Users.md).

The device enrollment URL generated in earlier versions of Ivanti Neurons for MDM will cease to work with the current version. The administrator will need to regenerate the device enrollment URL for device registration.

## Installing the management profile manually

**Applicable to:**

- iOS 12.2 through the most recently released version as supported by Ivanti Neurons for MDM.
- macOS 11.0 through the most recently released version as supported by Ivanti Neurons for MDM.

### iOS Device Registration

During in-app registration on iOS devices:

- During device registration using Go app a page with instructions to install the profile appears.
- Click the **Install Downloaded Profile** option and click Click **I Understand**.
- The downloaded profile is valid for a few minutes, after which re-registration is required.

### macOS Device Registration

For macOS device registration in the self-service portal, a user must perform the following steps:

**Procedure**

1. Log in with their credentials.
2. In the Install Management Profile page, the profile is downloaded to the user's local system.
3. Double-click the downloaded profile to make it visible in the user's System Preferences.There is limited time for the user to install the profile before it becomes invalid.
4. Open **Profiles** in System Preferences. When the profile is downloaded to the device, users can view a web page having the Profiles link. Click **Profiles** to open the Settings app.
5. Click **Install** to install the management profile.
6. Continue and finish the installation procedure. Enter the system password when prompted.

## Sending an invitation (iOS, macOS, and Android)

Start the registration process by sending an invitation. Ivanti Neurons for MDM provides the following ways to send end users an invitation to register a device:

- In the [**Startup Wizard**](./Getting_Started.md)
- When you [**add one or more users**](./Users.md)
- In the Users page ([**Actions > Send Invite**](./Inviting_Users.md))

If the end users misplace the invite, you can share the URL that was listed in the invitation. Ensure that you add **/go** at the end of the URL.

End users who have an Ivanti Neurons for MDM account with a password do not need an invitation to start the registration process. You can send them the URL that is listed in the invitation.

## Instructing end users to download the app (iOS and Android)

The Go application is available for Android and iOS devices. You can provide instructions to the end users on how to download the application from a public app store and start the registration process from the app. The email invitation contains the following information:

- A link to the registration page
- A one-time use PIN (if set by the administrator)
- Basic instructions for the next steps

If you have already set a password for the account, you can send the password to the corporate email address of the end user. If you are using LDAP for authentication, inform the end user that network credentials are required.

If the user does not complete installation of the MDM profile during registration, then Ivanti Neurons for MDM periodically sends push notifications to the device to prompt the user to complete the registration process.

The user can use either Username and Password or scan the QR code to begin the device registration from Go app. The details are as follows:

- **Username**: Email address
- **Password**: If specified in the [**User Settings**](./User_Settings.md) and a temporary password is defined by the administrator
- **QR Code**: Generate the QR code from the Ivanti Neurons for MDM self-service portal. When you scan the QR code using the **Scan QR Code** option, a prompt appears on the screen requesting you to grant permission to access the camera on the device. After you grant permission, the camera scans the QR code and the device is registered. This option is supported for Android 9 and later, iOS 14 and later versions.

As an end user, if you receive a registration email on your mobile device, tap the link to start the registration process. If you receive the email on a laptop or desktop, enter the URL in a browser on your mobile device to begin the registration process.  

If you do not yet have a password defined for your Ivanti Neurons for MDM user account or if your [**User Settings**](./User_Settings.md) require a registration PIN, a one-time use PIN is included . After you enter the PIN, you are prompted to set a password for the account if the password does not exist.

For Android Enterprise devices, when the registration is complete, any manually installed CA certificates to a work profile on company owned device or a work managed device are uninstalled.

### Re-enrolling iOS devices

If you want to re-enroll your device you can do so as follows:

1. Launch the Go client on your device.
2. Go to **Settings** > **Troubleshoot** > **Re-enrol Device**. The re-enrollment process starts and displays a few prompts for confirmation.
3. Tap **Yes** on the prompts.

If you tap **Cancel** during the profile installation, the enrollment process stops and the Ivanti Neurons for MDM server disables the device MDM.

To restart the re-enrolment process you must re-install the already downloaded profile. The downloaded profile is valid only for a few minutes after that you must perform the re-enrollment from Go client.

**Re-registering Android devices**

The admin can re-register a device by using the retire, wipe, or delete operations without manually clearing the existing active entry. This method is specifically more helpful for re-registrations where the new entry and existing entry belong to the same tenant. The Devices page displays the status of the device on the Ivanti Neurons for MDM administrative portal as follows:

- **Active** - device registration is successful
- **Retired** - device gets reset and retired status will be shown
- **Wiped** - device gets reset and wiped status will be shown
- **Reset** - device gets reset and will be in active status on the server until next registration

The Audit Trails page lists the device registration, re-registration, and retired statuses for Android devices. For more information, see [**Working with Widgets**](./Working_with_Widgets.md).

For Android 9.x and earlier versions, a single entry will be shown after re-registration. In case of Android 10.x and later versions, multiple entries will be displayed. However, only the latest entry will be active and older entries will be in a retired state.
