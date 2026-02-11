---
title: Help@Work
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

**License:** Platinum

**Supported on:** Android and iOS devices as supported by Ivanti Neurons for MDM

Use Help\@Work for Android/iOS to provide remote assistance to users of Android and iOS devices. Help\@Work for Android/iOS is based on the TeamViewer QuickSupport app. You will need a TeamViewer account to use Help\@Work for Android/iOS. If you do not have an account, visit teamviewer.com for details.

Help\@Work transforms the help desk experience for iOS 11.0+ and Android devices by allowing users to ask for help with a click of a button and to share their screen with a help desk agent. Users no longer waste valuable time trying to verbalize the issue, and IT staff is more efficient when troubleshooting device issues. This is not supported for MAM-only iOS devices.

TeamViewer is supported on Android Device Owner devices in Kiosk mode.

TeamViewer launch commands ceases to exist if the app exits or the device reboots.

In Android devices, if the Teamviewer QuickSupport app is not installed, the user is prompted to download the app. In iOS devices, the app has to be pushed through App Catalog or if it is already installed on device, it must be converted as a managed app.

The Teamviewer QuickSupport app should be in foreground for the session to be applied to the application. The TeamViewer host app is required for Unattended mode.

The desktop application version that admin installs should be compatible with the Quicksupport version installed in the client device to support remote sessions.

## Setting up Help\@Work for Android or iOS

The following are one-time setup steps for branding and distributing Help\@Work for Android or iOS:

1. Go to the **Admin** tab.
2. Under Infrastructure, click **Help\@Work**.
3. **Help\@Work** requires TeamViewer. In the Activate TeamViewer section, activate either **TeamViewer Attended** or **TeamViewer Unattended (Android only)** option by clicking the **Activate Now** button.
4. Review the TeamViewer license agreement and click **Agree** to continue. Your Enterprise License is now activated. This identifies Ivanti customers to TeamViewer so that access is granted.
5. The **Remove Activation** option becomes available upon activating the TeamViewer. When you click **Remove Activation** present under the **Activate TeamViewer** section, the **Confirm Remove Activation** window appears on the screen. Click **Remove Activation** to remove the TeamViewer Activation, which in turn will remove the Help\@Work functionality on all supported devices. However, you can activate TeamViewer using an existing account or a different account at a later stage.
   If you want to delete the **TeamViewer** account in Unattended mode, you must de-provision the associated devices for which the Unattended mode is enabled. To de-provision the associated devices, you must undistribute the **TeamViewer** app from the associated devices and do a force check-in. Ensure the TeamViewer app is deleted from all devices and then delete the binding of the account from the Admin console.
   Distribute the TeamViewer app to users you wish to start remote sessions using the standard app distribution workflow. This is specific to **Attended** and **Unattended** modes. If the admin wants to control the device, the Universal add-on or OEM/model-specific add-on by TeamViewer needs to be distributed to the device as well. See [**App Configuration**](./App_Configuration.md) for instructions.

## Starting a remote session using Help\@Work for Android or iOS

A typical Help\@Work for Androidor iOS session starts with an end-user needing help.

To start a Help\@Work session with the user's device:

::::WorkflowBlock
:::WorkflowBlockItem
In Ivanti Neurons for MDM, go to **Devices**.
:::

:::WorkflowBlockItem
In the device list page, click on the device that needs support.
:::

:::WorkflowBlockItem
From the Actions menu, click **Start TeamViewer Remote Control** for Android devices or **Remote Display** for iOS devices. You will see two options:
:::

:::WorkflowBlockItem
- Attended mode (default) - This option requires **TeamViewer Quick Support** app to be installed and Whitelisted in the target device.
- Unattended mode (available on Android only) - This option requires **TeamViewer Host** app to be installed and Whitelisted in the target device.
  If you want to Whitelist the hostnames or override the content security policy, please contact the support team.

The Unattended mode option works on Kiosk mode as well. It should be enabled from the TeamViewer integration page. The Unattended remote control requires TeamViewer host app on device, one time activation on a device, and a MI add-on license. For the one time activation, the permission prompt will be displayed when the TeamViewer host app installed and launched for the very first time. The administrator can use the "Auto-launch (settings in Managed App configuration)" TeamViewer app after installation if desired. The number of licenses is calculated based on TeamViewer host app distribution. If the TeamViewer host app is distributed to a device, one Unattended remote host session license is consumed. In addition to the TeamViewer host app, other add-on apps may be needed and should be allowed in kiosk or shared kiosk mode. Other add-ons might be needed depending on the device model and manufacturer.

The Google Pixel devices do not persist this permission grant and require consent for permission for every session.

If the administrator has a valid TeamViewer token, the desktop client starts with a support session to the device. Otherwise, the administrator will be required to log in with TeamViewer and grant permissions.
:::
::::

To quickly initiate a remove session, administrators can login to the desktop application beforehand.

## Installing TeamViewer

Install the TeamViewer app on the desktop to access and provide support for your users' remote devices. To install TeamViewer:

1. Download the installation package for the TeamViewer full version for Mac, Windows, or Android from here:[**https://www.teamviewer.com/en/download/**](https://www.teamviewer.com/en/download/)
2. Launch the TeamViewer installation program.
3. Select **Basic Installation**.
4. Select **Company / Commercial use**.
5. Click **Accept - finish**.

## Requesting a TeamViewer account

You must have a TeamViewer account to provide support using TeamViewer. To obtain a TeamViewer account:

1. Go to [**https://login.teamviewer.com/**](https://login.teamviewer.com/LogOn#register).
2. Enter your email, name, and password.
3. Click **Sign Up**.
4. Use the email account you entered in step 2 to receive an TeamViewer account activation email.
5. Complete the instructions in the email to activate your TeamViewer account.

## Confirming TeamViewer session ID

TeamViewer generates a session ID when connection is established between the administrator's computer and the user's mobile device.

1. When the session ID is generated, Ivanti Neurons for MDM passes it to the TeamViewer QuickSupport app using the managed app configuration, which in turn uses this session ID to invoke the TeamViewer client on the device. For iOS, the session ID expires after 30 minutes.
2. The user is prompted to accept the TeamViewer EULA.
