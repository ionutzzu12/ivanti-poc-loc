---
title: Configuring Windows Autopilot Profiles
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Windows Autopilot is a Microsoft feature that helps administrators to setup and pre-configure new devices to make them business ready. The Autopilot feature helps with a quick, reliable, and seamless provisioning of Windows Desktop or HoloLens2 devices. In addition, the Autopilot feature helps perform the following tasks:

- Automatically join devices to Entra ID (Entra ID)
- Auto-enroll devices into MDM services
- Create and auto-assign devices to configuration groups based on the profile of the device
- Customize the enrollment experience
- Apply configurations and policies
- Install essential applications

### Prerequisites

To operate the Windows Autopilot page, review the Ivanti Neurons for MDM partner steps and Azure licensing requirements. Make sure that the following prerequisites are met for the Autopilot feature to function as expected:

- **Azure Licensing for Autopilot requirements**: Check for “Windows Autopilot licensing requirements."
- **Azure Windows Autopilot Devices Registration**: Check for "Windows Autopilot registration overview."
- **Resellers adding devices to customer account**: Check for "Use Windows Autopilot profiles on new devices to customize a customer's out-of-box experience."

### Additional Requirements

1. Integrate Entra ID tenants and Ivanti Neurons for MDM. For more information, see [**Setup with Microsoft Azure**](./Setup_with_Microsoft_Azure.md).
2. Make sure that you have an administrator account in Ivanti Neurons for MDM and Entra ID.
3. To leverage self-deploying profiles, create a fake user for enrollment of user-less self-deploying devices in Ivanti Neurons for MDM.
4. Create and sync a dummy user, fooUser\@Entra IDPrimaryDomain.com from Entra ID Primary Domain.Microsoft licenses are not needed to create and sync a dummy user.
5. The "Custom domain names" page in Entra ID displays the primary domain of your Entra ID environment.
6. Make sure that the user can enroll devices and is not disabled. For example, if the primary domain is contoso.com, resulting user will be [**fooUser@contoso.com**](mailto\:fooUser@contoso.com). If the primary domain is contoso.onmicrosoft.com, resulting user will be [**fooUser@contoso.onmicrosoft.com**](mailto\:fooUser@contoso.onmicrosoft.com).
7. To provision the user with SCIM into Ivanti Neurons for MDM, edit the user details in Entra ID and add the email address. Generally, the email address will be the same as UPN.
8. Make sure that all the users, including the fooUser are present in Azure and Ivanti Neurons for MDM.
9. Administrators can create Autopilot Profiles using Microsoft Store for Business or Ivanti Neurons for MDM. To create profiles using Ivanti Neurons for MDM administrators require Global Entra IDmin and Intune administrator permissions.Administrators need Azure P1 or P2 and Ivanti Neurons for MDM Secure UEM or Secure UEM Premium licenses are needed. The Intune license is not needed for administrators.In Neurons for MDM, creating Autopilot Profiles feature leverages Microsoft Graph APIs for Autopilot, which are still in beta.

### Autopilot Enrollment Modes

After you associate devices with a specific user profile group, basis the device usage, you can configure the Autopilot enrollment mode to allow users to quickly get started with their device. Ivanti Neurons for MDM provides the following Autopilot enrollment modes:

- Self-Deploying mode
- User-Driven (Pre-Provisioned mode)
- User-Driven

**Self-deploying autopilot mode** - The self-deployment Autopilot device enrollment mode makes sure that a seamless deployment of an enterprise device for a user by bypassing the initial device setup and by pushing all the necessary configuration files that are required for the device to securely get started. This mode secures the hardware, connects the device to the enterprise network, enrolls the device to the Entra ID (Entra ID), the MDM service, and to the Ivanti Neurons for MDM administrator portal using a dummy user ID and all the necessary configuration files are pushed to the device before the user logs in. After the mandatory configuration files are pushed to the device, the device restarts and displays the login screen for the enterprise user to get started. You can use the self-deploying mode for a device that can be used as a kiosk or digitally signed device.

