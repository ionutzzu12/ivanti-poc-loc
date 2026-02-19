---
title: Setting up the Provisioner app
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Provisioning Requirements**](./Setting_up_the_Provisioner_app.md)
- [**Enable Android beam to use NFC bump**](./Setting_up_the_Provisioner_app.md)
- [**Provision a corporate-owned device**](./Setting_up_the_Provisioner_app.md)
- [**Register the device**](./Setting_up_the_Provisioner_app.md)
- [**Verify the device registration status**](./Setting_up_the_Provisioner_app.md)

Provisioner is a Ivanti Neurons for MDM app used to provision corporate-owned devices so that they can be registered as work managed devices and placed in Device Owner mode.  

A company-managed device has a corporate profile only and no personal profile. The administrator is able to set over twenty lockdowns on the device, that can restrict device functions such as the camera, phone calls, SMS, networking, and more.

The Provisioner app is needed by the device that will initiate the configuration of the Android Enterprise target device with an NFC bump. To provision corporate-owned devices, install the Provisioner app onto a master device, and use the NFC (near field communication)  bump to provision new devices. The bump is tapping the two devices together. The devices can be provisioned to use one of the client apps:

- Go to use with Ivanti Neurons for MDM
- At Work UEM, an unbranded client app, to use with Ivanti Neurons for MDM.

## Provisioning Requirements

To provision a corporate-owned Android Enterprise device to be a work managed device:

- Corporate-owned native Android Enterprise-capable devices must be factory reset prior to provisioning.
- Android Enterprise configuration must be defined and applied to the Android device group.
- An NFC-capable Android device designated to serve as the master or as the template, with the Provisioner app installed.
- Android Enterprise-capable devices to provision.
- Provisioner appDownload the Provisioner app for Android from Google Play.

## Enable Android beam to use NFC bump

**Procedure**

1. Go to **Settings** on the device.
2. Go to **Wireless & networks** and click **More**.
3. Select the **NFC** checkbox.
4. Click **Android Beam** and slide the switch to **On**.

The exact steps may differ slightly for your device.

## Provision a corporate-owned device

**Procedure**

1. Install the Provisioner app on the device to be used as the Android master device.
2. Launch Provisioner on the master device.
3. Select an app from the dropdown menu.
4. Enter the information requested by the Provisioner app. Some fields may auto-populate if a supported Wi-Fi type is present. Use these guidelines:| **Field**                   | **Value**                                                                                                                              |
   \| --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
   \| Select app for provisioning | Go (select for use with Ivanti Neurons for MDM)At Work UEM (unbranded client app; select for use with branded Ivanti Neurons for MDM). |
   \| Wi-Fi Network SSID          | Enter the Wi-Fi SSID the master device is to use.                                                                                      |
   \| Wi-Fi Security Type         | Enter the Wi-Fi security type                                                                                                          |
   \| Wi-Fi Password              | Enter the password for the Wi-Fi                                                                                                       |
   \| Time Zone                   | Enter the local current time zone                                                                                                      |
   \| Locale                      | Enter the locale                                                                                                                       |
5. Click **Continue**.The **Bump the devices** screen is displayed on the master device.
6. With the target device turned on and displaying the Android Welcome screen, press the master device back-to-back with the target device to initiate an NFC transfer.If the NFC transfer is successful, the target device may make a sound, and then proceed to downloading the chosen client app. If the device is not encrypted, it will start the encryption process before continuing.
7. Continue to provision additional devices by bumping the devices. The target device must display the Welcome screen, and the master device must display the **Bump the devices** screen.

## Register the device

Once the corporate-owned device has been provisioned using NFC bump, it will have the selected client app installed. Launch the client app and register the device.

## Verify the device registration status

**Procedure**

1. Go to **Devices > Devices**.
2. Click the link for a device to view the details.
3. The status of the device is listed in the left pane.
