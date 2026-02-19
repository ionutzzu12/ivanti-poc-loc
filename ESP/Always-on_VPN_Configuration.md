---
title: Always-on VPN Configuration
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**License:**

- Gold for Android Enterprise
- Silver for iOS

The Always-on VPN configuration ensures that users are automatically connected to VPN (when available) without needing to take any action. This feature requires Android 7.0 + or iOS 8+, as well as a VPN provider that supports the IKEv2 protocol.

## Always-on VPN settings for Android

Always-on VPN configuration is sent to Android Enterprise devices with Android 7.0 +. On Managed device with Work Profile (Android 8.0+), the VPN configuration is applied in the Work Profile.

When a device is deployed in **COSU** mode with **AMA** as Device Enrollment type, and if an app with **Always-on** configuration is pushed to the device, then the **Always-on** configuration will also get pushed to the device.

To enable this configuration, select an app from the App Catalog or enter a package name.

## Always-on VPN settings for iOS

| Setting                                              | What To Do                                                                                                                                               |
| ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                                                 | Enter a name that identifies this configuration.                                                                                                         |
| Description                                          | Enter a description that clarifies the purpose of this configuration.                                                                                    |
| Use same tunnel configuration for Cellular and Wi-Fi | Select to define one server-identifier pair for VPN connections, regardless of whether the connection is established over a cellular or a Wi-Fi network. |
| Server                                               | Enter the host name or IP address of the VPN server.                                                                                                     |
| Local Identifier                                     | Identifier of the IKEv2 client in one of the following formats:\* FQDN                                                                                   |

- UserFQDN
- Address
- ASN1DN                                                                                                                                                  |
  \| Remote Identifier                                                     | Remote identifier in one of the following formats:\* FQDN
- UserFQDN
- Address
- ASN1DN                                                                                                                                                               |
  \| Enable EAP                                                            | Select to enable extended authentication.                                                                                                                                                                                                            |
  \| Machine Authentication                                                | Available only if Enable EAP is not selected.Select one of the following:\* Certificate
- Shared Secret                                                                                                                                               |
  \| EAP Authentication                                                    | Available only if Enable EAP is selected.Select one of the following:\* Certificate
- Username/Password                                                                                                                                               |
  \| Shared Secret                                                         | Available only if Shared Secret was selected for Machine Authentication. Enter the shared secret for the connection.                                                                                                                                 |
  \| Credential                                                            | Available only if Certificate was selected for Machine Authentication. Select the certificate to use. this certificate will be sent out for IKE client authentication. If extended authentication is used, this certificate can be used for EAP-TLS. |
  \| Account                                                               | Available only if Username/Password was selected for EAP Authentication. Enter the account ID for the VPN server.                                                                                                                                    |
  \| Password                                                              | Available only if Username/Password was selected for EAP Authentication. Enter the password for the VPN server.                                                                                                                                      |
  \| Dead Peer Detection Interval                                          | Select one of the following:\* None (Disable)
- Low (keepalive sent every 1 hour)
- Medium (keepalive sent every 30 minutes)
- High (keepalive sent every 10 minutes)                                                                                 |
  \| Encryption Algorithm                                                  | Select one of the following:\* DES
- 3DES
- AES-128
- AES-256
- AES-128-GCM
- AES-256-GCM
- ChaCha20-Poly1305                                                                                                                                         |
  \| Integrity Algorithm                                                   | Select one of the following:\* SHA1-96
- SHA1-160
- SHA2-256
- SHA2-384
- SHA2-512                                                                                                                                                                    |
  \| Diffie Hellman Group                                                  | Select the D-H key exchange group.                                                                                                                                                                                                                   |
  \| Lifetime In Minutes                                                   | Enter the SA lifetime (re-key interval) in minutes. Valid values are 10 through 1440.                                                                                                                                                                |
  \| Voice Mail                                                            | Select Allow traffic via tunnel to make voice mail exempt for Always-on VPN. Select Drop traffic to not make it an exemption.                                                                                                                        |
  \| Airprint                                                              | Select Allow traffic via tunnel to make Airprint traffic exempt for Always-on VPN. Select Drop traffic to not make it an exemption.                                                                                                                  |
  \| Cellular Services                                                     | Select Allow traffic via tunnel to make cellular services traffic exempt for Always-on VPN. Select Drop traffic to not make it an exemption.                                                                                                         |
  \| Allow traffic from captive websheet outside the VPN tunnel            | Select to allow traffic from captive web sheets outside the VPN tunnel.                                                                                                                                                                              |
  \| Allow traffic from all captive networking apps outside the VPN tunnel | Select to allow traffic from all captive networking apps outside the VPN tunnel to perform captive network handling.                                                                                                                                 |
  \| Captive Networking App Bundle Identifiers                             | List the bundle IDs for captive networking apps whose traffic will be allowed outside the VPN tunnel to perform captive network handling. Captive networking apps may require additional entitlements to operate in a captive environment.           |
