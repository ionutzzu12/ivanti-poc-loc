---
title: Azure Tenant Requirements
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

This section describes setting up Ivanti Neurons for MDM with Microsoft Azure Tenant.

## Requirements

### Microsoft

Ivanti Neurons for MDM customers must have a valid subscription to Microsoft Intune and assign a Microsoft Intune license to device users.

### MobileIron

- Ivanti Neurons for MDM - Ivanti Neurons for MDM version 75 through the latest version as supported by MobileIron.
- Additional licensing - Azure Device Compliance is a Premium offering and is available to [**Secure UEM Premium**](https://www.mobileiron.com/en/pricing#) and Platinum customers. A Platinum license suffices for existing customers.
- Go for iOS (client) or Go for Android (client) version 75.0 through the latest version as supported by MobileIron.

### Multiple Ivanti Neurons for MDMs support

If you have multiple Ivanti Neurons for MDMs connected to the same Azure tenant, disconnect from all Ivanti Neurons for MDMs or disable compliance policy for Entra ID compliance integration from a specific (single) Ivanti Neurons for MDM so that it does not upload device data to Azure

Be sure to disable the compliance policy prior to disconnecting Ivanti Neurons for MDM.

## Ivanti Neurons for MDM administrator's process

The process from the Ivanti Neurons for MDM administrator's perspective:

1. Administrator applies Intune licenses to device users. See [**Apply the Intune license to device users**](./Apply_the_Intune_license_to_device_users.md).
2. Administrator logs into Azure Portal.
3. Administrator adds MobileIron as an Azure compliance partner. See [**Adding MobileIron as a compliance partner**](./Adding_MobileIron_as_a_compliance_partner.md).
4. Administrator creates the Conditional Access policy for the apps. See [**Creating a conditional access policy in Microsoft Endpoint Manager**](./Creating_a_conditional_access_policy_in_Microsoft_Endpoint_Manager.md).
5. Administrator sets up the connection between MobileIron and Azure. See [**Connecting Microsoft Azure to Ivanti Neurons for MDM**](./Connecting_Microsoft_Azure_to_Ivanti_Neurons_for_MDM.md).
6. Administrator creates the device compliance policy in Ivanti Neurons for MDM. See [**Creating a partner device compliance policy**](./Creating_a_partner_device_compliance_policy.md).
7. The Conditional Access policy goes into effect. Depending upon whether the device is compliant or not, the access to the app(s) is granted or denied.Ivanti recommends the administrator run tests on each Microsoft app.
