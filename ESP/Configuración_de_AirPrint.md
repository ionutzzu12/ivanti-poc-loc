---
title: Configuración de AirPrint
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Licencia:&#x20;**&#x53;ilver

Mediante la configuración de AirPrint se configura la impresión inalámbrica. La siguiente lista enumera los ajustes de AirPrint:

| Ajustes             | Qué hacer                                                                                                                                                                                                                                                                           |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre              | Introduzca un nombre que identifique a esta configuración.                                                                                                                                                                                                                          |
| Descripción         | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                                                                                                                         |
| Ajustes de AirPrint | **Dirección IP:** Introduzca la dirección IP de la impresora AirPrint.**Ruta del recurso:** Introduzca la ruta del recurso asociada con la impresora AirPrint, que se corresponde con el parámetro rp del registro \_ipps.tcp de Bonjour.Ejemplos:\* printers/Canon\_MG5300\_series |

- printers/Xerox\_Phaser\_7600
- ipp/print
- Epson\_IPP\_Printer.La ruta del recurso distingue entre mayúsculas y minúsculas.**Puerto:** introduzca el puerto de escucha del destino de AirPrint.Si no se especifica, AirPrint usará el puerto predeterminado. Para ver detalles sobre los puertos estándar de Apple, visite [**https://support.apple.com/en-us/HT202944**](https://support.apple.com/en-us/HT202944)**Forzar TLS**: le permite activar la conexión para segurizarla mediante Transport Layer Security(TLS). De forma predeterminada, esta opción está desactivada. |

Después de la instalación de la configuración de AirPrint en el macOS, los detalles de la impresora se insertan a través de la configuración de AirPrint al dispositivo. Los usuarios pueden ver los detalles de la impresora autorrellenados haciendo clic en Preferencia del sistema > Impresoras y escáneres > +. En la pantalla Añadir, el usuario debe seleccionar Predeterminado y luego seleccionar el perfil de impresión concreto. Esto añade la impresora requerida a la página web Impresoras y escáneres.
