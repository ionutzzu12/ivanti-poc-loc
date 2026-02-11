---
title: VPN a petición
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** dispositivos iOS

Mediante la configuración de VPN a petición se configura el acceso a un servidor VPN que se basa en dominios, nombres de host, etc.

## Ajustes de VPN a petición

| **Ajuste**                                                                | Qué hacer                                                                                                                                                 |
| ------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre                                                                    | Introduzca un nombre que identifique a esta configuración.                                                                                                |
| Descripción                                                               | Introduzca una descripción que explique la finalidad de esta configuración.                                                                               |
| Tipo de conexión                                                          | Seleccione el tipo de VPN que quiere configurar.Los siguientes ajustes dependerán de esta selección.                                                      |
| Activar VPN a petición                                                    | Seleccione esta opción si desea usar esta configuración para dominios y nombres de host que establecen una VPN a petición.                                |
| Activar las reglas de iOS(aplicable si se ha seleccionado VPN a petición) | En iOS y macOS, se pueden configurar:\* Reglas de red que permitan o no permitan conexiones con (y permitan o ignoren) las redes consideradas verdaderas. |

- Reglas de conexión que permiten cuando sea necesario, o no permiten nunca, conexiones a las redes consideradas verdaderas.Para las reglas de redes, se pueden especificar los siguientes tipos de parámetros:\* Coincidencia de dominio DNS
- Coincidencia de dirección de servidor DNS
- Coincidencia SSID
- Sondeo de la cadena de la URL
- Coincidencia del tipo de interfazPara las reglas de conexión, se pueden especificar los siguientes tipos de parámetros:\* Coincidencia de dominio DNS
- Coincidencia de dirección de servidor DNS
- Coincidencia SSID
- Sondeo de la cadena de la URL
- Coincidencia del tipo de interfaz
- Nombre del dominio
- Servidor DNS
- Sondeos de URL |
  \| Tipo de proveedor (iOS 9+)                                                | Seleccione uno de los siguientes proveedores de Tunnel:\* proxy de la aplicación - redirecciona el tráfico en la capa de la aplicación. Consulte la [**documentación de Apple**](https://developer.apple.com/documentation/networkextension/app_proxy_provider) para obtener una descripción general del proveedor de proxy de la aplicación.
- túnel del paquete - redirecciona el tráfico en la capa IP. Consulte la [**documentación de Apple**](https://developer.apple.com/documentation/networkextension/packet_tunnel_provider) para obtener una descripción general sobre el proveedor de Tunnel del paquete.                                                                                                                                                                                                                                          |
  \| EnforceRoutes                                                             | Cuando está habilitado, las rutas no defectuosas de la VPN anulan las rutas definidas localmente.\* Si IncludeAllNetworks está habilitado, el sistema no tiene en cuenta la configuración de las ejecutores
- Disponible en iOS 14.2 y posterior                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
  \| ExcludeLocalNetworks                                                      | Cuando está habilitado junto con IncludeAllNetworks, todas las rutas de tráfico de red locales fuera de la VPN.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
  \| IncludeAllNetworks                                                        | Cuando está habilitado, enruta todo el tráfico a través de la VPN.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

Los protocolos y sus ajustes se enumeran a continuación:

- [**IPsec (Cisco)**](./VPN_a_petición.md)
- [**Cisco AnyConnect**](./VPN_a_petición.md)
- [**SSL de Juniper**](./VPN_a_petición.md)
- [**VPN de NetMotion**](./VPN_a_petición.md)
- [**F5 SSL**](./VPN_a_petición.md)
- [**SonicWALL Mobile Connect**](./VPN_a_petición.md)
- [**Aruba VIA**](./VPN_a_petición.md)
- [**SSL personalizada**](./VPN_a_petición.md)
- [**Palo Alto Networks GlobalProtect**](./VPN_a_petición.md)

### IPsec (Cisco)

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                             |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                  |
| Autenticación del equipo  | Solo se puede utilizar la autenticación mediante certificado.                                                                                                                                                                                                    |
| Credencial                | Seleccione el certificado de identidad que desea utilizar.                                                                                                                                                                                                       |
| Incluir el PIN de usuario | Seleccione esta opción para solicitar un PIN al usuario.                                                                                                                                                                                                         |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.**Si selecciona Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\***Si selecciona Automática,** estarán disponibles los siguientes campos adicionales:\* **Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### Cisco AnyConnect

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                             |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                  |
| Grupo                     | Introduzca el grupo que desea utilizar para autenticar la conexión.                                                                                                                                                                                              |
| Autenticación del usuario | Solo se puede utilizar la autenticación mediante certificado.                                                                                                                                                                                                    |
| Credencial                | Seleccione el certificado de identidad que desea utilizar.                                                                                                                                                                                                       |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.**Si selecciona Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\***Si selecciona Automática,** estarán disponibles los siguientes campos adicionales:\* **Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### SSL de Juniper

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                             |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                  |
| Dominio                   | Introduzca el dominio de autenticación que desea utilizar para autenticar la conexión.                                                                                                                                                                           |
| Función                   | Introduzca la función de autenticación que desea utilizar para autenticar la conexión.                                                                                                                                                                           |
| Autenticación del usuario | Solo se puede utilizar la autenticación mediante certificado.                                                                                                                                                                                                    |
| Credencial                | Seleccione el certificado de identidad que desea utilizar.                                                                                                                                                                                                       |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.**Si selecciona Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\***Si selecciona Automática,** estarán disponibles los siguientes campos adicionales:\* **Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### VPN de NetMotion

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Autenticación del usuario | El certificado es el método de autenticación del usuario.**Credencial**: Seleccione el certificado de identidad que desea utilizar.                                                                                                                                        |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### F5 SSL

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                             |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                  |
| Autenticación del usuario | Solo se puede utilizar la autenticación mediante certificado.                                                                                                                                                                                                    |
| Credencial                | Seleccione el certificado de identidad que desea utilizar.                                                                                                                                                                                                       |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.**Si selecciona Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\***Si selecciona Automática,** estarán disponibles los siguientes campos adicionales:\* **Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### SonicWALL Mobile Connect

| **Ajuste**                          | Qué hacer                                                                                                                                                                                                                                                        |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                            | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                             |
| Cuenta                              | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                  |
| Grupo o dominio de inicio de sesión | Introduzca el grupo de inicio de sesión o el dominio que desea utilizar para autenticar la conexión.                                                                                                                                                             |
| Autenticación del usuario           | Solo se puede utilizar la autenticación mediante certificado.                                                                                                                                                                                                    |
| Credencial                          | Seleccione el certificado de identidad que desea utilizar.                                                                                                                                                                                                       |
| Configuración del proxy             | Para configurar un proxy, seleccione **Manual** o **Automática**.**Si selecciona Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\***Si selecciona Automática,** estarán disponibles los siguientes campos adicionales:\* **Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### Aruba VIA

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                             |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                  |
| Autenticación del usuario | Solo se puede utilizar la autenticación mediante certificado.                                                                                                                                                                                                    |
| Credencial                | Seleccione el certificado de identidad que desea utilizar.                                                                                                                                                                                                       |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.**Si selecciona Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\***Si selecciona Automática,** estarán disponibles los siguientes campos adicionales:\* **Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### SSL personalizada

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Identificador             | Introduzca el identificador de este VPN SSL en formato DNS invertido (por ejemplo: com.miempresa.miservidor).                                                                                                                                                    |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                             |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                  |
| Datos personalizados      | Introduzca los pares clave-valor que definen los datos personalizados para esta VPN.                                                                                                                                                                             |
| Autenticación del usuario | Solo se puede utilizar la autenticación mediante certificado.                                                                                                                                                                                                    |
| Credencial                | Seleccione el certificado de identidad que desea utilizar.                                                                                                                                                                                                       |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.**Si selecciona Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\***Si selecciona Automática,** estarán disponibles los siguientes campos adicionales:\* **Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### Palo Alto Networks GlobalProtect

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                             |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                  |
| Datos personalizados      | Introduzca los pares clave-valor que definen los datos personalizados para esta VPN.                                                                                                                                                                             |
| Autenticación del usuario | El certificado es el método de autenticación del usuario.Seleccione un certificado de identidad para usar en el campo **Credencial**.                                                                                                                            |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.**Si selecciona Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\***Si selecciona Automática,** estarán disponibles los siguientes campos adicionales:\* **Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

Escriba $ para ver una lista de [**variables&#x20;**](./Variables.md)compatibles, si las hubiera, para este campo.
