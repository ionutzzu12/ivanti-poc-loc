---
title: VPN Configuration
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:**

- Android (Deprecated for Android Enterprise devices. You need to use the Managed Configuration for specific VPN from the App Catalog.)
- Windows
- iOS
- macOS
- visionOS

A VPN configuration defines the settings for virtual private network access.

Delegation with custom distribution option is available for this configuration. For more information, see *Distributing the configuration* topic in [**Working with Configurations**](./Working_with_Configurations.md).

**Procedure**

1. Go to **Configurations** > **+Add**.
2. Select the  **VPN** configuration.
3. Enter a **Name** for the configuration.
4. Enter a description.
5. Configure the VPN settings as per the following descriptions.
6. (iOS 9.0+ Only) In the Match Domains section, click **+ Add** to enter one or more matching domains (example: company.com). Proxy connection is used when the domain is one of these specified domains.
7. Click **Next**.
8. (macOS only) In the Distribute page, select one of the following distribution options:\* Device channel - the configuration is effective for all users on a device, which is the typical option.
   - User channel - the configuration is effective only for the currently registered user on a device.
9. Select the remaining distribution options for this configuration.
10. Click **Done**.

## VPN settings

| **Setting**     | What To Do                                                                           |
| --------------- | ------------------------------------------------------------------------------------ |
| Name            | Enter a name that identifies this configuration.                                     |
| Description     | Enter a description that clarifies the purpose of this configuration.                |
| Connection Type | Select the type of VPN to configure.The remaining settings depend on this selection. |

The protocols and their settings are listed as follows:

