---
title: Attributes
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

Use the Attributes page to do the following tasks:

- Manage the types of information you can record for users, devices, and apps.
- View the standard types of information that Ivanti Neurons for MDM tracks.

Custom user attributes include information such as Department or an internal ID. Each attribute has a corresponding variable that you can use to build groups or distribute configurations.

While creating user rule group criteria, if the custom attributes have a number value, Ivanti Neurons for MDM does not support integer operations.

## Creating custom attributes

You can create custom attributes from the Ivanti Neurons for MDM administrative portal.

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Log in to the Administrative Portal.
:::

:::WorkflowBlockItem
Navigate to **Admin** > **System** > **Attributes**.
:::

:::WorkflowBlockItem
Under **Custom Attributes**, click **+Add**
:::

:::WorkflowBlockItem
In the **Attribute Name** field, enter text that will represent the attribute.
:::

:::WorkflowBlockItem
The text you enter will be used to create the corresponding variable in the **Usage** field.

Select any the type of attribute from the following **Attribute Type** options.
:::

:::WorkflowBlockItem
- **User**
- **Device**
- **App**
- **IDP** (for more information, see [**User Provisioning with SCIM&#x20;**](./User_Provisioning_with_SCIM.md)or [**Connect Ivanti Neurons for MDM with Entra ID User Source**](./Connect_Ivanti_Neurons_for_MDM_with_Entra_ID_User_Source.md))
  If the Attribute type is Device, select one of the following **Data Type** options:- **Numeric**
- **Text**
:::

:::WorkflowBlockItem
Click **Add**.

The created custom user attribute is displayed under **Admin Added** section in the Attributes page.
:::
::::

The custom attributes combination $\{deviceattribute} + $\{custom-attribute} + $\{userattribute} + $\{Static String} is supported in any order.

## Renaming a custom attribute

Renaming a custom attribute will rename all references of that custom attribute that are used in the following entities:

- Custom Policy
- User group
- Device group
- App Distribution Filter
- Spaces

References of the custom attribute in any other entities such as configurations, invitation email templates, email and push messages in policy compliance actions, and so on will not be updated.

**Procedure**

1. Under **Admin Added**, click **+Edit** next to the attribute you want to rename.
2. In the **Attribute Name** field, enter a new name that will represent the attribute.
3. The text you enter will be used to create the corresponding variable in the **Usage** field.
   Click **Save**.

## Deleting a custom attribute

Deleting a custom attribute will remove its values from all the associated users or devices. It cannot be reversed.

Custom attributes cannot be deleted if the attribute is used in any of the following entities:

- Custom Policy
- User group
- Device group
- App Distribution Filter
- Spaces

Remove the custom attribute from the entities before attempting to delete the custom attribute.

If the attribute you want to delete does not have references to any of the above entities, clicking **Delete** next to the attribute will display a pop-up to confirm the action. Confirm the action and click **Delete**.

The field names of the following custom attributes are sorted in the applicable rule builders:

- Custom LDAP Attribute
- Custom User Attribute
- Custom Device Attribute
- Custom IdP Attribute
- Custom App Attribute

## Viewing the system attributes

System attributes are pre-defined attributes for you to use in your configurations as variables. The complete list is provided in the **System Attributes** section of the **Admin&#x20;**>**&#x20;System&#x20;**>**&#x20;Attributes** page. System attributes include the following types of attributes:

- User Attributes
- Device Attributes
- Email Template Attributes
- System Attributes
- Timestamp Attributes
- Entra ID Custom User Attributes
- Policy Attributes

## User attributes

Use user attributes to specify information about users.

| Key                            | Description                                                                              |
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

## Device attributes

Use device attributes to specify information about a mobile device.

| Key                              | Description                                                              |
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
|                                  | Phone Number 2                                                           |
|                                  | ICCID 2                                                                  |

When you create a custom attribute and refer this attribute in a Managed app config, If the attribute value is updated, the attribute referenced in the managed app config also gets updated and the managed app config will be re-pushed to the device.

When the Custom or Device attributes are updated and the configuration is pushed to a device, the Android Kiosk branding configuration should be updated as well.

## App attributes

Use app attributes to specify information about applications and create custom application groups.

| Key               | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| $\{appAdded}      | Date application was added to the AppCatalog                 |
| $\{appName}       | Name of the application                                      |
| $\{appOsPlatform} | Application operating system                                 |
| $\{appPackageId}  | Application bundle or package ID                             |
| $\{appSource}     | Describes the source from where the application was imported |
| $\{IsVpp}         | Describes if an iOS or macOS application is VPP or not       |

### Email template attributes

| Key                      | Description   |
| ------------------------ | ------------- |
| $\{policyMessageContent} | Email body    |
| $\{policyMessageTitle}   | Email subject |

### Time stamp attributes

| Variable Key    | Description                                      |
| --------------- | ------------------------------------------------ |
| $\{timestampMS} | Current timestamp (milliseconds since the epoch) |

### Policy template attributes

| Key                          | Description                                                                                   |
| ---------------------------- | --------------------------------------------------------------------------------------------- |
| $\{nameOfPolicy}             | Policy name violated                                                                          |
| $\{nextAction}               | Next Tiered Compliance Action (different than wait and retire) to be taken after send message |
| $\{nonComplianceTime}        | Count of days device has been in non-compliant state                                          |
| $\{policyViolationFirstTime} | Time stamp when policy violation was first triggered (UTC DD-MM-YYYY format)                  |
| $\{ruleConditions}           | Rule definition (query string the way it appears now)                                         |

Related topics:

- [**Assigning Custom Attributes to Users**](./Assigning_Custom_Attributes_to_Users.md)
- [**Assigning Custom Attributes to Devices**](./Assigning_Custom_Attributes_to_Devices.md)
- [**Removing Custom Attributes from Users**](./Removing_Custom_Attributes_from_Users.md)
- [**Removing Custom Attributes from Devices**](./Removing_Custom_Attributes_from_Devices.md)
