---
title: Per-app VPN Configuration
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

**License:**&#x53;ilver

**Applicable to:** iOS, watchOS, and visionOS devices

A Per-app VPN configuration defines the settings for virtual private network access for the following specific apps:

- [**Per-app VPN settings**](./Per-app_VPN_Configuration.md)
- [**Psec (Cisco)**](./Per-app_VPN_Configuration.md)
- [**Cisco AnyConnect**](./Per-app_VPN_Configuration.md)
- [**Juniper SSL**](./Per-app_VPN_Configuration.md)
- [**NetMotion VPN**](./Per-app_VPN_Configuration.md)
- [**F5 SSL**](./Per-app_VPN_Configuration.md)
- [**SonicWALL Mobile Connect**](./Per-app_VPN_Configuration.md)
- [**Aruba VIA**](./Per-app_VPN_Configuration.md)
- [**Custom SSL**](./Per-app_VPN_Configuration.md)
- [**Palo Alto Networks GlobalProtect**](./Per-app_VPN_Configuration.md)
  Per-App VPN configuration is dependent on App configuration. Per-App VPN configuration is created during App Configuration setup. When Per-App VPN configuration is deleted or undistributed, App configuration malfunctions by disconnecting the App from the network.

## Distributing the configuration

Starting from Ivanti Neurons for MDM release 91, global administrators can delegate space administrators to edit the Per-App VPN Configuration for All Devices and for the Custom distribution option. For the Per-App VPN Configuration, you can optionally select the Allow this configuration to be available in all Spaces option.

The distribution changes are applicable only to the specific space. All other spaces continue to inherit the default space distribution settings.

Specify the configuration settings in the fields using the information from the following tables as applicable and then distribute the configuration:

For more information, see *Distributing the configuration* topic in [**Working with Configurations**](./Working_with_Configurations.md).

## Per-app VPN settings

| **Setting**                                                      | What To Do                                                                                                                                         |
| ---------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                                                             | Enter a name that identifies this configuration.                                                                                                   |
| Description                                                      | Enter a description that clarifies the purpose of this configuration.                                                                              |
| Connection Type                                                  | Select the type of VPN to configure.The remaining settings depend on this selection.                                                               |
| Enable VPN On Demand                                             | Select to use this configuration for domains and host names that establish a VPN on demand.                                                        |
| Enable iOS Rules(Applicable if Enable VPN On Demand is selected) | For iOS and macOS, you can set up:\* Network rules that allow or disallow connections to, and allow or ignore, the networks that evaluate as true. |

