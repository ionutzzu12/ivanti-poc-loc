---
title: Software Updates
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:**

•iOS 10.3+ and tvOS 12.0+ supervised devices

•macOS devices

•Windows 10+ devices

Create and distribute rules for OS updates.

This section contains the following topics:

- [**Configuring software updates for iOS/tvOS devices**](./Software_Updates.md)
- [**Configuring software updates for Non-DEP and DEP macOS devices**](./Software_Updates.md)
- [**Configuring software updates for Windows devices**](./Software_Updates.md)
- [**Software Updates Enforcement using Declarative Device Management**](./Software_Updates.md)

## Configuring software updates for iOS/tvOS devices

**Procedure**

To allow iOS/tvOS devices to have OS updates sent to them if they are in supervised mode:

1. Go to **Configurations**.
2. Click **+ Add**.
3. Click **Software Updates**.
4. Click **iOS/tvOS** to view the Configuration Setup section.
5. Select the **Allow OS updates to be automatically installed on supervised devices** option.
6. Select one of the following options:\* Update to latest version
   - Update to specific version - For example, enter iOS version number as 11.3.0.
7. Select one of the following install actions:\* Default
   - Download Only
   - Install ASAP
8. Select the following time options for the updates to happen:\* Start Time
   - End Time
   - Timezone
9. Click **Next**.
10. Select the **Enable this configuration** option.
11. Select one of the following distribution options:\* All Devices
    - No Devices (default)
    - Custom
12. Click **Done**.

- When installing a specific version of OS update for iOS devices, you must select a version that is available for the device. If you select an invalid or an unavailable version, software update of the device will be ignored.
- If the device has a passcode, after MDM sends the update to the device, the device queues the update and the user is prompted to enter their passcode in order to start the installation.
- Enable `enforcedSoftwareUpdateDelay` in [**iOS Restrictions**](./iOS_Restrictions.md) to make sure the manual scan on devices for software updates will not delete the specific versions downloaded by this configuration.

## Configuring software updates for Non-DEP and DEP macOS devices

Device Enrollment profile is part of Apple Business Manager that enables customers to purchase devices in bulk and automatically enroll the devices in MDM during activation. For more information, see [**Device Enrollment**](./Device_Enrollment.md).

The following procedure helps you send OS updates to Non-DEP and DEP macOS devices.

**Procedure**

1. Go to **Configurations**.
2. Click **+ Add**.
3. Click **Software Updates**.
4. Click **macOS** to view the Configuration Setup section.
5. Select the **Enable macOS Software Updates** option.
6. Select the type of updates for the device. For each of these updates, you can also select updates that do not require restart.\* OS Updates
   - Critical Updates
   - Configuration Data Updates
   - Firmware Update
   - Non Critical UpdatesAdmin can manage(install/schedule) non critical macOS updates by enabling **Enable Non Critical Updates**. This option is disabled by default for the existing tenants and needs to be enabled by admin explicitly post upgrade if required.In **OS updates**, Administrators can update the device to a specific version of macOS.All macOS updates can be configured with actions as follows:\* Default
     - Notify Only
     - Install Later
     - Install Force Restart
     - Download Only
     - Install ASAP
   - PriorityDefault - LowPossible values - Low, High
   - Max User DeferralsPossible value - IntegerOnly supported when Install Later option is selected.
7. Select the following time options for the updates to happen:\* Start Time
   - End Time
   - Timezone
8. Click **Next**.
9. Select the **Enable this configuration** option.
10. Select one of the following distribution options:\* All Devices
    - No Devices (default)
    - Custom
11. Click **Done**.

## Configuring software updates for Windows devices

**Procedure**

To configure your Windows installation update schedule:

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Configurations**.
:::

:::WorkflowBlockItem
Click **+ Add**.
:::

:::WorkflowBlockItem
Click **Software Updates**.
:::

:::WorkflowBlockItem
Click **Windows** to view the Configuration Setup section.
:::

:::WorkflowBlockItem
Enter the following options depending on the version of your Windows devices.
:::

:::WorkflowBlockItem
Click **Next**.
:::

:::WorkflowBlockItem
Select the **Enable this configuration** option.
:::

:::WorkflowBlockItem
Select one of the following distribution options:
:::

:::WorkflowBlockItem
- All Devices
- No Devices (default)
- Custom
  Click **Done**.
:::
::::

### Software updates for Windows 10+ devices

- Update Sources - Select one of the following sources:
  - Enterprise WSUS
  - Microsoft Update and/or Enterprise WSUS
    Driver Update Source
- Feature Update Source
- Other Update Source
- Quality Update Source
- URL to Enterprise WSUS Server
- Alternate intranet Microsoft update server
- Allow Updates from 'Trusted Publishers' - Limit sources for updates to trusted publishers only.
- Auto Update Strategy - Select one of the options from the pull-down menu.
- Scheduled Installation Day - Set the frequency of updates.
- Scheduled Installation Time - Select an installation time for updates.
- Allow updates to be downloaded automatically over metered connections - Enable or disable the option.
- Do not allow update deferral policies to cause scans against Windows Update - Enable or disable the option.
- Engaged restart deadline - Select the number of days to restart deadline.
- Snooze engaged restart deadline - Select the number of days to snooze the engaged restart deadline.
- Engaged restart transition schedule - Select the number of days to restart transition schedule.
- Update/Fill empty content URLs.
- MO App download limit - Select one of the following options:\* Do not ignore MO download limit for apps and their updates
  - Ignore MO download limit (allow unlimited downloading) for apps and their updates
