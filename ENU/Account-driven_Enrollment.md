---
title: Account-driven Enrollment
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

This section is applicable for Account-driven User and Account-driven Device enrollments.

**Supported devices**

- Devices with iOS 15+ (for Account-Driven User Enrollment) and iOS17+ (for Account-Driven Device Enrollment)
- Devices with macOS 14+
- Devices with visionOS 1.1+

**Prerequisites:**

**For Account-driven User Enrollment**

- A user account in Ivanti Neurons for MDM with managed Apple ID (users in Apple Business Manager or Apple School Manager).
- Under the **Apple Enrollment** section, select **User Enrollment** from the **Select Apple Enrollment Type** dropdown list.
- Under the **Users** -> **User Settings** ->set the **Device Owner Settings** to **ON** > select **User Owned** option.

**For Account-driven Device Enrollment**

- A user account in Ivanti Neurons for MDM with managed Apple ID (users in Apple Business Manager or Apple School Manager).
- Under the **Apple Enrollment** section, select **Device Enrollment** from the **Select Apple Enrollment Type** dropdown list.
- Under the **Users** -> **User Settings** ->set the **Device Owner Settings** to **ON** > select **Company Owned** option.

**Account-driven User Enrollment** for iOS 15+, macOS 14+, and visionOS 1.1+ devices is an enrollment option designed for companies implementing BYOD (Bring Your Own Device). Account driven User Enrollment is a modified version of the MDM protocol and User Enrollment with Apple Business Manager with a much greater focus on user privacy, implemented with a level of security that enterprises need.

**Account-driven Device Enrollment** for iOS 17+, macOS 14+, and visionOS 1.1+ devices is an enrollment option designed for companies to enroll company-owned / corporate devices. Account-driven Device Enrollment leverages the MDM protocol and Device Enrollment with Apple Business Manager with a much greater focus on user privacy, implemented with a level of security that enterprises need. End users can enroll their devices using the Work Account feature in Settings.

## Setup the discovery service

If your enterprise has an enterprise domain name, for example, acme.com, then the email ID for your device is [**devicename@acme.com**](mailto\:devicename@acme.com).

1. The user enters [**username@acme.com**](mailto\:username@acme.com) to sign in to their work or school account, then the device makes a HTTP GET request call to the URL:[**https://acme.com/.well-known/com.apple.remotemanagement?user-identifier=user@acme.comFor**](https://acme.com/.well-known/com.apple.remotemanagement?user-identifier=user@acme.comFor) more information, see - [**https://developer.apple.com/documentation/devicemanagement/discover\_authentication\_servers**](https://developer.apple.com/documentation/devicemanagement/discover_authentication_servers)
2. On the acme.com domain, configure redirection rule for the URI - /.well-known/com.apple.remotemanagement to redirect it to the following URL\:https\://\<n-MDM cluster>/.well-known/com.apple.remotemanagement

## Simplified service discovery for Account-driven Device Enrollment

Applicable to iOS 18.2+, macOS 15.2+, and visionOS 2.2+ devices.

For account-driven enrollment, when a user enters their organization email to sign into their work or school account, the device first searches for a well-known HTTP resource at the organization's domain, which contains a link to the MDM enrollment URL.

**Procedure**

1. Sign-in to the Work or School account.
2. Verify domains in **Apple Business Manager** and **Apple School Manager** - Applies only to domains that have been verified within Apple Business Manager or Apple School Manager. If a domain is verified, the device can check with Apple Business Manager /Apple School Manager to get an alternate MDM enrollment URL.
3. Set a default Ivanti Neurons for MDM assignment for **Mac**, **Apple Vision Pro**, **iPhone**, and **iPad** platform types.
4. On the Ivanti Neurons for MDM console, navigate to **Admin** > **Apple** > **Device Enrollment**. In the **Device Enrollment** screen, **ADDE URL** and **ADDE URL SET TIME** columns are added.**First Preference**: The device checks the well-known HTTP resource at the organization’s domain.**Fallback Option**: If the first method fails, the device contacts Apple ABM/ASM to fetch the alternative destination specified by Ivanti Neurons for MDM.
5. Under **Actions**, select **Configure ADDE URL**.
6. Refresh the page.

### Device user instructions

This topic addresses the actions the device user needs to take for registering Account Driven User Enrollment or Account Driven Device Enrollment.

**Procedure**

1. On the device, go to one of the following:\* For **iOS** device - **Settings** > **General** > **VPN** & **Device Management**.
   - For **macOS** device - **System Settings** > **Privacy & Security** > **Profiles**.
   - For **visionOS** device - **Settings** > **General** > **VPN** & **Device Management**.
2. Go to **Sign in to Work or School Account**.
3. Type the work or school account email address. Ensure that the email address is according to the following format\:username@\<enterprise domain name>, for example, [**username@acme.com**](mailto\:username@acme.com).
4. The login page automatically takes the Managed Apple ID and takes the user through iReg flow. Ensure that you enter Ivanti Neurons for MDM credentials.
5. Type the work or school account credentials and click **Continue**.
6. After a 2-factor authentication, the device enrollment completes.
