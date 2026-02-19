---
title: Using Microsoft Azure
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM can be setup with Microsoft Azure for seamless enrollment for your users on their Windows desktop and Tablets devices running on Windows 10. Follow the steps below to configure and connect your instances.

This section contains the following topics:

- [**Setting up Entra ID account**](./Using_Microsoft_Azure.md)
- [**Creating Users on Entra ID**](./Using_Microsoft_Azure.md)
- [**Connecting Entra ID to UEM for Windows 10 Devices**](./Using_Microsoft_Azure.md)
- [**Multi-User Support for Windows devices**](./Using_Microsoft_Azure.md)

## Setting up Entra ID account

To set up Entra ID:

1. Go to [**https://azure.microsoft.com/en-in/pricing/purchase-options/**](https://azure.microsoft.com/en-in/pricing/purchase-options/) to purchase your Azure account.
2. Use your existing Hotmail or Outlook.com account, or create a new account and register as a new user.
3. Buy an Azure account by using one of the payment options and following the verification steps.
4. Ask Microsoft to Allowlist the Ivanti Neurons for MDM tenant.
5. Use the same Hotmail or Outlook.com account you used in step 2 to login to Entra ID at [**https://manage.windowsazure.com/**](https://manage.windowsazure.com/)[**https://manage.windowsazure.com/**](https://manage.windowsazure.com/) as an admin.
6. Go to **Domain** tab.A default the domain, TestMiBGLRoutlook.onmicrosoft.com, is created for your account and any users created will belong to this domain. If needed you can recreate a custom domain.

## Creating Users on Entra ID

To create users on Entra ID:

1. Go to active directory - > **Default Directory - >Users**.
2. Selecting the Add user option -> Select New user in your organization.
3. Enter the username. Click next **(->)**.The **User Profile** page is displayed.
4. Add the user information such as, first and last name and the display name.
5. Use the dropdown menu to assign the appropriate role to the user.
6. Generate the temporary password.The user will be required to change this password at the first login.

## Connecting Entra ID to UEM for Windows 10 Devices

To connect Entra ID to UEM:

1. Go to **Admin** > **Microsoft Azure > Windows Enrollment And Compliance Using Entra ID**.
2. Complete the UEM setup steps described in the section, [**Entra ID Windows 10 Unified Endpoint Management Setup**](./Entra_ID_Windows_10_Unified_Endpoint_Management_Setup.md)
3. Complete the [**Assigning Entra ID UEM app**](./Assigning_Entra_ID_UEM_app.md) setup in the Azure portal.
4. In the Ivanti Neurons for MDM Admin Portal, type the domain name of your Entra ID account, and click Connect Azure portal, and then select the checkbox.
5. After signing in successfully, accept the consent that allows MobileIron AD Tenant Validation APP to verify that your Ivanti Neurons for MDM UEM APP is set up. A message appears indicating a successful connection.

### Microsoft Passport for Work for Windows 10 Devices

Microsoft Passport for Work is replaced with Windows Hello for Business. For more Information, see [**Windows Hello for Business Configuration**](./Windows_Hello_for_Business_Configuration.md).

### Windows device Entra ID enrollment

**Prerequisites**

Users must be registered in Ivanti Neurons for MDM.

Connect your domain to enroll user on their Windows 10+ devices.

1. Click **Join Entra ID**.
2. Enter username and password.
3. Click **Sign-in**.
4. Accept the EULA
5. Click **Create PIN**.\* If you have enabled Microsoft Passport for Work PIN complexity, you are prompted to set up a complex PIN as per the configured policy.
   - Entra ID authenticates the user and downloads a JWT (JSON Web Token) to the device.
   - The device is now enrolled.
   - User is contacted through the device for verification.
6. Enter and confirm a PIN.
7. Click **OK**.

## Multi-User Support for Windows devices

Ivanti Neurons for MDM supports multi-user capabilities for the Windows 10 Entra ID enrolled devices. This capability includes pushing some profiles like VPN, WiFi, default email client profiles and Certificates to an individual user and not a device. It also supports distribution of in- house and public apps for the logged- in user. Each time a new Entra ID user logs onto a device, Ivanti Neurons for MDM evaluates not just the device but also the user. If the user is new, Ivanti Neurons for MDM updates the device for that user. If the user is an existing user on the device then any changes to the device and user settings that need to be updated since their last login are evaluated.

The details of the Entra ID user who is logged into the device are reported in the Ivanti Neurons for MDM Admin portal. When the user logs out of the device and the second user logs into the device, the details of the second user is updated in the device details page.

## Setting up Microsoft Store for Business with UEM

Microsoft Store for Business is a portal provided by Microsoft as a part of Azure. Administrators can login to this portal and shop the apps and distribute them to all the managed devices. Ivanti Neurons for MDM can be setup with Microsoft Store for Business to manage applications from within the Ivanti Neurons for MDM admin portal by setting up the following steps.    

### Step 1: Registering Entra ID application in the Microsoft Azure Portal

1. Open the first browser and log into the Microsoft Azure portal ([**https://portal.azure.com/**](https://portal.azure.com/)[**https://portal.azure.com/**](https://portal.azure.com/)).
2. Click **App registrations** on the left pane.
3. Click **+New application registration**
4. Enter the following information to register MobileIron as an Azure app:\* **Name**: Enter a name for the MobileIron app. (This field is required with a minimum of 4 characters.)
   - **Application Type**: Select Web app / API.
   - **Sign-on URL**: Enter the URL device users access to sign into MobileIron (required).
5. Click **Create** to add the app and return to the Azure home page.
6. Go to Settings and create a new key.

### Step 2: Adding the application as a management tool

1. In Microsoft Store for Business Settings, click Manage
2. Distribution Settings
3. In the Add Management tool activate the created application.

### Connecting the account in the Admin Portal

1. Go to **Admin > Microsoft Azure > Microsoft Store for Business**.
2. Under Step 1, **Register Entra ID application**, select the checkbox **Yes, I completed this step**.
3. Under Step 2, **Add Management Tool**, select the checkbox **Yes, I completed this step**
4. Under Step 3, Connect Account, update the following fields:\* Entra ID Domain
   - Application Identifier
   - Application key
   - Sync Interval (hours)
5. Click **Connect**.You will see a confirmation message that the MobileIron store for business is successfully setup.
6. Click **Sync App**.When successfully synced, the status displays as **Applications synced successfully**.

When the Microsoft Store for app is pushed to the device, the app details are available in the under **Installed apps** tab in the device details. Each Microsoft Store for business app reported from device, can be identified as **Microsoft Store for Business** in the **Source** column.
