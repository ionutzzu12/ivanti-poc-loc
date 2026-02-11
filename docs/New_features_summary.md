---
title: New features summary
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:51 GMT+0200 (Eastern European Standard Time)
---

This section provides summaries of new features and enhancements that are available in this release. References to documentation describing these features and enhancements are also provided, when available.

[**General features and enhancements**](./New_features_summary.md)

[**Android features**](./New_features_summary.md)

[**iOS, macOS, watchOS, visionOS, and tvOS features**](./New_features_summary.md)

## General features and enhancements

- **Enhanced Rule and Account Groups Limit**: Limits have been increased for rule and account group evaluations, capping them at 200 rules. This can resolve issues caused by large rule sets, prevent object mapper failures, and improve elastic search performance.
- **Dual Certificate Support for Sentry-Tunnel Communication**: To mitigate service disruptions caused by certificate expiration, a new **Add second certificate field** has been introduced. This enhancement allows administrators to upload and link two certificates—a primary and a secondary (reserve)—to a Sentry profile. Additionally, the expiry date of each certificate is now displayed, enabling proactive tracking and timely renewal, ensuring uninterrupted Tunnel-to-Sentry communication.For more information, see [**Setting Up AppTunnel**](./Setting_Up_AppTunnel.md).
- **Enhanced Audit Trail Export Security**: The Audit Trail Export feature now supports additional secure algorithms for SFTP connections:\* **Key Exchange**: Added support for curve25519-sha256
  - **HMAC**: Added hmac-sha2-256 and hmac-sha2-512These enhancements improve connection security. For more information, see [**Exporting Audit Trails**](./Exporting_Audit_Trails.md).
- **Notification support for Sentry**: Ivanti Neurons for MDM now periodically monitors the Sentry service connection availability. Ivanti Neurons for MDM displays notifications from Sentry versions 10.4 and supported new versions.

## Android features

- **Support to Hide and Suspend Apps**: From the App Configuration section, apps can now be hidden or suspended on fully managed devices.For more information, see [**App Configuration**]().
- **Support for Secondary SIM Attributes on Android devices**: The system now captures and displays **Phone Number 2** and **ICCID 2** for dual-SIM Android devices. For Android devices on version less than 13, NA for Phone Number 2 and ICCID2 will be shown. In case of devices in Work Profile mode, the ICICD2 value will also be shown as NA. These attributes are visible in Device details, Advanced search, and Custom reports in Fully managed device mode and Work profile on company-owned device mode.
- **App Deployment Workflow for Android Enterprise**: Administrators can now initiate app installations and updates using step-by-step workflow in the App Catalog. The process includes targeted delivery based on app presence, user group selection, and compatibility, with real-time confirmation and visibility into actions via audit trails. For Public and Private apps, only installation (not updates) can be triggered through this interface.For more information, see [**App Configuration**](./App_Configuration.md).

## iOS, macOS, watchOS, visionOS, and tvOS features

- **Apple DDM Filter for DDM Config**s: A new filter **Apple DDM** (Declarative Device Management) with the option **Supported** has been added under **Configurations** > **Add Configuration** to help identify DDM-related configurations more easily in the UI. This enhancement improves the user experience by enabling better differentiation of DDM configuration types.
- For more information, see [**Working with Configurations**](./Working_with_Configurations.md).
  **Web Content Filter Configuration support for macOS devices**: The Web Content Filter Configuration is now supported for macOS devices.For more information, see [**Web Content Filter**](./Web_Content_Filter.md).
- **Support for AppConnect Certificate Configuration in Pulse Secure App (iOS)**: AppConnect Certificate Configuration for Ivanti Secure Access Client (iOS) is now supported in Ivanti Neurons for MDM settings. The “AppConnect Certificate Configuration” section is visible for the App Store Ivanti Secure Access Client (iOS) in Ivanti Neurons for MDM.
- **Beta Management in Device Enrollment Profile**: Device Enrollment Profile now supports Beta Management on iOS 17 and macOS 14 devices. A new field is added for beta programs under **Require minimum OS version for enrollment** selection for iOS and macOS devices. For more information, see [**Device Enrollment**](./Device_Enrollment.md).
- **View Platform Information for Licenses**: Administrators can now view platform information for license details in the VPP details page. For more information, see [**Apple Apps and Books**](./Apple_Apps_and_Books.md).
- **Support Tab in Ivanti Go Client**: **Ivanti Go Client Privacy** is now renamed to **Ivanti Go Client Settings**. A new field **Enable Support Tab** is added in **Ivanti Go Client Settings Configuration**. For more information, see [**Ivanti Go Client Settings**](./Ivanti_Go_Client_Settings.md).
- **Support for Apple Access Management**: Ivanti Neurons for MDM now supports **Apple Access Management** for Supervised and Managed devices. For more information see, [**Apple Access Management**](./Apple_Access_Management.md).

## Mobile Threat Defense features

Mobile Threat Defense (MTD) protects managed devices from mobile threats and vulnerabilities affecting device, network, and applications. For information on MTD-related features, as applicable for the current release, see the Mobile Threat Defense Solution Guide for your platform, available under the MOBILE THREAT DEFENSE section on the Ivanti [**Product Documentation**](https://www.ivanti.com/support/product-documentation) page.

Each version of the MTD guide contains all Mobile Threat Defense features that are currently fully tested and available for use on both server and client environments. Because of the gap between server and client releases, new versions of the MTD guide are made available with the final release in the series when the features are fully functional.
