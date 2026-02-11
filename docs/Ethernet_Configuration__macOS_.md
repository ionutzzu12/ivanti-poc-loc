---
title: Ethernet Configuration (macOS)
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

**License:** Gold

**Applicable to:** macOS 10.13+ or supported newer versions.

Administrator can configure Ethernet Interface in variations. The following payloads are available for configuring Ethernet:

- Global Ethernet
- First active Ethernet
- First Ethernet
- Second active Ethernet
- Second Ethernet
- Third active Ethernet
- Third Ethernet

The different payload for configuring Ethernet are default fallback Global, First, First active, Second, Second active, Third, and Third active Ethernet interface. Apple has an existing known issue with install of First, First active, Second, Second active, Third, and Third active Ethernet interface.

## Ethernet configuration

Procedure

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **Ethernet** in the search field, and then select **Ethernet** Configuration.
4. Enter a name and describe the configuration.
5. Choose the configuration setup from the drop-down list.
6. Enter the [**Ethernet configuration settings**](./Ethernet_Configuration__macOS_.md).
7. Click **Next**.
8. Select the **Enable this configuration** option.
9. Select one the following channel options to apply the configuration:\* Device channel (most common)
   - User channel (Current registered user)
10. Select one of the following distribution options:\* All Devices
    - No Devices (default)
    - Custom
11. Click **Done**.

## Ethernet configuration settings

Use the settings in the following table to configure Ethernet. For more information about these settings, see [**Apple documentation**](https://developer.apple.com/documentation/devicemanagement/profile-specific_payload_keys?language=objc).

| **Setting**            | **Description**                                                                                                                                                                                                                                                                               |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Protocols**          |                                                                                                                                                                                                                                                                                               |
| **Accepted EAP Types** | Select the EAP types that can be used for accessing this network:\* Transport Layer Security(TLS): The TLS is a protocol that establishes an encrypted session between two computers on the Internet. It verifies the identity of the server and prevents hackers from intercepting any data. |

- TTLS: In the **Inner Identity** field, select one of the authentication protocols such as OS Default, PAP, CHAP, MSCHAP, MSCHAPv2, and EAP.
- PEAP
- LEAP
- EAP-SIM: In the **EAP SIM Number of RANDs** field, select number of rands from the drop-down list.
- EAP-AKA
- EAP-FAST: Select the EAP-FAST option that define authentication methods:\* **Use PAC**:Select to use a proxy auto-config (PAC).
  - **Provision PAC**: Select to allow a PAC to be provisioned. Otherwise, only a PAC already provisioned on the device can be used. This option is available only if you selected Use PAC.
  - **Provision PAC Anonymously**: Select to allow a PAC to be provisioned without authenticating the server. This option is available only if you selected Provision PAC.                                                                                                                                                                                                                                                                                                                                                        |
    \| **Authentication**     | **Username**: Specify the username required for network access. If you leave this blank, the device user will be prompted for it.\* Use Per-Connection Password: Select to prompt the device user for a password for each connection. When the device rejoins the same network, the device user will be prompted to re-authenticate to join the network. Every time connection is initiated, password is requested.
- Prompt One time password when connected to network: Password is requested only once when the configuration is pushed to the device. Every connect and disconnect to network, will not request any password.**Password**: (Optional) Enter the password for accessing this network. Otherwise, the device user will be prompted for any password required for accessing the network.**Outer identity**: (Optional) For TTLS, PEAP, and EAP-FAST, select to allow device users to hide their identity. The user's actual name appears only inside the encrypted tunnel. This option can increase security because an attacker cannot see the authenticating user's name in the clear.System Mode Credentials Source Identity: System mode is used for computer authentication. Authentication using system mode occurs before a user logs in to the computer. System mode is commonly configured to provide authentication with the computer's X.509 certificate (EAP-TLS) issued by a local certificate authority. |
  \| **Trust**              | **Trusted Certificates:&#x20;**&#x53;elect the checkboxes to select multiple certificates from the list.**Trusted Server Certificate Names**: Add the certificate name.\* **Allow Trust Exceptions**: Allow trust decisions (via dialog) to be made by the user.
- **Require TLS certificate****Maximum TLS version allowed with EAP authentication****Minimum TLS version allowed with EAP authentication\*\*\*\*TLS Trusted Certificates: MobileIron Agent CA Certificate**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
