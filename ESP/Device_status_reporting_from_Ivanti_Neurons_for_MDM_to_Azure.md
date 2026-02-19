---
title: Device status reporting from Ivanti Neurons for MDM to Azure
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

For the following cases, Ivanti Neurons for MDM reports device inventory and compliance status.

- On-device compliance state change
- On-device inventory change
- Once a week, Ivanti Neurons for MDM reports compliance and inventory status

Depending on the action chosen in the compliance policy, the following device status will be sent:

| Action(most restrictive one applies)     | What Ivanti Neurons for MDM sends       |
| ---------------------------------------- | --------------------------------------- |
| Block Email, AppConnect Apps, Quarantine | Device Non-compliant                    |
| Send Alert                               | Compliant to Azure                      |
| Retire device                            | Device data removed from Azure platform |

## Device Details page

To view the Azure information about the device, go to the Device Details page. The description of the fields and their possible values:

| Field                          | Description                                                                                                                                                                                                                                                                                                                            |
| ------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Azure Device Identifier        | The device ID reported by Microsoft to the iOS or Android device. For example: 007c8232-9489-4074-9b35-345b16f0a72d. Ivanti Neurons for MDM receives this device ID as device users are required to register to Microsoft Authenticator application to use this feature.If unable to retrieve the Device ID, this field is left blank. |
| Azure Device Compliance Status | Lists the device's compliance status in Azure. Possible values:\* In-progress                                                                                                                                                                                                                                                          |

- Successful
- Failed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \| Azure Client Status Code            | Indicates whether device is connected to Azure. Possible values:\* Success - Able to retrieve device ID.
- Internal\_Error - An unrecoverable error occurred either within the client or on server side.
- Workplace\_Join\_Required - Registration of device required. Device user can mitigate this status.
- Interaction\_Required - An interactive log-in is required. Device user can mitigate this status.
- Server\_Declined\_Scopes - Some scopes were not granted access to.
- Server\_Protection\_Policies\_Required - The requested resource is protected by an Intune Conditional Access policy.
- User\_Canceled -The device user cancelled the web Auth session by tapping the "Done" or "Cancel" button in the web browser.
- Account\_logged\_out - Account logged out. |
  \| Azure Device Compliance Report Time | The time Ivanti Neurons for MDM reported the device compliance status to Microsoft Intune. A blank field indicates one of the following:\* that feature is disabled
- Ivanti Neurons for MDM received the data and has yet to call the Microsoft API
- there is an error such as user\_Cancelled or Internal Error                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
