---
title: Android APN Settings Configuration
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

The Android APN Settings Configurations allow you to set the Access Point Name (APN) settings required on devices on a public network. This configuration is applicable to Android Enterprise Work Managed Devices and Managed Devices with Work Profile on Company Owned Device (on Android version 9.0 or supported newer versions).

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Configuration**&#xNAN;**> +Add**.
:::

:::WorkflowBlockItem
Select **Android APN Settings** configuration.
:::

:::WorkflowBlockItem
Enter a name for the configuration.
:::

:::WorkflowBlockItem
Enter a description.
:::

:::WorkflowBlockItem
In the Configuration Setup section, configure the following options:
:::

:::WorkflowBlockItem
| Setting               | Description                                                               |
| --------------------- | ------------------------------------------------------------------------- |
| **Entry Name**        | Type the name of the Access Point settings.                               |
| **Access Point Name** | Type the name of access point.                                            |
| **Access Point Type** | Select the type of access point from the following options:\* **Default** |

- **DUN**
- **IMS**
- **Emergency**
- MMS
- **HIPRI**
- **CBS**
- **MCX**
- **SUPL**
- **FOTA**
- **IA**                                                                                                                                   |
  \| **MVNO Type**                 | Select the type of Mobile Virtual network Operator from the following options:\* **None**
- **SPN**
- **IMSI**
- **GID**
- **ICCID**                                                                                                                                                                                 |
  \| **Bearer**                    | Select the type of bearer service used for data transmission from the following options:\* **1xRTT**
- **CDMA**
- **EDGE**
- **EHRPO**
- **EVDO**
- **EVDO A**
- **EVDO B**
- **GPRS**
- **GSM**
- **HSDPA**
- **HASP**
- **HSPAP**
- **HSUPA**
- **IDEN**
- **IWLAN**
- **LTE**
- **NR**
- **TD\_SCDMA**
- **UMTS** |
  \| **APN Protocol**              | Select the APN protocol required for the APN. The following are the available options:\* **None**
- **IPV4**
- **IPV6**
- **IPV4/IPV6**
- **NON\_IP**
- **PPP&#x20;**(Point-to-Point Protocol)
- **UNSTRUCTURED**                                                                                                    |
  \| **APN Roaming Protocol**      | Select the APN roaming protocol required for the APN. The following are the available options:\* **None**
- **IPV4**
- **IPV6**
- **IPV4/IPV6**
- **NON\_IP**
- **PPP&#x20;**(Point-to-Point Protocol)
- **UNSTRUCTURED**                                                                                            |
  \| **Enable/Disable APN**        | Turn ON the APN configuration.                                                                                                                                                                                                                                                                                      |
  \| **Carrier ID**                | Enter the numeric value of the Carrier ID.                                                                                                                                                                                                                                                                          |
  \| **Authentication Type**       | Select the type of authentication protocol from the following options:\* **None**
- **PAP** (Password Authentication Protocol)
- **CHAP** (Challenge-Handshake Authentication Protocol)
- **PAP or CHAP**                                                                                                            |
  \| **Username**                  | Enter the login username.                                                                                                                                                                                                                                                                                           |
  \| **Password**                  | Enter the login password.                                                                                                                                                                                                                                                                                           |
  \| **Confirm Password**          | Re-enter the password for confirmation.                                                                                                                                                                                                                                                                             |
  \| **Port Number**               | Enter the port number (numeric value between 1 to 65535).                                                                                                                                                                                                                                                           |
  \| **Proxy Address**             | Type the proxy address.                                                                                                                                                                                                                                                                                             |
  \| **Mobile Country Code**       | Enter the mobile country code.                                                                                                                                                                                                                                                                                      |
  \| **Mobile Network Code**       | Enter the mobile network code.                                                                                                                                                                                                                                                                                      |
  \| **MMS Proxy Address**         | Type the MMS proxy address.                                                                                                                                                                                                                                                                                         |
  \| **MMS Port Number**           | Enter the MMS port number (numeric value between 1 to 65535).                                                                                                                                                                                                                                                       |
  \| **MMS Server Address (mmsc)** | Type the MMS server address.                                                                                                                                                                                                                                                                                        |
  Click **Next**.
:::

:::WorkflowBlockItem
Select one of the following distribution options:
:::

:::WorkflowBlockItem
- **All Devices**
- No Devices (default)
- **Custom**
  Click **Done**.
:::
::::

You cannot add another APN configuration with same values for the following fields If there is an existing APN configuration with these values for the device:

- Mobile Country Code
- Mobile Network Code
- Access Point Name
- Proxy Address
- Port Number
- MMS Proxy Address
- MMS Port Number
- MMS Server Address
- Enable/Disable APN
- MVNO Type
- APN Protocol
- APN Roaming Protocol

The Android APN Settings Configuration overrides the APN settings if already configured in the device manually or by the nework operator.
