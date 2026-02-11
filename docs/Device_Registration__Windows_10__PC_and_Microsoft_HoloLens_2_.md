---
title: Device Registration (Windows 10+ PC and Microsoft HoloLens 2)
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Manual registration**](./Device_Registration__Windows_10__PC_and_Microsoft_HoloLens_2_.md)\* [**Sending an invitation**](./Device_Registration__Windows_10__PC_and_Microsoft_HoloLens_2_.md)
  - [**Completing the end users registration process**](./Device_Registration__Windows_10__PC_and_Microsoft_HoloLens_2_.md)
- [**Windows Autopilot**](./Device_Registration__Windows_10__PC_and_Microsoft_HoloLens_2_.md)
- [**Entra ID Standard Registration**](./Device_Registration__Windows_10__PC_and_Microsoft_HoloLens_2_.md)

Device registration process are of the following types:

- Manual registration\* Invitation
  - End User registration
- Windows Autopilot
- With SCCM and Ivanti EPM via a Provisioning Package Enrollment with PIN. See [**Provisioning Package Enrollment with PIN**](./Provisioning_Package_Enrollment_with_PIN.md).
- [**Bulk Enrollment**](./Using_Bulk_Enrollment_for_Windows_devices.md)

## Manual registration

Most users start by registering a device. You can use any of the following approaches to start the registration process:

- Email invitation
- Direct users to the URL for your implementation
- The end [**user must have an account**](./Users.md) in Ivanti Neurons for MDM before you can start the device registration process. For LDAP users, that means a [**Connector**](./Connector.md) and an [**LDAP server**](./Configuring_LDAP_server.md) must be set up, and the user must be imported from the LDAP server. For local users, that means [**adding a user**](./Users.md).
- The device enrollment URL generated in earlier versions of Ivanti Neurons for MDM will cease to work with the current version. The administrator will need to regenerate the device enrollment URL for device registration.

## Sending an invitation

In most cases, you will start the registration process by sending an invitation. Ivanti Neurons for MDM provides the following ways to send end users an invitation to register a device:

- in the [**Startup Wizard**](./Getting_Started.md)
- when you [**add one or more users**](./Users.md)
- in the Users page ([**Actions > Send Invite**](./Inviting_Users.md))

If end users misplace the invite, receive it on a desktop or laptop, or fail to receive it for some reason, you can send them to the URL that was listed in the invitation. Just add **\go** to the end of your service URL.

End users who have an Ivanti Neurons for MDM account with a password set do not need an invitation to start the registration process. You can send them to the URL that would have been listed in an invitation.

## Completing the end users registration process

Tell your device users how to complete the registration process. You can use the following instructions as a template and make any necessary changes:

**Procedure**

1. Open a browser on your Windows 10+ PC.
2. Navigate to mobileiron.com/go.You are redirected to a new page containing an enrollment URL.
3. Copy the enrollment URL to the clipboard.
4. Tap **add account** at the bottom of the **Settings** page.
5. Enter the email address associated with the invitation you received.
6. If the user's Ivanti Neurons for MDM username does not match user's email address as entered in Ivanti Neurons for MDM, tell the user to enter the username when prompted for the email address.
   Paste the Workplace server URL you copied into the next text field.
7. Tap **sign in**.
8. Enter your password in the next field.
9. Leave the other fields blank.
10. Tap **sign in**.
11. Click **done** in the **ACCOUNT ADDED** screen.The Workplace start screen shows that an account has been added.

## Windows Autopilot

Windows Autopilot is a Microsoft feature that helps administrators to setup and pre-configure new devices to make them business ready. The Autopilot feature helps with a quick, reliable, and seamless provisioning of Windows Desktop or HoloLens 2 devices. In addition, the Autopilot feature helps perform the following tasks: 

- Automatically join devices to Entra ID (Entra ID)
- Auto-enroll devices into MDM services
- Create and auto-assign devices to configuration groups based on the profile of the device
- Customize the enrollment experience
- Apply configurations and policies
- Install essential applications

Ivanti supports all modes of Autopilot profiles: 

- User Driven
- User Driven Pre-provisioned (former White Glove)
- Self-Deploying mode

For more information, see [**Configuring Windows Autopilot Profiles**](./Configuring_Windows_Autopilot_Profiles.md).

For security and unauthorized use of the device, all Autopilot Windows devices can be locked to a tenant using the TenantLockdown CSP feature. To use this feature, the devices must be enrolled using the Autopilot option. This configuration is applied at the device level. See [**TenantLockdown CSP**](./TenantLockdown_CSP.md).

## Entra ID Standard Registration

When users are added to the Entra ID tenant, they can directly enroll their devices via the Work Account.

**Procedure**

1. On a Windows device, go to **Settings > Accounts > Access work or school**.
2. Select Add Work or School account and then click **Connect**.
3. Provide email address from your work account.

The device gets automatically enrolled to Ivanti Neurons for MDM.