**User-driven pre-provisioning profile mode** – Once the administrator creates a User-driven pre-provisioned profile, the administrator assigns the profile to a user group, and the device hardware ID is uploaded and assigned to the Entra ID group. The device will be associated to the user-driven pre-provisioned profile. This mode is used by the administrator to setup a device before it is handed over the enterprise user.

**Procedure**

Follow the steps for pre-provisioned deployment:

1. Connect the new hardware device to the LAN and press the Windows button five times.
2. The device displays a question prompt. Select the option Windows autopilot provisioning and click Continue. The Entra ID detects the User-driven pre-provisioning profile mode, and all the basic configuration settings are deployed in the device. The Windows Autopilot Configuration screen is displayed.
3. Click Proceed. The device progresses and secures the hardware, connects the device to the enterprise network, enrolls the device to the Entra ID (Entra ID), the MDM service, and to the Ivanti Neurons for MDM administrator portal using a dummy user ID and all the necessary configuration files are pushed to the device and a confirmation message appears.
4. You can now hand over the device to the user. When the user logs in to the device, the user ID is enrolled into the Ivanti Neurons for MDM administrator portal with the device details.

- The following configurations are pushed automatically before the user logs in to the device:\* Identity Certificate
  - Wi-Fi
  - Windows Hello For Business
  - Windows Restrictions

The rest of the configurations are in Pending state and are pushed after the user logs in to the device using an email address.

During the Autopilot enrollment process in Self-deploying and User-driven (pre-provisioning) modes, the assigned .MSI, and .EXE apps will be installed on the device to complete the enrollment process. When installing the .MSI, and .EXE apps during Autopilot enrollment process, if the apps report or fail to report during the installation, the Autopilot process will be completed and the Reseal button will be enabled.

## Creating Windows Autopilot User Profiles

After you configure the Entra ID (Entra ID) User Source and sync the users and Entra ID user groups with the Ivanti Neurons for MDM tenant, you can create the Autopilot profiles.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrator portal.
2. Go to **Admin > Microsoft Azure > Windows Device Management**.If the Entra ID User Source is not configured, the **Add** button will be disabled. You need to configure the User Source using the **Windows Device Management** option present under the **Microsoft Azure** section.
3. Click **Add**.The **Add Windows Autopilot Profile** page appears on the screen.
4. Enter a profile name in the **Name** box.
5. Complete the **Profile Settings** using the table below this procedure.
6. Click **Next**.A new page with all the Entra ID Device Groups appears on the screen.
7. Select the one or more Entra ID Device Groups to which the Autopilot Profile must be assigned.
8. You can also create a Entra ID Device Group and assign the Autopilot Profile to this newly created group. See [**Creating Entra ID Device Groups**](./Configuring_Windows_Autopilot_Profiles.md) for more information.
   If you want to assign the Autopilot Profile to all the Entra ID Groups, select the **Assign to all Entra ID Groups** option.You cannot assign more than one profile to “All Groups” due to a limitation from Microsoft.
9. Click **Done**.

| Setting         | Description                                                                       |
| --------------- | --------------------------------------------------------------------------------- |
| **Device Type** | Select one of the following two options depending on the device:\* **Windows PC** |

- **HoloLens** - When this option is selected, the default deployment mode should be set to **Self-Deploying** mode.In rare cases, when enrolling HoloLens 2 devices using Autopilot, the enrollment might get stuck on the 'Setting up your device for work' screen. In such a rare case, the user must power off and on the device by pressing the Power button. The device then shows the Login screen where the user should enter the Entra ID credentials to complete the enrollment. |
  \| **Deployment mode**                           | - **Self-Deploying**: In this mode, the device deployment happens with little or no manual involvement.
