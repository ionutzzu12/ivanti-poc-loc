---
title: Enrolling Oculus devices
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM can now manage the Quest for Business devices (Oculus devices). Currently, Meta supports Oculus for Business (OFB) and Quest for Business (QFB) devices for MDM. You need to perform some basic tasks on the Meta console to make the devices MDM-ready and then register for Ivanti Neurons for MDM.

You can enroll the Oculus device fleet in the Device Manager under the Meta Workplace console. You need to log in to the Oculus Business Workplace using the credentials shared on your registered email. On the Home page, All Devices information will be displayed under the Device Fleet section. The Device Fleet section provides an overview of all the devices available under Device Management. These details include the Device Name, Device Status, OS (Operating System), Model, etc.

This section contains the following topics:

- Prerequisites to enrolling Oculus devices
  - [**Setting up an MDM app in the Device Manager**](./Enrolling_Oculus_devices.md)
  - [**Setting up the Oculus device**](./Enrolling_Oculus_devices.md)
    Register an OFB device with MobileIron Go
  - [**On Ivanti Neurons for MDM Console**](./Enrolling_Oculus_devices.md)
  - [**On Go client**](./Enrolling_Oculus_devices.md)

## Prerequisites to enrolling Oculus devices

### Setting up an MDM app in the Device Manager

The Devices / Headsets are provisioned and updated to at least **v28** of **Oculus for Business**. On the Meta Console, the administrator must set up an MDM in the Device Manager and map the Oculus devices to this specific MDM service.

**Procedure**

1. On the **Oculus Business Workplace** home page, select **Apps**.
2. Under the **App Library**, click on the third-party MDM app that you want to install, and then click **Update**.
3. Select the appropriate MDM for the app from the list under **Mobile Device Management** and then click **Update App**.
4. Click the Oculus Device headset on which you want to install the MDM. The device information will appear on the screen.
5. Under the **About** tab, scroll down to **Mobile Device Manager**.
6. Click the **Edit** button next to the **MDM Authority** option.
7. By default, the Oculus Device Manager option will be selected. You need to select the MDM Authority App and select **MobileIron Go** from the MDM Authority App list.
   Click **Save**. The Device automatically resets and then you need to set up the Oculus device using the setup app.

### Setting up the Oculus device

You can add Oculus Quest 2 Headset devices using the Device Setup app. This app must be shared with the required users so that the users can download and install the app on their Android devices.

**Procedure**

1. Under the **Device Fleet** section, click **Unconfigured Devices**.
2. Click **Get Setup App**. The **Send Download Link** page appears on the screen.
3. Select one or more team members from the list or click **Add recipient** to select from the list.
4. Click **Send Link**. The selected users will receive an email with a link to install the **Device Setup** app.
5. Click the **Download Device Setup App** link in the email to install the **Device Setup App** on your Android device.
6. After downloading, this app will not appear in the App Store of your device. You need to get it from the Downloads section of your device and install it.
   Open the **Oculus for Business** app from your Android device.
7. Power ON the Oculus devices by pressing the power button for 2 seconds.
8. Turn on Bluetooth and place your Android device close to the Oculus devices until the setup is complete.
9. Search for Oculus devices using Bluetooth of your Android device.
10. Once the required Oculus device is found, you need to connect it to a Wi-Fi network to complete the setup.
11. Click **Enter Wi-Fi Information** and provide the Network Name and Password and then click **Save**. Now, the Oculus device is connected to the Wi-Fi network.
12. Click **Start Setup**. A notification appears on the screen that the setup is in progress, and you should not close the app or handle the headsets during the setup.
    A confirmation appears on the screen. You can continue to search for more devices using the **Find More Devices** button.

## Registering an OFB device with MobileIron Go

### On Ivanti Neurons for MDM Console

An OFB device can be registered with MobileIron Go on Ivanti Neurons for the MDM console. However, the Work Managed Device Non-GMS mode (AOSP) configuration (under **Configurations**) must be distributed to these OFB device groups.

### On Go client

An OFB device can be registered on the MobileIron Go client. You need to perform the following tasks to register the OFB device:

- After completing the setup using the OFB Setup app, continue with the on-screen instructions on the OFB headset and complete the device setup.
- The MobileIron Go app launches automatically and you need to provide the login credentials and complete the registration by following the MDM instructions.

Now, the device is provisioned in DO mode and is set to be managed by the MDM.
