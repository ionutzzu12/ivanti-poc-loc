---
title: APN Configuration
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

An APN configuration sets up the cellular Access Point Name for the device. For iOS 7, use the [**Cellular configuration**](./Cellular.md), instead.

## APN settings

| **Setting**            | What To Do                                                                                                                |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Name                   | Enter a name that identifies this configuration.                                                                          |
| Description            | Enter a description that clarifies the purpose of this configuration.                                                     |
| Access Point Name      | Enter the name for the corresponding access point. The name is generally defined by the operator providing service.       |
| Access Point User Name | Enter a user name authorized for this access point.\*                                                                     |
| Access Point Password  | Enter the password corresponding to the user name entered.                                                                |
| Proxy Server and Port  | Enter the IP address or URL and the port number of the APN proxy.                                                         |
| EnableXLAT464          | Select the check box to enable the Access Point Name (APN). This option provides IPv4 services over an IPv6-only network. |

Type $ to see a list of supported [**variables**](./Variables.md), if available, for this field.
