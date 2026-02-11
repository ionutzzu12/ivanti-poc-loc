---
title: Apple Configurator
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

You can use this page to prepare Apple Configurator for setting up Ivanti Neurons for MDM device management on iOS devices. Apple Configurator makes it really easy to deploy iOS devices in large quantities. Additionally, Configurator lets administrators make iOS devices Supervised, which allows for greater levels of configuration and management capabilities. For more information about Apple Configurator, please see the Mac App Store.

The basic steps are:

1. Export the MDM profile from your Ivanti Neurons for MDM tenant.
2. Import the MDM profile into the Configurator.
3. Use the Configurator to apply the MDM profile to tethered devices.

## Defining a default user for devices

Devices configured through the Apple Configurator are assigned to the nobody user in Ivanti Neurons for MDM unless you pick a different user:

1. Click in the **Assign configured devices** to field.
2. Start typing the username of the Ivanti Neurons for MDM user you want to select.
3. Select the username when it displays in the drop-down list.
4. Click **Save**.

## Installing apps using Apple Configurator

Before using the Apple Configurator to install apps:

- Access to the Apple app store is restricted by the device configuration.
- Apps installation is permitted by the device configuration.
- Apple Configurator must be installed on the computer used to configure the devices.

To install apps using the Apple Configurator:

::::WorkflowBlock
:::WorkflowBlockItem
In Ivanti Neurons for MDM, go to **Admin > Apple Configurator**.
:::

:::WorkflowBlockItem
Switch the enroll devices toggle switch to On.
:::

:::WorkflowBlockItem
Click one of the following:
:::

:::WorkflowBlockItem
- **Default User's plist**.
- **Specific User's plist** - Enter the specific user's username or email ID.
  In the Apple Configurator, go to **Prepare > Apps**.
:::

:::WorkflowBlockItem
Go to **Prepare > Setting and disable Supervision**.
:::

:::WorkflowBlockItem
Select the **Never update device** option in Update iOS.
:::

:::WorkflowBlockItem
Click **Prepare**(bottom of the Apple Configurator).The apps will be visible in the list of  Installed apps on the device after a device check-in.
:::
::::

## Installing apps using UEM server

To install apps using the UEM server:

1. Upload an app from the in house store in the Apps tab.
2. Select the app.
3. Click the **App Configurations** tab.
4. Select **Install on Device**.Complete configuration settings.
5. Select **Actions > Force Check-in**.

## What the end user needs to do

Apple requires the end-user has to launch the Go at least once, or the Ivanti Neurons for MDM Location feature will not function properly. This is to ensure that the end-user is aware that their location is being tracked.

**Caution:** If devices are deployed in single app mode using Configurator, then this approach will not be possible.

If you cannot see the **Install Apple Configurator** page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- System Management
- System Read Only
