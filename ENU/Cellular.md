---
title: Cellular
createdAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:32 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** iOS 7.0+ and watchOS 10.0+

This section contains the following topics:

- [**Cellular settings for Default APN**](./Cellular.md)
- [**Cellular settings for Data APNs**](./Cellular.md)
- [**Controlling cellular access while roaming**](./Cellular.md)
- [**Controlling cellular access**](./Cellular.md)

A cellular configuration sets up the cellular profile for a device. Configure the cellular network settings on devices running with iOS 7.0+ or watchOS 10.0+. Some companies have contracts with their cellular operators that grant them access to a unique Access Point Name (APN) for remote network access or for special billing plans. Consult your cellular operator for configuration parameters.

- No more than one cellular profile can be installed at any time.
- A cellular profile cannot be installed if an [**APN profile**](./APN_Configuration.md) is already installed.

You can configure cellular settings for the following APN types from the **Configured APN Types** dropdown box:

- Default & Data APNs
- Default APNs
- Data APNs

For all the configurations, enter a name that identifies the configuration and an optional description.

## Cellular settings for Default APN

| **Default APN Settings** | What To Do                                                                                                          |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| APN Name                 | Enter the name for the corresponding access point. The name is generally defined by the operator providing service. |
| APN Authentication Type  | (Optional) Select one of the following:\* CHAP (challenge handshake authentication protocol)                        |

- PAP (password authentication protocol) |
  \| User Name                | (Optional) Enter a user name to be used for authentication.                                                                          |
  \| Password                 | (Optional) Enter a password to be used for authentication.                                                                           |

## Cellular settings for Data APNs

| **Data APN Settings**   | What To Do                                                                                                          |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------- |
| APN Name                | Enter the name for the corresponding access point. The name is generally defined by the operator providing service. |
| APN Authentication Type | (Optional) Select one of the following:\* CHAP (challenge handshake authentication protocol)                        |

- PAP (password authentication protocol) |
  \| User Name                                 | (Optional) Enter a user name to be used for authentication.                                                                          |
  \| Password                                  | (Optional) Enter a password to be used for authentication.                                                                           |
  \| Proxy Server                              | Specify the proxy server.                                                                                                            |
  \| Proxy Server Port                         | Specify the proxy server port.                                                                                                       |
  \| 10.3+                                     |                                                                                                                                      |
  \| Allowed Protocol Mask                     | Select IPv4, IPv6, or Both.                                                                                                          |
  \| Allowed Protocol Mask in Domestic Roaming | Select IPv4, IPv6, or Both.                                                                                                          |
  \| Allowed Protocol Mask in Roaming          | Select IPv4, IPv6, or Both.                                                                                                          |

## Controlling cellular access while roaming

You can limit the access of some or all of the managed apps to cellular data while the device is in a roaming state.

**Procedure**

1. Go to the **Configurations** tab in the Ivanti Neurons for MDM main navigation menu.
2. Click **+Add**
3. Enter **Network** in the search field, and then click the **Network Usage** configuration.
4. Select the **Disallow for all managed apps** checkbox to block managed apps from accessing cellular data when roaming or at all times.
5. Leave the checkbox unselected to be able to specify the managed apps by name or bundle ID to block from receiving cellular data.
6. Use the pulldown menus in the Apps field to search for an app by name or by bundle ID.

## Controlling cellular access

You can  limit the access of some or all of the managed apps  to cellular data at any time. The apps can still be used on a limited basis, but they will not have access to cellular data.

**Procedure**

1. Go to the **Configurations** tab in the Ivanti Neurons for MDM main navigation menu.
2. Click **+Add**
3. Enter **Network** in the search field, and then click the **Network Usage** configuration.
4. Select the **Disallow for all managed apps** checkbox to block managed apps from accessing cellular data at any time.
5. Optionally,  leave the checkbox unselected to specify the managed apps to block from receiving cellular data.
6. Use the pulldown menus in the Apps field to search for an app by name or by bundle ID.