- [**L2TP**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- [**PPTP**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- [**IPsec (Cisco)**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- [**Cisco AnyConnect**](./VPN_Configuration.md) (Supported on Ivanti Go)
- [**Juniper SSL**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- [**NetMotion VPN**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- Pulse Secure (Supported on Ivanti Go)
- [**F5 SSL**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- [**SonicWALL Mobile Connect**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- [**Aruba VIA**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- [**Custom SSL**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- [**Palo Alto Networks GlobalProtect**](./VPN_Configuration.md) (Supported on Ivanti Go)
- [**KEv2 (Windows Only)**](./VPN_Configuration.md) (Not supported on Ivanti Go)
- [**IKEv2**](./VPN_Configuration.md) (Not supported on Ivanti Go)

### L2TP

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| User Authentication | Select the authentication method to use: **Password** or **RSA SecurID**.                                                                                                                                                      |
| Shared Secret       | Enter the shared secret passcode if one is necessary for initiating the connection.                                                                                                                                            |
| Send All Traffic    | Select this option to use this connection for all network traffic. This option helps protect data from being compromised, particularly on public networks.                                                                     |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### PPTP

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| User Authentication | Select the authentication method to use: **Password** or **RSA SecurID**.                                                                                                                                                      |
| Encryption Level    | Select a level of data encryption for the connection: **None, Automatic**, or **Maximum (128-bit)**.                                                                                                                           |
| Send All Traffic    | Select this option to use this connection for all network traffic. This option helps protect data from being compromised, particularly on public networks.                                                                     |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### IPsec (Cisco)

| **Setting**               | What To Do                                                                                                                                                                                                                     |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server                    | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account                   | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Machine Authentication    | Select the authentication method to use: **Shared Secret/Group Name** or **Certificate**.                                                                                                                                      |
| Group Name                | Shared Secret/Group Name authentication.Specify the name of the group to use. If Hybrid Authentication is used, the string must end with â€œ\[hybrid]â€.                                                                      |
| Shared Secret             | Shared Secret/Group Name authentication.Enter the shared secret passcode.                                                                                                                                                      |
| Use Hybrid Authentication | Shared Secret/Group Name authentication.Select to specify hybrid authentication, i.e., server provides a certificate and the client provides a pre-shared key.                                                                 |
| Prompt for Password       | Shared Secret/Group Name authentication.Specify whether the user should be prompted for a password when connecting.                                                                                                            |
| Credential                | *Certificate authentication*Select the identity certificate to use.                                                                                                                                                            |
| Include User PIN          | *Certificate authentication*Select to prompt the user for a PIN.                                                                                                                                                               |
| Proxy Setup               | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional fields are available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Cisco AnyConnect

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Group               | Enter the group to use to authenticate the connection.                                                                                                                                                                         |
| User Authentication | Select the user authentication method to use: **Password** or **Certificate**.If you select **Certificate**, then the following field is available:**Credential**: Select the identity certificate to use.                     |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Juniper SSL

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Realm               | Enter the authentication realm to be used for authenticating the connection.                                                                                                                                                   |
| Role                | Enter the authentication role to be used for authenticating the connection.                                                                                                                                                    |
| User Authentication | Select the user authentication method to use: **Password** or **Certificate**.If you select **Certificate**, then the following field is available:**Credential**: Select the identity certificate to use.                     |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### NetMotion VPN

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| User Authentication | Select the user authentication method to use: **Password** or **Certificate**. If you select **Certificate**, then the following field is available:**Credential**: Select the identity certificate to use.                    |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### F5 SSL

| **Setting**         | What To Do                                                                                                                                                                                                             |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                  |
| Account             | Enter the user account to be used for authenticating the connection.                                                                                                                                                   |
| User Authentication | Enter the user authentication method to use: **Password** or **Certificate**.If you select **Certificate**, then the following field is available:**Credential**: Select the identity certificate to use.              |
| Proxy Setup         | Select Manual or Automatic to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### SonicWALL Mobile Connect

| **Setting**           | What To Do                                                                                                                                                                                                                     |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server                | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account               | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Login Group or Domain | Enter the login group or domain to be used for authenticating the connection.                                                                                                                                                  |
| User Authentication   | Select the user authentication method to use: **Password** or **Certificate**.If you select Certificate, then the following field is available:**Credential**: Select the identity certificate to use.                         |
| Proxy Setup           | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Aruba VIA

| **Setting**         | What To Do                                                                                                                                                                                                             |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                  |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                 |
| User Authentication | Select the user authentication method to use: **Password** or **Certificate**.If you select **Certificate**, then the following field is available:**Credential**: Select the identity certificate to use.             |
| Proxy Setup         | Select Manual or Automatic to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Custom SSL

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Identifier          | Enter the identifier for this custom SSL VPN in reverse DNS format (such as com.mycompany.myserver).                                                                                                                           |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Custom Data         | Enter the key-value pairs that define the custom data for this VPN.                                                                                                                                                            |
| User Authentication | Select the user authentication method to use: **Password** or **Certificate**.If you select Certificate, then the following field is available:**Credential**: Select the identity certificate to use.                         |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Palo Alto Networks GlobalProtect

Not applicable to Android devices.

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.                                                                                                                                                           |
| Custom Data         | Enter the key-value pairs that define the custom data for this VPN.                                                                                                                                                            |
| User Authentication | Select the user authentication method to use: **Password** or **Certificate**.If you select Certificate, then the following field is available:**Credential**: Select the identity certificate to use.                         |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### IKEv2 (Windows Only)

| **Setting** | **What To Do**                                                                                                                                                                                                                 |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server      | Enter the host name or IP address of the VPN server.                                                                                                                                                                           |
| Proxy Setup | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### IKEv2

| **Setting**          | **What To Do**                                                         |
| -------------------- | ---------------------------------------------------------------------- |
| **Server**           | Enter the host name or IP address of the VPN server.                   |
| **Local Identifier** | Identifier of the IKEv2 client in one of the following formats:\* FQDN |

- UserFQDN
- Address
- ASN1DN                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| Remote Identifier                                       | Remote identifier in one of the following formats:\* FQDN
- UserFQDN
- Address
- ASN1DN                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
  \| Machine Authentication                                  | Available only if **Enable EAP** is not selected.Select one of the following:\* Certificate
- Shared Secret                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| EAP Authentication                                      | Available only if **Enable EAP** is selected.Select one of the following:\* Certificate
- Username/Password                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| Shared Secret                                           | Available only if Shared Secret was selected for Machine Authentication. Enter the shared secret for the connection.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| Credential                                              | Available only if Certificate was selected for Machine Authentication. Select the certificate to use. this certificate will be sent out for IKE client authentication. If extended authentication is used, this certificate can be used for EAP-TLS.                                                                                                                                                                                                                                                                                                                 |
  \| Enable EAP                                              | Select to enable extended authentication.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  \| Account                                                 | Available only if Username/Password was selected for EAP Authentication. Enter the account ID for the VPN server.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Password                                                | Available only if Username/Password was selected for EAP Authentication. Enter the password for the VPN server.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
  \| Dead Peer Detection Interval                            | Select one of the following options:\* None (Disable)
- Low (keepalive sent every 1 hour)
- Medium (keepalive sent every 30 minutes)
- High (keepalive sent every 10 minutes)                                                                                                                                                                                                                                                                                                                                                                                         |
  \| Server Certificate Issuer Common Name                   | (Optional) - Common name of a server certificate issuer, causes the IKE server to send a certificate request based on the certificate issuer to the server.                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| Server Certificate Common Name                          | (Optional) - Common name of a server certificate used to validate the certificate sent by the IKEv2 server.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| Use IP4 and IP6 subnets attributes                      | (Optional) Select to use IP4 and IP6 subnets attributes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
  \| Enable IKEv2 Mobility and Multihoming Protocol (MOBIKE) | (Optional) The default setting is 0. MOBIKE (The ability to support multi-homed mobile devices when connected to both Wi-Fi and cellular links with multiple IP addresses) is enabled. It is enabled by default. Set to 1 to disable MOBIKE.                                                                                                                                                                                                                                                                                                                         |
  \| Enable **Perfect Forward Secrecy (PFS)**                | (Optional) When set to 1 it enables PFS for IKEv2 connections. The default setting is 0.                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
  \| Enable **IKEv2 redirect**                               | (Optional) The default setting is 0. The IKEv2 connection is redirected if a redirect request is received from the server. It is enabled by default. Set to 1 to disable IKEv2 redirect.                                                                                                                                                                                                                                                                                                                                                                             |
  \| Enable **NAT keepalive**                                | Enables the Network Address Translation keepalive that prevents the deletion of NAT entries in the absence of any traffic when there is NAT between IKE peers.                                                                                                                                                                                                                                                                                                                                                                                                       |
  \| **NAT keepalive interval**                              | If NAT keepalive is enabled, this is the time in seconds that keepalive packets will be sent for the device.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
  \| **PPK**                                                 | Enter the Post-quantum Pre-shared key (PPK) with VPN servers that support RFC 8784. If this key is present, the PPK Identifier must be present.                                                                                                                                                                                                                                                                                                                                                                                                                      |
  \| **PPK Identifier**                                      | Enter the PPK identifier.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  \| **PPK Mandatory**                                       | Select one of the following drop-down options:\* **Mandate**: The VPN connection will successfully establish if the server supports RFC 8784 or if it accepts the PPK identifier specified in the PPK Identifier.
- **Non-Mandate**: The VPN connection will fail to establish if the server does not support RFC 8784 or it does not accept the PPK identifier specified in the PPK Identifier.                                                                                                                                                                      |
  \| **Encryption Algorithm**                                | Select one of the following options:\* **DES**
- **3DES**
- **AES-128**
- **AES-256** (Default)
- **AES-128 GCM**
- **AES-256 GCM**                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Integrity Algorithm                                     | Select one of the following options:\* **SHA2-256** (Default)
- **SHA2-384**
- **SHA2-512**                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| Diffie Hellman Group                                    | Select one of the following options:\* **1**
- **2** (Default)
- **5**
- **14**
- **15**
- **16**
- **17**
- **18**                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| Lifetime In Minutes                                     | Enter the SA lifetime (re-key interval) in minutes. Valid values are 10 through 1440.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \| Proxy Setup                                             | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\*
- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

\*Type $ to see a list of supported [**variables**](./Variables.md), if available, for this field.
