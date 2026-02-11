---
title: Deploying Windows devices
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Overview**](./Deploying_Windows_devices.md)
- [**Device Management**](./Deploying_Windows_devices.md)
- [**Windows Device Enrollment and Registration**](./Deploying_Windows_devices.md)
- [**Windows Update Management**](./Deploying_Windows_devices.md)
- [**App Management and distribution**](./Deploying_Windows_devices.md)
- [**App Control**](./Deploying_Windows_devices.md)
- [**Windows Device Management Configurations**](./Deploying_Windows_devices.md)
- [**Windows Device Compliance**](./Deploying_Windows_devices.md)
- [**Windows Apps and Hardware Inventory**](./Deploying_Windows_devices.md)

## Overview

Ivanti Neurons for MDM helps you to manage all Windows laptops and desktops including HoloLens 2 end-end device life cycle management: from configuration, enrollment, provisioning, securing, application, management, monitoring, software and OS updates, to retirement.

## Device Management

Windows devices supported:

- Windows PC 10+
- Microsoft HoleLens 2

For more information about the Device Management and reporting functionality, see [**Devices**](./Devices.md)

## Windows Device Enrollment and Registration

Ivanti Neurons for MDM supports all standard device registration methods for Windows devices:

- Manual Registration
- Bulk Enrollment
- via SCCM and Ivanti EPM
- Windows Autopilot
- Entra ID Registration

For more information about the registration methods, see [**Using Microsoft Azure**](./Using_Microsoft_Azure.md)

For information on Multi-User Support, see [**Multi-User Support for Windows devices**](./Using_Microsoft_Azure.md).

## Windows Update Management

- Configuring and Scheduling Windows updates - To configure and schedule Windows updates, create a configuration using Configuration - [**Software Updates**](./Software_Updates.md).
- Windows Update Management - You can view and approve the updates reported by Windows devices that you want to be updated using Windows Update Management. By using this feature, you can prevent the updates that are not necessary or not tested from being installed on the devices. For more information, see [**Windows Update Management**](Windows_Update_Management.htm).

## App Management and distribution

Users can manage complete App life cycle (Import, configuration, schedule, distribution, update and removal) for Windows applications.

Supported App types: 

- In-house
- MSB
- Public store

Supported App extensions:

- MSI
- MSIX
- APPX
- APPX bundles
- EXE (Bridge)

For more details on managing Windows apps, see [**App Configuration**](./App_Configuration.md). To automate app updates, see [**Windows app scheduling**](./Windows_app_scheduling.md) and [**Working with Configurations**](./Working_with_Configurations.md).

## App Control

The App Control configuration allows you to categorize apps as Allowlist or Blockedlist at the device level. Apps that are already installed will not be visible and cannot be launched. Apps will still be visible in the App Store, but they cannot be downloaded or launched. Any device to which the App Control configuration is distributed will use this configuration and ignore any Allowed Apps Policy Settings. The App Control configuration supersedes any app-related policies that refer to the same app on the target devices.

For more details, see [**App Control Configuration: Control Which Apps Are Installed Per Device**](./App_Control_Configuration__Control_Which_Apps_Are_Installed_Per_Device.md).

## Windows Device Management Configurations

Support for Windows 10+ PC and Microsoft HoloLens 2 includes the following abilities:

- [**Device Registration (Windows 10+ PC and Microsoft HoloLens 2)**](./Device_Registration__Windows_10__PC_and_Microsoft_HoloLens_2_.md)
- [**Passcode Configuration**](./Passcode_Configuration.md)
- [**Exchange Configuration**](./Exchange_Configuration.md)
- [**Configurations**](./Configurations.md)
- [**Devices**](./Devices.md)
- [**Apps**](./Apps.md)
- [**Windows app scheduling**](./Windows_app_scheduling.md)
- [**App Control Configuration: Control Which Apps Are Installed Per Device**](./App_Control_Configuration__Control_Which_Apps_Are_Installed_Per_Device.md)
- [**Windows Update Management**](Windows_Update_Management.htm)
- [**Device status reporting from Ivanti Neurons for MDM to Azure**](./Device_status_reporting_from_Ivanti_Neurons_for_MDM_to_Azure.md)
- [**Configuring Windows Autopilot Profiles**](./Configuring_Windows_Autopilot_Profiles.md)
- [**Pushing SyncML to Devices using Custom Configurations**](./Pushing_SyncML_to_Devices_using_Custom_Configurations.md)
- [**Policies**](./Policies.md)
- Windows Restrictions
- Identity Certificates
- Windows Hello for Business
- Wi-Fi and VPN Profiles

Configurations distributed to HoloLens devices that are not supported by this device type, will not be reported as configurations distributed under the Configurations tab in the Device Details.

Windows features (only supported for Windows PC):

- [**Ivanti Bridge**](./Ivanti_Bridge.md)
- [**Windows BIOS Configuration**](./Windows_BIOS_Configuration.md)
- [**Windows BitLocker**](./Windows_BitLocker.md)
- [**Windows Kiosk Configuration**](./Windows_Kiosk_Configuration.md)
- [**Windows License Configuration**](./Windows_License_Configuration.md)
- [**EMA Server Intergration Configuration**](./EMA_Server_Intergration_Configuration.md)
- [**Printer Settings**](./Printer_Settings.md)
- [**Remove Bloatware Configuration**](./Remove_Bloatware_Configuration.md)
- [**ADMX (GPO) Browser**](./ADMX__GPO__Browser.md)

## Windows Device Compliance

Ivanti Neurons for MDM can be set up with Microsoft Azure for seamless enrollment of the users on their Windows desktop and Tablets devices running on Windows 10+. To configure Azure tenant integration to enable Windows Device Compliance, see [**Using Microsoft Azure**](./Using_Microsoft_Azure.md).

## Windows Apps and Hardware Inventory

**Windows App Inventory**

The App inventory is a list of apps detected on enrolled devices. Use this page to get information on the apps being used by enrolled devices. For more information, see [**App Inventory**](./App_Inventory.md).

The App Inventory displays Win32 or Win32 Store apps on a device if the privacy configuration for that device allows collecting the information of all apps on that device.

**Configuring App inventory intervals**

You can set Windows 10 app inventory collection intervals for multiple app source type inventories. The intervals are used when Privacy Configuration is set to collect all apps from the device.

For more information, see [**Configuring app inventory intervals**](./Configuring_app_inventory_intervals.md).

**Windows Hardware Inventory**
