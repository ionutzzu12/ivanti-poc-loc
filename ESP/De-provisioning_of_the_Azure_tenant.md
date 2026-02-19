---
title: De-provisioning of the Azure tenant
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

If multiple Ivanti Neurons for MDMs are enabled to use the same Azure tenant, de-provision from all Ivanti Neurons for MDMs. If a single Ivanti Neurons for MDM needs to stop using Azure, you can disable the partner compliance policy for that Ivanti Neurons for MDM only.

If the administrator performs a disconnect on Ivanti Neurons for MDM, then Ivanti Neurons for MDM stops reporting the device inventory and compliance status to Azure.

Prequisites

- make sure all the devices as unmanaged
- make sure all the devices as non-compliant

Procedure

### Microsoft

1. Log in to Microsoft Azure.
2. Go to Intune > Conditional Access. Make sure the conditional access policy is disabled.

### Ivanti Neurons for MDM

1. Log in to Ivanti Neurons for MDM and go to Admin.
2. In the left navigational pane, click Microsoft Azure > Device Compliance for iOS & Android.
3. Click on Disconnect Account.

::Image[]{src="Resources/Images/AAD_Deprov_confirm.png" signedSrc="Resources/Images/AAD_Deprov_confirm.png" size="36" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Deprov_confirm.png" githubPath="Resources/Images/AAD_Deprov_confirm.png" position="flex-start" indent="2"}

4. Click Yes.

### Retiring a device from Azure

Upon device retirement, Ivanti Neurons for MDM reports to Azure that the device is no longer under management and is non-compliant.

Azure deletes the retired device entry after 90 days.

### Azure account activity recorded in the logs

All activity is recorded in the Logs.

![](Resources/Images/AAD_logs.png)