- Connection rules allow when needed, or never allow, connections to the networks that evaluate as true.For network rules, you can specify the following types of parameters:\* DNS Domain Match
- DNS Server Address Match
- SSID Match
- URL String Probe
- Interface Type MatchFor connection rules, you can specify the following types of parameters:\* DNS Domain Match
- DNS Server Address Match
- SSID Match
- URL String Probe
- Interface Type Match
- Domains
- DNS Server
- URL Probe |
  \| On demand match app enabled                                      | Select to enable the per-app VPN on demand.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| Enable 5G network slicing                                        | Select **DNN** (Data Network Name provided by network provider) to tunnel, targeting to the specific cellular slice VPN.Select **App Category** (provided by network provider), to identify the type of cellular slice to be tunneled.                                                                                                                                                                                                                                                                                                                                                                                                             |
  \| **Domains**                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Safari Domains (iOS)                                             | An array whose entries must each specify a domain that triggers the VPN connection in Safari. Each entry is in the format [**www.apple.com**](http://www.apple.com).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| **iOS 14.0+ and macOS 11.0+**                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Associated Domains                                               | Specify one or more associated domains. Connections to servers within one of these domains are associated with the per-app VPN.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Excluded Domains                                                 | Specify one or more excluded domains. Connections to servers within one of these domains are excluded from the per-app VPN.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| **iOS 13+ and macOS 10.15+**                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Mail Domains                                                     | Click **+ Add** to enter one or more domains that will trigger this VPN connection in Mail. Each entry is in the format [**www.apple.com**](http://www.apple.com).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  \| Contacts Domains                                                 | Click **+ Add** to enter one or more domains that will trigger this VPN connection in Contacts. Each entry is in the format [**www.apple.com**](http://www.apple.com).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| Calendar Domains                                                 | Click **+ Add** to enter one or more domains that will trigger this VPN connection in Calendar. Each entry is in the format [**www.apple.com**](http://www.apple.com).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| **iOS 9 and later**                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Provider Type (iOS 9+)                                           | Select one of the following tunnel provider:\* app-proxy - tunnels traffic at the app layer. See [**Apple documentation**](https://developer.apple.com/documentation/networkextension/app_proxy_provider) for an overview of App Proxy Provider.
- packet-tunnel - tunnels traffic at the IP layer. See [**Apple documentation**](https://developer.apple.com/documentation/networkextension/packet_tunnel_provider) for an overview of Packet Tunnel Provider.                                                                                                                                                                                             |

### IPsec (Cisco)

| **Setting**            | What To Do                                                                                                                                                                                                                     |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server                 | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account                | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Machine Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential             | Select the identity certificate to use.                                                                                                                                                                                        |
| Include User PIN       | Select to prompt the user for a PIN.                                                                                                                                                                                           |
| Proxy Setup            | Select **Manual** or **Automatic** to configure a proxy.**If you select Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.**If you select Automatic,** then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Cisco AnyConnect

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Group               | Enter the group to use to authenticate the connection.                                                                                                                                                                         |
| User Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential          | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual**, then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic**, then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Juniper SSL

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Realm               | Enter the authentication realm to be used for authenticating the connection.                                                                                                                                                   |
| Role                | Enter the authentication role to be used for authenticating the connection.                                                                                                                                                    |
| User Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential          | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual**, then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic**, then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### NetMotion VPN

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| User Authentication | **Certificate** is the user authentication method to use. The following field is available:**Credential**: Select the identity certificate to use. User provided certificates are supported only for iOS devices.              |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy.Select the following options:\* Enable VPN On Demand - Add domains or host names that establish a VPN on demand.
- Enable iOS rules.
- On demand match app enabled. |
  \| Safari Domains           | Click **+ Add** to add Safari domains.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| Provider Type (iOS 9.0+) | **packet-tunnel** is selected as the tunnel provider type by default.See [**Apple documentation**](https://developer.apple.com/documentation/networkextension/packet_tunnel_provider) for an overview of Packet Tunnel Provider.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

### F5 SSL

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| User Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential          | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual**, then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic**, then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### SonicWALL Mobile Connect

| **Setting**           | What To Do                                                                                                                                                                                                                     |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server                | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account               | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Login Group or Domain | Enter the login group or domain to be used for authenticating the connection.                                                                                                                                                  |
| User Authentication   | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential            | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup           | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual**, then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic**, then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Aruba VIA

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| User Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential          | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual**, then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic**, then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Custom SSL

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Identifier          | Enter the identifier for this custom SSL VPN in reverse DNS format (such as com.mycompany.myserver).                                                                                                                           |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Custom Data         | Enter the key-value pairs that define the custom data for this VPN.                                                                                                                                                            |
| User Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential          | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual**, then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic**, then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |
  \| (iOS 9.0+) Include ProviderType in main and sub VPN dictionary | Choose to include the provider type while generating a plist (predefined configuration file).                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  \| Provide bundle identifier                                      | Enter the bundle identifier for the VPN provider. You can maintain multiple apps Config for the same app with different Provider Bundle Identifiers.                                                                                                                                                                                                                                                                                                                                                                                                                     |

### Palo Alto Networks GlobalProtect

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.                                                                                                                                                           |
| Custom Data         | Enter the key-value pairs that define the custom data for this VPN.                                                                                                                                                            |
| User Authentication | Certificate is the user authentication method.Select an identity certificate to use in the **Credential** field.                                                                                                               |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual**, then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic**, then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

Type $ to see a list of supported [**variables**](./Variables.md), if available, for this field.

**Related topics**:
