---
title: Variables
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

You can use variables in certain configuration fields to represent values specific to a given user. Any field that supports variables displays a list of supported variables if you type $ in the field. This section contains the following topics:

- [**Supported user account variables**](./Variables.md)
- [**Supported device variables**](./Variables.md)

## Supported user account variables

### User Variables

::Image[]{src="awvariables.png" signedSrc="awvariables.png" size="18" caption alt isUploading="false" sha initialPath="awvariables.png" githubPath="awvariables.png" position="flex-start"}

| **Variable key**               | **Value description**                                                                    |
| ------------------------------ | ---------------------------------------------------------------------------------------- |
| $\{department}                 | department attribute (requires Entra ID)                                                 |
| $\{edipi}                      | Electronic Data Interchange-Personal Identifier                                          |
| $\{managedAppleId}             | User's Managed Apple ID                                                                  |
| $\{sAMAccountName}             | sAMAccountName attribute (requires Active Directory)                                     |
| $\{userCN}                     | Common Name (CN) attribute extracted from the distinguished name (requires LDAP)         |
| $\{userDisplayName}            | Display name                                                                             |
| $\{userDN}                     | Distinguished Name (requires LDAP)                                                       |
| $\{userEmailAddressDomain}     | The domain part of the email address (part after '@')                                    |
| $\{userEmailAddressLocalPart}> | The local part of the email address (part before '@')                                    |
| $\{userEmailAddress}           | Email address                                                                            |
| $\{userFirstName}              | First name                                                                               |
| $\{userLastName}               | Last name                                                                                |
| $\{userLocale}                 | Locale                                                                                   |
| $\{userOU}                     | Organizational Unit (OU) attribute extracted from the distinguished name (requires LDAP) |
| $\{userREALM}                  | Kerberos Realm information (requires Active Directory)                                   |
| $\{userUIDDomain}              | The domain part of the login ID (the part after '@')                                     |
| $\{userUIDLocalPart}           | The local part of the login ID (the part before '@')                                     |
| $\{userUID}                    | Login ID (email address format)                                                          |
| $\{userUPN}                    | userPrincipalName attribute (requires Active Directory)                                  |

## Supported device variables

Use device variables to specify information about a mobile device.

### Device Variables

![](Resources/Images/VariableSubstitution.png)

| **Variable key**                 | **Value description**                                                    |
| -------------------------------- | ------------------------------------------------------------------------ |
| $\{clientLastCheckin}            | Date client last checked-in (most recent checkin - either MDM or Client) |
| $\{deviceAltSN}                  | Alternative Serial Number                                                |
| $\{deviceClientDeviceIdentifier} | Identifier used by the client application                                |
| $\{deviceGUID}                   | Globally unique device identifier                                        |
| $\{deviceIccIdentifier}          | ICCID                                                                    |
| $\{deviceIMEI2}                  | IMEI2                                                                    |
| $\{deviceIMEI}                   | IMEI                                                                     |
| $\{deviceIMSI}                   | IMSI                                                                     |
| $\{deviceLastCheckin}            | Date device last checked-in (most recent checkin - either MDM or Client) |
| $\{deviceMdmChannelId}           | Internal device identifier                                               |
| $\{deviceMdmDeviceIdentifier}    | Identifier used for MDM                                                  |
| $\{deviceMEIdentifier}           | MEID                                                                     |
| $\{deviceModel}                  | Model                                                                    |
| $\{deviceName}                   | Device name                                                              |
| $\{devicePhoneNumber}            | Device phone number                                                      |
| $\{devicePK}                     | Cluster unique device identifier                                         |
| $\{deviceSN}                     | Serial Number                                                            |
| $\{deviceUDID}                   | iOS UDID                                                                 |
| $\{deviceWifiMacAddress}         | Wi-Fi MAC Address                                                        |

### Email template variables

| **Variable key**         | **Value description** |
| ------------------------ | --------------------- |
| $\{policyMessageContent} | Email body            |
| $\{policyMessageTitle}   | Email subject         |

### Time stamp variables

| **Variable key** | **Value description**                            |
| ---------------- | ------------------------------------------------ |
| $\{timestampMS}  | Current timestamp (milliseconds since the epoch) |

### Policy template variables

| **Variable key**             | **Value description**                                                                         |
| ---------------------------- | --------------------------------------------------------------------------------------------- |
| $\{nameOfPolicy}             | Policy name violated                                                                          |
| $\{nextAction}               | Next Tiered Compliance Action (different than wait and retire) to be taken after send message |
| $\{nonComplianceTime}        | Count of days device has been in non-compliant state                                          |
| $\{policyViolationFirstTime} | Time stamp when policy violation was first triggered (UTC DD-MM-YYYY format)                  |
| $\{ruleConditions}           | Rule definition (query string the way it appears now)                                         |

**Related topics:**
