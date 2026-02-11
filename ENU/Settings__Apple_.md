---
title: Settings (Apple)
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Administrators can configure, enable, disable various settings for Apple devices.

## Silent registration (for macOS only)

Silent registration for macOS devices is locked as Enabled. This applies to all new device registrations in the tenant and is supported by Mobile\@Work 1.4 and or supported newer versions.

## Profile settings

Administrators can enable or disable sending emails to the end-users and notifications to the macOS and Go for iOS clients if the MDM profile is not installed. The MDM profile notifications feature is enabled by default.

Procedure

1. Go to **Admin > Settings**.
2. Select or deselect the **Send email to user and notification to client if MDM profile is not installed** option.
3. Select the maximum number of emails/notifications between 1 to 4.
4. Click **Save**.

## OS updates for automated device enrollment (iOS only)

Administrators can turn on iOS operating system updates for automated device enrollment. If this option is enabled, then the Device Enrollment devices will use the [**Software Updates**](./Software_Updates.md) configuration instead of the schedule OS update setting in the Device Enrollment Profile.

This option is disabled by default, in which case the schedule OS update setting in the Device Enrollment Profile is used. Turning on this setting is permanent and cannot be turned off. This setting will remove the schedule OS update setting in all the available Device Enrollment profiles.

Supervised non-Device Enrollment devices use the Software Updates configuration.

Procedure

1. Go to **Admin > Settings**.
2. Select or deselect the **Use Software Update Configuration for Automated Device Enrollment** option.
3. Click **Yes** to confirm.
4. Click **Save**.

## Multi-user Secure Sign-In

The administrators can clear the device password when the user logs out from the Multi-user Secure Sign web clip on iOS shared devices by selecting the "**Clear passcode after User logout**" option in the "**Multi User secure sign-in**" section under Admin > Apple > Settings

## Priority Settings for Restrictions Configuration

The administrator can enable priority for multiple iOS and macOS restrictions configurations by selecting the **iOS Restrictions Configuration** or **macOS Restriction Configuration** options in the **Priority Settings for Restrictions Configuration** section under the **Admin >Apple > Settings**. This option is disabled by default. For more information on how priority works, see [**Prioritizing Configurations**](./Prioritizing_Configurations.md)

Procedure

1. Go to **Admin > Apple > Settings**.
2. In the **Priority Settings for Restrictions Configuration** section, select the **iOS Restrictions Configuration** or **macOS Restriction Configuration** option.
3. Click **Save** to enable priority. The "**Priority Settings for Restrictions Configuration (iOS or macOS)has been enabled**" banner is displayed. Before the priority is **Approved**:\* **Edit distribution summary(if applicable)**: When priority setting is enabled, the distribution summary for the selected restrictions configuration is changed from "**Apply to devices in other spaces**" is changed to "**Apply to all devices in other device spaces as highest priority**" by default.
   - **Default priority is assigned in the order of creation**: For selected restriction type configuration, an existing default priority is assigned in the order it was created.
   - **Suspension of management of the configuration**: The management of the selected restrictions configuration (for example, iOS Restrictions Configuration) is suspended until you approve the priority.After priority is enabled, any changes in the restrictions are not processed until they are approved. Before approving, the admin can edit the distribution, distribution summary, or priority for restrictions configuration in the **Configurations** section.
4. Select the **Approve** option to put priority in effect.
5. Click **Save**.The **Approval** option is not available when deselecting an iOS or macOS Restrictions configuration option, the changes are applied instantly.

When priority setting is disabled, there is no priority associated with the configurations. All restriction configurations are pushed to the device if applicable (on next device sync).

- **Distribution summary (if applicable)**: When priority setting is disabled for restriction configuration, distribution summary is changed from Apply to all devices in other device spaces as highest priority or Apply to all devices in other device spaces as lowest priority to "Apply to devices in other spaces".
- **No priority is assigned**: Assigned priority is removed for selected restrictions configuration
