---
title: Creating a partner device compliance policy
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

Create a partner device compliance policy in Ivanti Neurons for MDM and apply the desired label. The partner compliance policy reports the device compliance status to Azure or BeyondCorp for conditional access.

Prerequisites

You must have an Azure Tenant ID or a Google BeyondCorp ID set up. For more information about Azure Partner Device Compliance, see [**Connecting Microsoft Azure to Ivanti Neurons for MDM**](./Connecting_Microsoft_Azure_to_Ivanti_Neurons_for_MDM.md).

![](<Resources/Images/Device Compliance2.png>)

Procedure

1. Log in to the Ivanti Neurons for MDM, go to Configurations.
2. Click **Add** and search for the **Partner Device Compliance** configuration.
3. Enter the following details on the **Create Partner Device Compliance Configuration** page: | Item                                                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
   \| -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   \| **Name**                                                                                     | Enter a name.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
   \| **+ Add Description**                                                                        | Enter an explanation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
   \| **Choose Partner**                                                                           | Select **Microsoft Azure Compliance**. or **Google BeyondCorp Compliance - Beta**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
   \| **Configuration Setup**Report Compliance Status to Azure for iOS, macOS, and Android devices | Toggled ON by default. If you do not see this field, you need to set up your Azure Tenant ID.If the Report Compliance Status for iOS, macOS, and Android devices option is enabled, and the compliance policy is applied to the client, the client will display "Microsoft 365 Access" in the devices under Settings. The compliance status of the device is reported when:\* device is out of compliance
   - the device is compliant
   - the device returns to compliance
   - 24 hours passes. If there is no change in the status, a report is sent once a week / every seven days. |
     \| Report Compliance Status to Google BeyondCorp for iOS, macOS and Android devices             | Toggled ON by default.The compliance status of the device is reported when:\* device is out of compliance
   - the device is compliant
   - the device returns to compliance
   - 24 hours passes. If there is no change in the status, a report is sent after every 24 hours.                                                                                                                                                                                                                                                                                                           |
4. Click Next.
5. Enable this configuration is selected by default.
6. Select a distribution level for the configuration. For more information about configuration distribution, see [**Adding a configuration**](./Working_with_Configurations.md).
7. Click Done.