- **User-Driven**: Administrators can use this option to select the enrollment mode to configure a new device for the user before they hand over the device to the user.                                                                                                                                                                                                                                                                                            |
  \| **User account type**                         | \* **Administrator**: Select this option if the user needs complete control once the device is deployed.
- **Standard**: Select this option if the user needs authorization to the basic options once the device is deployed.                                                                                                                                                                                                                                                                                                                                                |
  \| **Language**                                  | By default, the language will be Operating system specific. You can change to a different language from the list.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| **Convert all targeted devices to Autopilot** | Select this option to convert all devices in the assigned group to Autopilot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
  \| **Allow Pre-provisioning**                    | Select this option to register devices for Autopilot using the normal registration process. This option is not available when the **Self-Deploying** option is selected.                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| **Automatically configure keyboard**          | Select **Yes** to skip the Keyboard selection in case the **Language** option is set to a different value other than the default value.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \| **Device name template**                      | Enter a template name to use during the device enrollment process.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| **Microsoft Software License Terms**          | You can Show or Hide this option only in User-Driven Deployment mode only.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| **Privacy settings**                          | You can Show or Hide this option only in User-Driven Deployment mode only.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| **Change account options**                    | You can Show or Hide this option only in User-Driven Deployment mode and when the User account type is Standard type.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

**Windows Device Management**

The administrator can configure the Autopilot feature on a tenant using the new option Windows Device Management. This option makes it easier to integrate with Ivanti Neurons for MDM if the user has an Entra ID environment.

To access this option, **Admin** > **Microsoft Azure** > **Windows Device Management**.

This integration grants permissions to Ivanti Neurons for MDM to manage devices, Autopilot profiles, check Windows device compliance, and validate the Azure tenant.

**Related Topics**

- [**TenantLockdown CSP**](./TenantLockdown_CSP.md)

## Creating Entra ID Device Groups

The administrator can create Entra ID Device Groups, as and when needed, from the Entra ID Device Groups section. The Entra ID tenant validation must have been configured under the Device Compliance section to create Entra ID Device Groups.

**Procedure**

1. Go to **Admin** > **Microsoft Azure** > **Entra ID Device Groups**.
2. The **Entra ID Device Groups** page appears on the screen.
   Click **ADD**.
3. The **Group Settings** page appears on the screen.
   Provide the following details:\* Group Name
   - Group Description
   - Membership Type\* Static Device - The administrator will get the list of available static devices on the **Assign Members to Group** window. Select the required devices and click **Save**.
     - Dynamic Device - The administrator has to provide certain criteria from the **Dynamic Query** window.

The new Entra ID Device Group will be created and the administrator can add devices to the newly created group.

After creating a dynamic group, the devices will be listed under the Devices tab of the specific device group after sometime.

## Editing Autopilot Devices

Users can edit the Autopilot devices from the Ivanti Neurons for MDM administrative portal.

**Prerequisites**

Make sure that the following prerequisites are met:

- IT Admin user should have Azure Global Admin and Intune Admin permissions.
- A user-friendly name can be set only if the user is set.
- The device name cannot be unset once set.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Log in to the Ivanti Neurons for MDM administrative portal.
:::

:::WorkflowBlockItem
Go to **Admin** > **Windows** > **Autopilot**. The Autopilot Devices are listed under the Autopilot Devices tab.
:::

:::WorkflowBlockItem
Click **Edit** (pencil icon). The edit page appears.
:::

:::WorkflowBlockItem
Edit the following details:
:::

:::WorkflowBlockItem
- **User**
- **User Friendly Name**
- **Device Name**
- **Group Tag**
  Click **Save**. The device details are updated.
:::
::::

## Deleting Autopilot Devices

Users can delete the Autopilot devices from the Ivanti Neurons for MDM administrative portal.

1. Log in to the Ivanti Neurons for MDM administrative portal.
2. Go to **Admin** > **Windows** > **Autopilot**. The Autopilot Devices are listed under the Autopilot Devices tab.
3. Click **Delete**. The device details are deleted.
