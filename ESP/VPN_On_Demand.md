---
title: VPN On Demand
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** iOS devices

A VPN On Demand configuration sets up access to a VPN server based on domains, host names, etc.

## VPN On Demand settings

| **Setting**                                                      | What To Do                                                                                                                                          |
| ---------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                                                             | Enter a name that identifies this configuration.                                                                                                    |
| Description                                                      | Enter a description that clarifies the purpose of this configuration.                                                                               |
| Connection Type                                                  | Select the type of VPN to configure.The remaining settings depend on this selection.                                                                |
| Enable VPN On Demand                                             | Select to use this configuration for domains and host names that establish a VPN on demand.                                                         |
| Enable iOS Rules(Applicable if Enable VPN On Demand is selected) | For iOS and macOS, you can set up:\* Network rules that allow or disallow connections to, and allow or ignore,  the networks that evaluate as true. |

- Connection rules allow when needed, or never allow, connections to the networks that evaluate as true.For network rules, you can specify the following types of parameters:\* DNS Domain Match
- DNS Server Address Match
- SSID Match
- URL String Probe
- Interface Type MatchFor connection rules, you can specify the following types of parameters:\* DNS Domain Match
- DNS Server Address Match
- SSID Match
- URL String Probe
- Interface Type Match
- Domain Name
- DNS Server
- URL Probe |
  \| Provider Type (iOS 9+)                                           | Select one of the following tunnel provider:\* app-proxy - tunnels traffic at the app layer. See [**Apple documentation**](https://developer.apple.com/documentation/networkextension/app_proxy_provider) for an overview of App Proxy Provider.
- packet-tunnel - tunnels traffic at the IP layer. See [**Apple documentation**](https://developer.apple.com/documentation/networkextension/packet_tunnel_provider) for an overview of Packet Tunnel Provider.                                                                                                                                                                                                  |
  \| EnforceRoutes                                                    | When enabled, the VPN's non-default routes overrides any locally defined routes.\* If IncludeAllNetworks is enabled, the system disregards the EnforceRoutes setting
- Available in iOS 14.2 and later.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| ExcludeLocalNetworks                                             | When enabled along with IncludeAllNetworks, all local network traffic routes outside of the VPN.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| IncludeAllNetworks                                               | When enabled, it routes all traffic through the VPN.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

The protocols and their settings are listed as follows:

- [**IPsec (Cisco)**](./VPN_On_Demand.md)
- [**Cisco AnyConnect**](./VPN_On_Demand.md)
- [**Juniper SSL**](./VPN_On_Demand.md)
- [**NetMotion VPN**](./VPN_On_Demand.md)
- [**F5 SSL**](./VPN_On_Demand.md)
- [**SonicWALL Mobile Connect**](./VPN_On_Demand.md)
- [**Aruba VIA**](./VPN_On_Demand.md)
- [**Custom SSL**](./VPN_On_Demand.md)
- [**Palo Alto Networks GlobalProtect**](./VPN_On_Demand.md)

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
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.**If you select Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.**If you select Automatic,** then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Juniper SSL

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Realm               | Enter the authentication realm to be used for authenticating the connection.                                                                                                                                                   |
| Role                | Enter the authentication role to be used for authenticating the connection.                                                                                                                                                    |
| User Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential          | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.**If you select Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.**If you select Automatic,** then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### NetMotion VPN

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| User Authentication | Certificate is the user authentication method.**Credential**: Select the identity certificate to use.                                                                                                                          |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.If you select **Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.If you select **Automatic,** then the following additional field is available:**Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### F5 SSL

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| User Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential          | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.**If you select Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.**If you select Automatic,** then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### SonicWALL Mobile Connect

| **Setting**           | What To Do                                                                                                                                                                                                                     |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server                | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account               | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Login Group or Domain | Enter the login group or domain to be used for authenticating the connection.                                                                                                                                                  |
| User Authentication   | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential            | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup           | Select **Manual** or **Automatic** to configure a proxy.**If you select Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.**If you select Automatic,** then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Aruba VIA

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| User Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential          | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.**If you select Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.**If you select Automatic,** then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Custom SSL

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Identifier          | Enter the identifier for this custom SSL VPN in reverse DNS format (such as com.mycompany.myserver).                                                                                                                           |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.\*                                                                                                                                                         |
| Custom Data         | Enter the key-value pairs that define the custom data for this VPN.                                                                                                                                                            |
| User Authentication | Only Certificate authentication is supported.                                                                                                                                                                                  |
| Credential          | Select the identity certificate to use.                                                                                                                                                                                        |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.**If you select Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.**If you select Automatic,** then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

### Palo Alto Networks GlobalProtect

| **Setting**         | What To Do                                                                                                                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Server              | Enter the IP address or host name for the VPN server.                                                                                                                                                                          |
| Account             | Enter the user account to be used for authenticating the connection.                                                                                                                                                           |
| Custom Data         | Enter the key-value pairs that define the custom data for this VPN.                                                                                                                                                            |
| User Authentication | Certificate is the user authentication method.Select an identity certificate to use in the **Credential** field.                                                                                                               |
| Proxy Setup         | Select **Manual** or **Automatic** to configure a proxy.**If you select Manual,** then the following additional fields are available:\* **Server and Port**: Enter the network address and port number for the proxy server.\* |

- **Authentication**: Enter a valid user name if one is required for connecting to the proxy.\*
- **Password**: Enter a valid password if one is required for connecting to the proxy.**If you select Automatic,** then the following additional fields are available:\* **Proxy Server URL**: Enter the fully-qualified URL for the proxy. |

Type $ to see a list of supported [**variables**](./Variables.md), if available, for this field.
