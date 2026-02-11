---
title: Preview features available in Sandbox tenants
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:54 GMT+0200 (Eastern European Standard Time)
---

This section lists the features currently available **ONLY** on the Ivanti Neurons for MDM sandbox instance. The Ivanti Neurons for MDM sandbox instances are available to Enterprise Users by default. You can access these features from the N-MDM sandbox instance and provide any feedback you have about such features.

If you need access to the sandbox instance, contact [**Ivanti Sales**](https://www.ivanti.com/lp/contact-us).

## Releases

This section contains the Sandbox-only features for the following releases:

- [**Current Release - R118**](./Preview_features_available_in_Sandbox_tenants.md)\* [**Apple PassKeys Attestation**](./Preview_features_available_in_Sandbox_tenants.md)
  - [**Apple Restrictions Configuration:**](./Preview_features_available_in_Sandbox_tenants.md)

## Current Release - R118

### Apple PassKeys Attestation

Use the Passkey Attestation configuration to configure the device to allow WebAuthn enterprise attestation for certain passkeys.

Passkeys are created on managed devices, and SecurityPasskeyAttestation uses an Enterprise Managed Credential to attest the passkey with a corporate certificate. Supported credentials include SCEP, ACME, and Identity credentials.

The Passkey Attestation supports the following:

- Minimum supported operating system versions: macOS 14
- Supported enrollment methods: Device Enrollment
- Managed Apple Accounts are required to control syncing of passkeys.
- Can be used in conjunction with Access Management from ABM.

Passkeys payload fails on Mac. The certificate assets are not hosted on authenticated endpoint.

When creating a Passkey Configuration, you must first create an Identity Certificate Configuration, and link that to Passkey Configuration. Also, provide the following details in Security Passkey Attestation Configuration section:

| **Field**                                                                      | **Description**                                                                                                                                                   |
| ------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                                                                           | Name of the passkey.                                                                                                                                              |
| Description                                                                    | Any information about the configuration.                                                                                                                          |
| Attestation Identity Asset Reference\* Attestation Identity Key is Extractable | Provide the asset reference identity that you have created to link to the Passkey Configuration.Select this option to confirm if the identity key is extractable. |
| Relying Parties                                                                | Enter the details for authenticated domains.                                                                                                                      |

### Apple Restrictions Configuration:

**Enhancement to Restrictions Settings**: The user interface of the **Restrictions Configuration** page has a fresh look for **Apple Restrictions Configurations** with the following changes:

- Previously, the administrators had to configure the iOS and macOS restrictions separately. Now, the administrators can navigate to **Configurations** > **+Add** and select **Apple Restrictions**. Additionally, the administrators can now select the **Platform Type** from the drop-down list to add a new Apple Restriction.
- The **Restrictions Settings** pane now segregates multiple settings under relevant tabs such as **Device Functionality**, **Applications**, **Security and Privacy**, and so on. If Apple releases a new restriction, then the new restriction automatically populates in the respective tab.
- The **Restrictions Settings** pane now allows administrators to push the selected settings to the devices using the **Push to Device** toggle button.
