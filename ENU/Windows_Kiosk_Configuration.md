---
title: Windows Kiosk Configuration
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

Using Windows Kiosk configuration, you can configure single or multiple-app kiosk on Windows 10 devices. By applying this configuration, the kiosk users are restricted from accessing any features outside the kiosk apps. This configuration requires Windows Bridge to be enabled.The following are 3 modes in which the configuration can be applied.

- Single Application
- Multiple Applications (fetch list of application from Windows device)
- Multiple Applications (select an existing layout from Start Menu configuration)

Applications used for a Windows Kiosk configuration should be already present on a device before entering into a configured Windows Kiosk mode.

To configure Windows Kiosk configuration:

1. Go to **Configuration**&#xNAN;**> +Add**.
2. Select **Windows Kiosk** configuration.
3. Enter a name for the configuration.
4. Enter a description.
5. In the Configuration Setup section, specify the remaining settings as described in the following table.|                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
   \| ----------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Setting**                                                                         | **What To Do**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
   \| **Select Kiosk mode**: Select any of the following 3 options.                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
   \| **Single Application**                                                              | Select this option to configure single application kiosk mode for a device.1) In the **Select Windows Device (optional)** section, choose a Windows 10 device. Click **Fetch Apps from Device** to fetch the list of apps from a device.The device you select should be under your supervision and requires a check-in to successfully fetch app data.To skip these steps, select the **Skip this step. You can change your mind later if desired** checkbox.
   2\) Click **Add From Fetched App List** to add apps from the fetched list.
   3\) Select a single app by clicking the radio button in the **Name** column of the app. Click **Add New** to add a new app to the list. To delete an app from the list, click on the Delete icon.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
   \| **Multiple Applications (Fetch list of Applications from Windows device)**          | Select this option to configure multiple applications kiosk mode for a device.1) In the **Select Windows Device (optional)** section, choose a Windows 10 device. Click **Fetch Apps from Device** to fetch the list of apps from a device. The device you select should be under your supervision and requires a check-in to successfully fetch app data.To skip these steps, select the **Skip this step. You can change your mind later if desired** checkbox.
   2\) In the **Kiosk Apps and Start Menu Layout**, click **Add From Fetched App List**. The **Select Kiosk App** window is displayed. Select the app(s)from the fetched list and click **Use Selected App**.
   3\) In the Additional Allows Apps section, click **Add From Fetched App List**. The **Select Kiosk App** window is displayed. Select the app(s)from the fetched list and click **Use Selected App**.Additional allowed apps are the apps that are considered as dependencies for the selected apps in the **Kiosk Apps and Start Menu Layout**.Without 'allowed apps', the OS does not allow to run this application even when the application icon is displayed in Start Menu.
   4\) Click **Add New** to add a new app to the list.To delete an app from the list, click on the Delete icon. You can drag and move an app in the list to any position in the list.
   5\) In the **Multiple App Other settings**, select the required options:\* **Hide Power Button**
   - **Hide User Tile**
   - **Hide Taskbar**In Microsoft Windows 11, the multi app kiosk mode option "**Hide Taskbar**" is not supported. |
     \| **Multiple Applications (Select an existing layout from Start Menu Configuration)** | If you have created a Start menu layout configuration, you can import the configuration and use it to configure the multiple-application mode by selecting this option.1) In the **Select Layout** section, Select a layout that has been previously setup as a Start Menu Configuration. Previously created configurations with applicable layout parameters are displayed in the drop-down list below.

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
In the Multiple App Other settings, select the required options:\* **Hide Power Button**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Hide User Tile**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Hide Taskbar**In Microsoft Windows 11, the multi app kiosk mode option "**Hide Taskbar**" is not supported.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
:::

6. Click **Next**.
7. Select one of the following distribution options:\* All Devices
   - No Devices(default)
   - Custom
