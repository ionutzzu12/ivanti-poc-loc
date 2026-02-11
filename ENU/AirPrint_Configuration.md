---
title: AirPrint Configuration
createdAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:31 GMT+0200 (Eastern European Standard Time)
---

**License:**&#x53;ilver

An AirPrint configuration sets up wireless printing. The following table lists the AirPrint settings:

| Settings          | What to do                                                                                                                                                                                                                                                     |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name              | Enter a name that identifies this configuration.                                                                                                                                                                                                               |
| Description       | Enter a description that clarifies the purpose of this configuration.                                                                                                                                                                                          |
| AirPrint Settings | **IP Address:** Enter the IP address of the AirPrint printer.**Resource Path:** Enter the Resource Path associated with the AirPrint printer. This corresponds to the rp parameter of the \_ipps.tcp Bonjour record.Examples:\* printers/Canon\_MG5300\_series |

- printers/Xerox\_Phaser\_7600
- ipp/print
- Epson\_IPP\_Printer.The resource path is case sensitive.**Port:** Enter the listening port of the AirPrint destination.If this is not specified, AirPrint will use the default port. For details on Apple standard ports, visit [**https://support.apple.com/en-us/HT202944**](https://support.apple.com/en-us/HT202944)**Force TLS**: Allows you to enable the connection to be secured by Transport Layer Security(TLS). By default, it is disabled. |

After installation of AirPrint configuration on the macOS, the printer details are pushed through the AirPrint configuration to the device. Users can view the auto populated printer details by clicking System Preference > Printers & Scanners > +. In the Add screen, user must select Default and then select the required print profile. This adds the required printer to the Printers & Scanners.
