---
title: Certificate configuration
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

A certificate configuration identifies a certificate to be distributed to devices. Certificates enable devices to establish trust with server and network resources. Starting with release 76 we support only v3 certificates.

As an administrator, you can now generate Ivanti Neurons for MDM certificate for smart card logon and custom object IDs (OIDs). You can generate certificates for the following authentication options:

- Client Authentication - enabled by default
- IPSEC – optional, admin can enable
- Smart Card Logon – optional, admin can enable
- Custom OIDs - optional, admin can enable

This feature is only applicable for the following certificate authorities (CA):

- Local Certificate Authority
- Intermediate Certificate Authority
- External Certificate Authority - configure the application policies of CA template in NDES server to support IPSEC , Smart Card Logon, and custom OIDs
- On-premise SCEP Certificate Authority

## Distributing the configuration

Starting from Ivanti Neurons for MDM release 91, global administrators can delegate space administrators to edit the Certificate Configuration for All Devices and for the Custom distribution option. For the certificate config, you can optionally select the Allow this configuration to be available in all Spaces option. This option makes  Certificate config available to all Spaces and can be used in  Exchange, Wifi, VPN, Per-App VPN  and any other applicable configurations. This option can be used in scenarios where certificate config is only needed to be distributed to devices (in non default Spaces) as part of associated configurations and not to be distributed as an individual configuration.

Procedure

1. Enter a name in the Name field.
2. Upload the certificate file.
3. Click **Next**.
4. Select the **Enable this configuration** option.
5. Select one of the following distribution options:\* **All Devices**. Select one of the following options:- **Do not apply to other spaces**.
   - **Apply to devices in other Spaces**.\* Select **Allow Space Admin to Edit the Distribution** check box to allow the delegated space administrators to edit the distribution for the specific space.
   - **No Devices** (default)
   - **Custom** Select one of the following options:\* **Do not apply to other spaces**.
     - **Apply to devices in other Spaces**.\* Select **Allow Space Admin to Edit the Distribution** check box to allow the delegated space administrators to edit the distribution for the specific space.Irrespective of spaces, the certificate configuration can be configured to all spaces, distributed to all devices, and applied to all devices in other device spaces.
6. Click **Done**.

## Certificate settings

As an administrator, you can configure on-premise non-SCEP certificate authority.

**Procedure**

1. Log in to the Ivanti Neurons for MDM administrator portal.
2. Go to **Admin** > **Infrastructure** > **Certificate Management** > **Certificate Authority**.
3. Click **+Add**. The following options are listed:\* **Create the local certificate authority provided by Ivanti Neurons for MDM**
   - **Sign Ivanti Neurons for MDM's local CA with your own existing CA**.
   - **Connect to a publicly-trusted Cloud Certificate Authority**.
   - **Connect an on-premises SCEP Certificate Authority**.
   - **Connect an on-premises non-SCEP Certificate Authority**.
4. Complete the following fields as relevant:

| **Setting**                | What To Do                                                           |
| -------------------------- | -------------------------------------------------------------------- |
| Name                       | Enter a name that identifies this configuration.                     |
| URL                        | OpenTrust CA URL that the administrator must procure from OpenTrust. |
| Password                   | Enter password for the Authentication Certificate                    |
| Authentication Certificate | Accepts .p12 file format that is provided by OpenTrust/ IDnomic.     |
| TLS CA Certificate Chain   | Accepts PEM file format that is provided by OpenTrust/ IDonomic.     |
| Click **Done**.            |                                                                      |

After you configure on-premise non-SCEP certificate authority you must create the identity certificate. Based on the profile ID fill all the mandatory fields to complete the setup.

A notification is generated when SCEP CA Certificate generation fails due to the following two reasons and the Stage 2 timeout is reached:

1. Connector is not reachable
2. CA server is not reachable
