---
title: Encrypted DNS
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

**License:** Gold

**Applicable to:**

- iOS 14.0 or supported newer versions.
- macOS 11.0 or supported newer versions.
- visionOS 1.1 or supported newer versions.

Configure Encrypted DNS that will allow you to enhance security without needing to configure VPN.

This section contains the following topics:

- [**Encrypted DNS configuration**](./Encrypted_DNS.md)
- [**Encrypted DNS configuration settings**](./Encrypted_DNS.md)

## Encrypted DNS configuration

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **DNS** in the search field, and then click the **Encrypted DNS** configuration.
4. Enter a name and describe the configuration.
5. Enter the [**Encrypted DNS configuration settings**](./Encrypted_DNS.md).
6. Click **Next**.
7. Select the **Enable this configuration** option.
8. Select one of the following distribution options:\* All Devices
   - No Devices (default)
   - Custom
9. Click **Done**.

## Encrypted DNS configuration settings

Use the settings in the following table to configure Encrypted DNS. For more information about these settings, see [**Apple documentation**](https://developer.apple.com/documentation/devicemanagement/dnssettings).

| **Setting**      | **Description**                                                                                                                  |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **DNS Settings** | A dictionary that defines a configuration for an encrypted DNS server.                                                           |
| DNS Protocol     | Specify the encrypted transport protocol used to communicate with the DNS server. Select one of the following protocols:\* HTTPS |

- TLS                                                                                                                                                                                                                                                                                                          |
  \| Server URL                                 | The URI template of a DNS-over-HTTPS server, as defined in RFC 8484. This URL must use the https\:// scheme, and the hostname or address in the URL will be used to validate the server certificate. If no Server Addresses are provided, the hostname or address in the URL will be used to determine the server addresses. This key must be present only if the DNS Protocol is HTTPS.                                                       |
  \| Server Addresses                           | An unordered list of DNS server IP address strings. These IP addresses can be a mixture of IPv4 and IPv6 addresses.Click **Add** to add one or more server addresses.                                                                                                                                                                                                                                                                          |
  \| Supplemental Match Domains                 | A list of domain strings used to determine which DNS queries will use the DNS server. If this array is not provided, all domains will use the DNS server.Click **Add** to add one or more domains.                                                                                                                                                                                                                                             |
  \| Prohibit users from disabling DNS Settings | Prohibits users from disabling DNS settings. This key is only available on supervised devices.                                                                                                                                                                                                                                                                                                                                                 |
  \| **Demand Rules**                           | An array of rules defining the DNS settings. If rules are not present, the system always applies the DNS settings.Click **+ Add Demand Rules** to add one or more sets of demand rules.                                                                                                                                                                                                                                                        |
  \| Network                                    | The action to take if this dictionary matches the current network. Select one of the following actions:\* **Connect:** Apply DNS Settings when the dictionary matches.
- **Disconnect:** Do not apply DNS Settings when the dictionary matches.
- **Evaluate Connection:** Apply DNS Settings with per-domain exceptions when the dictionary matches.                                                                                           |
  \| Evaluate Connection                        | This network option has the following settings:\* **Domain Action** - The DNS settings behavior for the specified domains. Select one of the following actions:- **Never Connect** - Do not use the DNS Settings for the specified domains.
  - **Connect if Needed&#x20;**- Allow using the DNS Settings for the specified domains.
- **Domains** - The domains for which this evaluation applies. Click **+ Add** to add one or more domains. |
  \| **Rules**                                  | Click **+ Add** to add one or more rules to match the following parameters with the corresponding specified values.                                                                                                                                                                                                                                                                                                                            |
  \| DNS Domain Match                           | An array of domain names. This rule matches if any of the domain names in the specified list matches any domain in the device’s search domains list.                                                                                                                                                                                                                                                                                           |
  \| DNS Server Address Match                   | An array of IP addresses. This rule matches if any of the network’s specified DNS servers match any entry in the array.                                                                                                                                                                                                                                                                                                                        |
  \| SSID Match                                 | An array of SSIDs to match against the current network. If the network is not a Wi-Fi network or if the SSID does not appear in this array, the match fails.Omit this key and the corresponding array to match against any SSID.                                                                                                                                                                                                               |
  \| Interface Type Match                       | An interface type. If specified, this rule matches only if the primary network interface hardware matches the specified type. Select one of the following types:\* Ethernet
- WiFi
- Cellular                                                                                                                                                                                                                                                   |
  \| URL String Probe                           | A URL to probe. If this URL is successfully fetched (returning a 200 HTTP status code) without redirection, this rule matches.                                                                                                                                                                                                                                                                                                                 |
