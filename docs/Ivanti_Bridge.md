---
title: Ivanti Bridge
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Bridge supported file types**](./Ivanti_Bridge.md)
- [**Bridge setup**](./Ivanti_Bridge.md)
- [**Bridge Logs**](./Ivanti_Bridge.md)
- [**Bridge Last Check-in**](./Ivanti_Bridge.md)
- [**Bridge Service Failure Recovery**](./Ivanti_Bridge.md)

Ivanti Bridge unifies mobile and desktop operations for Windows 10 using a single console and communications channel. It extends UEM capabilities to managing PCs and allows organizations to take advantage of [**significantly reduced costs**](https://www.mobileiron.com/en/solutions/windows/pc-management-tco) and increased efficiency while ensuring consistent security across PCs and mobile. By using Ivanti Bridge, enterprises have the ability to use a single protocol for Windows 10 Desktop devices as they do for supported Windows mobile devices, to send information to the legacy applications on the OS.

Ivanti Bridge allows IT to modernize Windows operations on UEM without giving up critical functionality. IT can apply policies and scripts already in place without requiring a systems image, domain join, or multiple channels of communication to the device.

With Ivanti Bridge, organizations can now:

- Have complete control over PCs with UEM
- Manage PCs remotely, over-the-air
- Reduce the need for imaging desktops
- Leverage GPO-based commands with PowerShell scripts deployed by UEM
- Easily edit and manage Registry
- Effortlessly deploy non-MSI wrapped Win32 apps and Win32 Store apps
- Gain File System visibility

Ivanti Bridge is supported on Windows 11+ devices and ARM processors. Ivanti Bridge does not support Windows 10 Home desktop devices.

## Bridge supported file types

Ivanti Bridge includes support for the following file types:

- PowerShellPowerShell scripts pushed to devices using Bridge support named arguments.64-bit PowerShell scripts are supported on 64-bit Windows 10 desktop devices.
- The Bridge timeout on the server-side for expecting a result after sending a PowerShell script to device is about 20 minutes. The timeout is logged as a Failure. However, the script on the device continues to work.
  The Bridge timeout on the device-side for expecting the process of a PowerShell script execution is about 60 minutes. After 60 minutes, the process will be killed, no output from the script is saved, and a new Failure is sent to the server.
  The server-side and device-side timeouts are logged as Failures. If the second timeout passes and the script generates some output, no output is logged on the server-side.
  Registry
- VB Scripts
- .EXE for Win32 application deployment
- Win32 Store apps uses WinGet tool for installing and uninstalling the apps.

If admins need to push Win32 (.EXE) files to a device (for example, as a Windows in-house app), the Bridge functionality will be automatically used if available. It is mandatory to enter an argument to silently run the file (for example, /SILENT or /VERYSILENT).The .EXE apps are installed through Bridge using the Admin PowerShell mode. For Windows devices, to install using user's credentials select 'Run as User' option.

The admins should select the **Installer run as user** checkbox in **App Installer - Settings** to install the apps for a user. Do not select the check box if you want the apps to install at the system level.

Using Ivanti Bridge, the device can be augmented in following key areas.

- **Registry:** Reading, writing, and updating registry values.
- **Files:** Verifying, reading, and updating contents of a file.
- **Application Deployment:** Adding the ability to install .EXE-based applications to the desktop device. These applications can either reside on the Ivanti Neurons for MDM servers or on a Content Delivery Network (CDN) in the Cloud.

## Bridge setup

Setting up Ivanti Bridge requires that admins complete the following steps in the following order:

1. [**Activating Bridge licenses**](./Ivanti_Bridge.md)
2. [**Installing the Bridge application**](./Ivanti_Bridge.md)
3. [**Uploading scripts to the devices**](./Ivanti_Bridge.md) for permanent or one time use to the devices

### Activating Bridge licenses

Ivanti Bridge is part of the legacy Gold package and the current Secure UEM package.

### Installing the Bridge application

After activating the Ivanti Bridge licenses, the Bridge mobile application can be installed as follows:

1. Go to **Apps > App Catalog**.
2. Click **+Add**.
3. Click **Ivanti Bridge** in the Business Apps section.
4. Add details, customize, and distribute the Bridge mobile application to the required devices as per the procured licenses.If you have enabled the **Silently install on Windows devices** option, Bridge mobile application will be silently installed and the Bridge service will start running on the devices.

Bridge app is added to the app catalog by default, and also distributed by default to all devices.

After importing the latest version of the Ivanti Bridge (2.1.419.0) into the tenant's catalog, the admin can view the newly aligned version of the app.

### Uploading scripts to the devices

Administrators can upload scripts to the devices for permanent use by creating a new Bridge configuration:

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Configuration > +Add**.
:::

:::WorkflowBlockItem
Select the **Ivanti Bridge** configuration.
:::

:::WorkflowBlockItem
Enter a name for the configuration.
:::

:::WorkflowBlockItem
Enter a description.
:::

:::WorkflowBlockItem
In the Configuration Setup section, specify the remaining settings as described in the table under step 7.
:::

:::WorkflowBlockItem
1. Enter the **Script File** category settings to specify an installation script to be pushed or executed on the devices.
2. (Optional) Enter the **Undo\*\*\*\*Script File** category settings to specify an uninstallation script to be pushed or executed on the devices. This is useful in scenarios such as device retirement or configuration deletion.
3. (Optional) Select the option **Configure Outlook** to configure Microsoft Outlook to a device using Bridge.Only supported on Outlook 2010 and 2013.
   Click **Next**.
:::

:::WorkflowBlockItem
Select a distribution for this configuration.A force check-in will be done automatically for these device actions.
:::
::::

| Category    | Setting                            | What To Do                                                                                                                                                     |
| ----------- | ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|             | Name                               | Enter a name that identifies this configuration.                                                                                                               |
|             | Description                        | Enter a description that clarifies the purpose of this configuration.                                                                                          |
| Script File | All Versions (Windows 10+ Desktop) |                                                                                                                                                                |
|             | Script File                        | Select a valid script or executable file (.ps1, .reg, .exe).\* The specified script file or executable file (.ps1, .reg, .exe) will be automatically executed. |

- Other file types will only be copied to the target folder. |
  \|                  | Script Arguments                   | Specify the list of arguments for the script file.\* For Win32 (.exe) files, enter an argument to silently run the file (for example, /SILENT or /VERYSILENT). This is mandatory.                                           |
  \|                  | Target Folder                      | Specify the target folder for the script file.\* If the target folder is not specified, then the value of the %TEMP% system environment variable is used as the target folder.                                              |
  \| Undo Script File | All Versions (Windows 10+ Desktop) |                                                                                                                                                                                                                            |
  \|                  | Script File                        | Select a valid script or executable file (.ps1, .reg, .exe).\* The specified script file or executable file (.ps1, .reg, .exe) will be automatically executed.
- Other file types will only be copied to the target folder. |
  \|                  | Script Arguments                   | Specify the list of arguments for the script file.\* For Win32 (.exe) files, enter an argument to silently run the file (for example, /SILENT or /VERYSILENT). This is mandatory.                                           |
  \|                  | Target Folder                      | Specify the target folder for the script file.\* If the target folder is not specified, then the value of the %TEMP% system environment variable is used by default.                                                        |

### Uploading scripts to the devices for one-time use

Administrators can upload a script to the devices for one-time (ad hoc) use.

1. Go to **Devices > Devices**.
2. Click the device name link to go to the Device details page. This is a Windows 10 desktop device to which the one-time script will be pushed/executed.
3. Click the

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
icon and click **Script and Actions via Ivanti Bridge**.
:::

4. Enter a name.
5. In the Script File section, specify a script to be pushed/executed on the device as described in the preceding table.
6. Click **Apply**.The script execution will be queued and may take a while to complete. Go to the Logs tab to check and view the status (output or failure messages). A force check-in will be done automatically for these device actions.

## Bridge Logs

This feature allows you to pull Ivanti Bridge logs for individual devices for troubleshooting and diagnosing applications. The logs are sent at the next device check-in. You can wait for the next scheduled sync or perform a forced device check-in to get the logs quickly.

To pull logs from a device:

1. Go to **Devices > Devices**.
2. Click the device name link to go to the Device details page. This is a Windows 10 desktop device to which the one-time script will be pushed/executed.
3. Click the

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
icon and click **Pull Ivanti Bridge Log**. The **Pull Ivanti Bridge Log** window is displayed.
:::

4. Select one of the following options:**Single log** - requests Ivanti Neurons for MDM to pull the most recent Bridge log on the device.**All logs** - requests Ivanti Neurons for MDM to pull all log (up to 30 days) on the device.
5. Click **Pull Log**. After a device has sent it to Ivanti Neurons for MDM, you can view the Bridge log from the Logs tab in the Device details page.Only logs sent using **All logs** option can be downloaded as zip file only.

## Bridge Last Check-in

The Bridge Last Check-in column lists the Bridge service's last check-in date and time on the Devices page. The column can be added to the Devices page using the Customize Columns option and it is not visible by default.

To make this column visible, select **Devices** > **Customize columns** > select **Bridge Check-in**.

The exported data will also have the Bridge Last Check-in details wherever applicable.

## Bridge Service Failure Recovery

The Bridge Service Failure Recovery has been introduced in Bridge 2.1.14 version. By default, this version gets imported into the App Catalog for all the users. In some rare cases, the Bridge Service may fail without any known reason. In such cases, the support is available in Bridge 2.1.14 and later versions.