- MO update download limit - Select one of the following options:\* Do not ignore MO download limit for OS updates
  - Ignore MO download limit (allow unlimited downloading) for OS updates
- Manage preview builds - Select one of the following options:\* Disable Preview builds
  - Disable Preview builds once the next release is public
  - Enable Preview builds
- Auto-restart warning notification schedule for updates - Select the minutes to be taken to auto-restart warning notification.
- Restart warning reminder - Select the hours to set the restart warning reminder.
- Automatic update schedule - Select the frequency of automatic updates.
- Auto-restart notification for updates - Turn on the auto-restart notification for updates.
- Product version - Enter the product version as listed on the Windows Update version page (URL: aka.ms/WindowsTargetVersioninfo). For example, "Windows 11" or "11" or "Windows 10".
- Target release version - Enter the target release version on the Windows Update version page.
- Active Hours Start – If you enable this option, a PC will not restart automatically after updates during active hours. Outside of active hours, the PC will attempt to restart.
- Active Hours End – If you enable this option, the PC will not restart automatically after updates during active hours. Outside of active hours, a PC will attempt to restart.
- Active Hours Max Range – Enable this option to indicate the maximum number of hours from the start time that users can set their active hours.
- No Update Notifications During Active Hours – The update notification options are below.\* Default Windows Update notifications
  - Turn off all notifications, excluding restart warnings
  - Turn off all notifications, including restart warnings
- Disable Updates for Drivers – Enable this option to exclude drivers with Windows quality updates. If you disable or do not configure this option, Windows Update will include updates with a driver classification.
- Quality Updates Deadline – The number of days before quality updates are automatically installed on devices is independent of active hours.
- Quality Updates Deadline Grace Period – The minimum number of days from update installation until automatic restarts for quality updates.
- Feature Updates Deadline Grace Period – The number of days until feature updates are automatically deployed on devices, independent of active hours.
- Feature Updates Deadline Grade Period – The minimum number of days until feature updates are automatically deployed on devices, independent of active hours.
- Don’t auto-restart until end of grace period – When enabled, devices will not automatically restart outside of active hours until the deadline and grace period have passed, even if an update is ready to restart. When disabled, an automatic restart may be attempted outside of active hours if the update is available for restart prior to the deadline.

### Software updates for pre-Windows 10.0.14393 devices

The following settings will not work if Telemetry Restriction is disabled on a device:

- Pause Upgrade/Updates - Turn on to delay changes to a later date
- Defer Updates for - Choose to delay up to 4 weeks
- Defer Upgrades - Turn on to defer upgrades
- Defer Upgrades for - Choose to delay up to 8 months

### Software updates for Windows 10.0.14393+ devices

- Branch to install updates from - Allows the IT admin to set which branch a device receives their updates from. Branch to install updates from field contains the following options:
  - Windows Insider build – Fast
  - Windows Insider build – Slow
  - Release Windows Insider build
  - Semi-annual Channel (Targeted)
  - Semi-annual Channel
  - Release Preview of Quality Updates Only
  - Canary Channel
    Feature Updates (upgrades) - Supported only in Windows Professional, Windows Enterprise, and Windows Education.
  - Pause updates
  - Defer for - Choose to delay up to 180 days.
    Quality Updates (updates) - Supported only in Windows Professional, Windows Enterprise, and Windows Education.
  - Pause updates
  - Defer for - Choose to delay up to 30 days.

### Software updates for Windows 10.0.17083+ devices

- Feature Updates:
  - Feature update uninstall period - Select the number of days to be taken to uninstall a feature update.

### Software updates for Windows 10.0.17763+ devices

- Disable "Pause Updates" access by users
- Disable UXWU Access by users (Windows Update Scan, download and install)
- Update notification level - Select one of the following options:\* Use the default Windows Update notifications
  - Turn off all notifications, excluding restart warnings
  - Turn off all notifications, including restart warnings
- Feature updates:\* Deadline before auto-restart for update installation - Select the number of days for the deadline before auto-restart for update installation.
  - Engaged restart deadline - Select the number of days for the engaged restart deadline.
  - Snooze engaged restart deadline - Select the number of days to snooze the engaged restart deadline.
  - Engaged restart transition schedule - Select the number of days to restart transition schedule.

## Software Updates Enforcement using DDM

The administrator can enforce Software Updates installation on iOS, macOS, and iPadOS devices using DDM.

Supported on:

- iOS 17+
- iPadOS 17+
- macOS 14+

**Procedure**

1. Create a **Software Update Enforcement** configuration from the Configurations section.
2. Perform a Force Check-in to ensure the Software Update Enforcement configuration is installed on the device.

When you open the device, you should see a notification about the required software updates with details like the version number, required by date, etc.

If you do not want to enforce the software update, you need to set the configuration distribution option to **None**.

### Distributing predicates for a Software Update Enforcement configuration

1. Create a Software Update Enforcement configuration.
2. Set the toggle switch “Activation with Predicates” to ON, and use + button to include the predicates (as needed).

::Image[]{src="Resources/Images/predicates.png" signedSrc="Resources/Images/predicates.png" size="66" caption alt isUploading="false" sha initialPath="Resources/Images/predicates.png" githubPath="Resources/Images/predicates.png" position="flex-start"}

To edit or delete a predicate, go to **Admin** > **Apple** > **Predicates**. You can find the list of predicates available in this page. Click **Edit** to make any changes to the existing predicate and save it. Similarly, to delete an existing predicate, select the predicate and click **Delete**.

You cannot delete a predicate if it is associated with any configuration.