8. Click **Done**.For the configuration to take complete effect, the device should be rebooted after applying or updating a Windows Kiosk configuration.Depending on applications for multi-app kiosk configuration, it is required to reboot a device the second time. Some icons may be missed on the first login, but the missing icons will be displayed on login after the second reboot.

Device has to be rebooted after applying, deleting or updating a Kiosk configuration. It can be done with Restart/Shutdown device command from the device action menu. Without reboot:

- Device is not entered into Kiosk mode automatically after applying a Kiosk configuration.
- Device does not exit from Kiosk mode automatically after deleting an applied Kiosk configuration.
- Device does not change the running Kiosk configuration.

If a device with an applied kiosk configuration receives an updated configuration, Windows OS on the device removes an existing kiosk user and recreates a new one kiosk user with a new kiosk configuration. The session for the current user should be ended explicitly with reboot of the device.

It is preferable to configure with '.lnk' files for a multi-app kiosk configuration and '.exe' for a single-app kiosk configuration. An imported Start Menu configuration from a device uses the '.lnk' format. Start Menu items created manually for '.exe' applications sometime could be not displayed in Start Menu of multi-app kiosk configuring depending on '.exe' application.

For example, Windows Media Player can be added to Start Menu using one of the following '.lnk' files:

- %ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Accessories\Windows Media Player.lnk
- %ALLUSERSPROFILE%\Microsoft\\\Windows\Start Menu\Programs\Windows Media Player.lnk

If this app is added directly with any of the following '.exe' file, a corresponding icon will not be displayed, even the first '.exe' path is used internally in the above '.lnk' files:

- C:\Program Files (x86)\Windows Media Player\wmplayer.exe
- %ProgramFiles(x86)%\Windows Media Player\wmplayer.exe
- C:\Program Files\Windows Media Player\wmplayer.exe

For single-app kiosk configuration, you can add arguments to exe file. E.g. '%ProgramFiles%\Internet Explorer\iexplore.exe -k [**www.bing.com**](http://www.bing.com)'. However, the icon for exe app with arguments are not displayed in the Start Menu in case of multi-app configuration.if you need an exe app with arguments in multi-app kiosk configuring, use '.lnk' file which can have arguments internally. '.lnk' does not work in case of a single-app kiosk configuration.

## Dependencies in multi-app kiosk mode

Win32/64 applications could require dependencies added to Additional Allowed Apps' section in case of multi-app kiosk mode. 'Additional Allowed Apps' are not required for a single-app kiosk mode.

**Example 1**: For Windows Media Player app, the following dependencies are required in multi-app kiosk mode:

- C:\Program Files (x86)\Windows Media Player\wmplayer.exe
- %ProgramFiles(x86)%\Windows Media Player\setup\_wm.exe

The first dependency is the app binaries called from corresponding ".lnk" file. The second one is one-time wizard called from the first dependency.

Without 'Allowed Apps', OS does not allow to run this application even when the application icon is displayed in Start Menu.

**Example 2**: For Internet Explorer, its icon is displayed in Start Menu if it is configured with any item from the following list:

- %APPDATA%\Microsoft\Windows\Start Menu\Programs\Accessories\Internet Explorer.lnk
- %USERPROFILE%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Accessories\Internet Explorer.lnk
- C:\Program Files\internet explorer\iexplore.exe
- %ProgramFiles%\Internet Explorer\iexplore.exe

Internet Explorer requires the following dependencies:

- C:\Program Files (x86)\Internet Explorer\iexplore.exe
- C:\Program Files (x86)\Internet Explorer\ExtExport.exe
- C:\Program Files (x86)\Internet Explorer\ieinstal.exe
- C:\Program Files (x86)\Internet Explorer\ielowutil.exe

The first dependency is app binaries required for '.lnk' item only, the other dependencies for one-time wizard. Without the first dependency, OS blocks the app with the popup. Without other dependencies, the application is closed just after startup without any additional notifications from OS.
