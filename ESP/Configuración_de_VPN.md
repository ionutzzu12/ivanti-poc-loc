---
title: Configuración de VPN
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:**

- Android (obsoleto para los dispositivos Android Enterprise. Es necesario utilizar la configuración gestionada para VPN específicas del Catálogo de aplicaciones).
- Windows
- iOS
- macOS
- visionOS

La configuración de VPN define los ajustes para el acceso a redes privadas virtuales.

La opción de delegación con distribución personalizada está disponible para esta configuración. Para obtener más información, consulte el tema *Distribuir la configuración* en [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md).

**Procedimiento**

1. Vaya a **Configuraciones** > **+Añadir**.
2. Seleccione la configuración de **VPN**.
3. Introduzca un **Nombre** para la configuración.
4. Introduzca una descripción.
5. Configure los ajustes de VPN según las siguientes descripciones.
6. (Solamente iOS 9.0+) En la sección Unir Dominios, haga clic en **+ Añadir** para introducir uno o varios dominios coincidentes (ejemplo: empresa.com). Se utiliza una conexión proxy cuando el dominio es uno de estos dominios específicos.
7. Haga clic en **Siguiente**.
8. (solo macOS) En la página Distribución, seleccione una de las siguientes opciones de distribución:\* Canal del dispositivo: la configuración es eficaz para todos los usuarios de un dispositivo; esta suele ser la opción más normal.
   - Canal del usuario: la configuración solo es eficaz para el usuario registrado actualmente en un dispositivo.
9. Seleccione las demás opciones de distribución para esta configuración.
10. Haga clic en **Hecho**.

## Ajustes de VPN

| **Ajuste**       | Qué hacer                                                                                            |
| ---------------- | ---------------------------------------------------------------------------------------------------- |
| Nombre           | Introduzca un nombre que identifique a esta configuración.                                           |
| Descripción      | Introduzca una descripción que explique la finalidad de esta configuración.                          |
| Tipo de conexión | Seleccione el tipo de VPN que quiere configurar.Los siguientes ajustes dependerán de esta selección. |

Los protocolos y sus ajustes se enumeran a continuación:

- [**L2TP**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- [**PPTP**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- [**IPsec (Cisco)**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- [**Cisco AnyConnect**](./Configuración_de_VPN.md) (Compatible con Ivanti Go)
- [**Junper SSL**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- [**VPN de NetMotion**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- Pulse Secure (Compatible con Ivanti Go)
- [**F5 SSL**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- [**SonicWALL Mobile Connect**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- [**Aruba VIA**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- [**SSL personalizado**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- [**Palo Alto Networks GlobalProtect**](./Configuración_de_VPN.md) (Compatible con Ivanti Go)
- [**KEv2 (solo Windows)**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)
- [**IKEv2**](./Configuración_de_VPN.md) (No compatible con Ivanti Go)

### L2TP

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Autenticación del usuario | Seleccione el método de autenticación que desea utilizar: **Contraseña** o **SecureID RSA**.                                                                                                                                                                               |
| Secreto compartido        | Introduzca el código de acceso del secreto compartido si es necesario para iniciar la conexión.                                                                                                                                                                            |
| Enviar todo el tráfico    | Seleccione esta opción para utilizar esta conexión para todo el tráfico de red. Esta opción ayuda a proteger los datos que pueden verse afectados, especialmente en redes públicas.                                                                                        |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### PPTP

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Autenticación del usuario | Seleccione el método de autenticación que desea utilizar: **Contraseña** o **SecureID RSA**.                                                                                                                                                                               |
| Nivel de cifrado          | Seleccione el nivel de cifrado de datos para la conexión: **Ninguno, Automático** o **Máximo (128 bits)**.                                                                                                                                                                 |
| Enviar todo el tráfico    | Seleccione esta opción para utilizar esta conexión para todo el tráfico de red. Esta opción ayuda a proteger los datos que pueden verse afectados, especialmente en redes públicas.                                                                                        |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### IPsec (Cisco)

| **Ajuste**                 | Qué hacer                                                                                                                                                                                                                                                                  |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                   | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                     | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Autenticación del equipo   | Seleccione el método de autenticación que desea utilizar: **Secreto compartido / Nombre del grupo** o **Certificado**.                                                                                                                                                     |
| Nombre del grupo           | Autenticación por Secreto compartido/Nombre de grupo.Especifique el nombre de grupo que desea utilizar. Si se utiliza la autenticación híbrida, la cadena debe terminar con €œ\[hybrid]â€.                                                                                |
| Secreto compartido         | Autenticación por Secreto compartido/Nombre de grupo.Introduzca el código de acceso del secreto compartido.                                                                                                                                                                |
| Usar autenticación híbrida | Autenticación por Secreto compartido/Nombre de grupo.Seleccione para especificar la autenticación híbrida, p. ej., el servidor proporciona un certificado y el cliente proporciona una clave precompartida.                                                                |
| Solicitud de contraseña    | Autenticación por Secreto compartido/Nombre de grupo.Especifique si se le debe solicitar una contraseña al usuario cuando se conecte.                                                                                                                                      |
| Credencial                 | *Autenticación del certificado*Seleccione el certificado de identidad que desea utilizar.                                                                                                                                                                                  |
| Incluir el PIN de usuario  | *Autenticación del certificado*Seleccione esta opción para solicitar un PIN al usuario.                                                                                                                                                                                    |
| Configuración del proxy    | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### Cisco AnyConnect

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Grupo                     | Introduzca el grupo que desea utilizar para autenticar la conexión.                                                                                                                                                                                                        |
| Autenticación del usuario | Seleccione el método de autenticación de usuario que desea utilizar: **Contraseña** o **Certificado**.Si selecciona **Certificado**, los siguientes campos adicionales estarán disponibles:**Credencial**: Seleccione el certificado de identidad que desea utilizar.      |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### SSL de Juniper

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Dominio                   | Introduzca el dominio de autenticación que desea utilizar para autenticar la conexión.                                                                                                                                                                                     |
| Función                   | Introduzca la función de autenticación que desea utilizar para autenticar la conexión.                                                                                                                                                                                     |
| Autenticación del usuario | Seleccione el método de autenticación de usuario que desea utilizar: **Contraseña** o **Certificado**.Si selecciona **Certificado**, los siguientes campos adicionales estarán disponibles:**Credencial**: Seleccione el certificado de identidad que desea utilizar.      |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### VPN de NetMotion

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Autenticación del usuario | Seleccione el método de autenticación de usuario que desea utilizar: **Contraseña** o **Certificado**. Si selecciona **Certificado**, los siguientes campos adicionales estarán disponibles:**Credencial**: Seleccione el certificado de identidad que desea utilizar.     |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### F5 SSL

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                          |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                               |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                    |
| Autenticación del usuario | Introduzca el método de autenticación que desea utilizar: **Contraseña** o **Certificado**.Si selecciona **Certificado**, los siguientes campos adicionales estarán disponibles:**Credencial**: Seleccione el certificado de identidad que desea utilizar.         |
| Configuración del proxy   | Para configurar un proxy, seleccione Manual o Automática.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### SonicWALL Mobile Connect

| **Ajuste**                          | Qué hacer                                                                                                                                                                                                                                                                  |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                            | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                              | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Grupo o dominio de inicio de sesión | Introduzca el grupo de inicio de sesión o el dominio que desea utilizar para autenticar la conexión.                                                                                                                                                                       |
| Autenticación del usuario           | Seleccione el método de autenticación de usuario que desea utilizar: **Contraseña** o **Certificado**.Si selecciona Certificado, estarán disponibles los siguientes campos adicionales:**Credencial**: Seleccione el certificado de identidad que desea utilizar.          |
| Configuración del proxy             | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### Aruba VIA

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                             |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                  |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                       |
| Autenticación del usuario | Seleccione el método de autenticación de usuario que desea utilizar: **Contraseña** o **Certificado**.Si selecciona **Certificado**, los siguientes campos adicionales estarán disponibles:**Credencial**: Seleccione el certificado de identidad que desea utilizar. |
| Configuración del proxy   | Para configurar un proxy, seleccione Manual o Automática.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\*    |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### SSL personalizada

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Identificador             | Introduzca el identificador de este VPN SSL en formato DNS invertido (por ejemplo: com.miempresa.miservidor).                                                                                                                                                              |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Datos personalizados      | Introduzca los pares clave-valor que definen los datos personalizados para esta VPN.                                                                                                                                                                                       |
| Autenticación del usuario | Seleccione el método de autenticación de usuario que desea utilizar: **Contraseña** o **Certificado**.Si selecciona Certificado, estarán disponibles los siguientes campos adicionales:**Credencial**: Seleccione el certificado de identidad que desea utilizar.          |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### Palo Alto Networks GlobalProtect

No se aplica a los dispositivos Android.

| **Ajuste**                | Qué hacer                                                                                                                                                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                  | Introduzca la dirección IP o el nombre de host para el servidor VPN.                                                                                                                                                                                                       |
| Cuenta                    | Introduzca la cuenta de usuario que desea utilizar para autenticar la conexión.                                                                                                                                                                                            |
| Datos personalizados      | Introduzca los pares clave-valor que definen los datos personalizados para esta VPN.                                                                                                                                                                                       |
| Autenticación del usuario | Seleccione el método de autenticación de usuario que desea utilizar: **Contraseña** o **Certificado**.Si selecciona Certificado, estarán disponibles los siguientes campos adicionales:**Credencial**: Seleccione el certificado de identidad que desea utilizar.          |
| Configuración del proxy   | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### IKEv2 (solo Windows)

| **Ajuste**              | **Qué hacer**                                                                                                                                                                                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Servidor                | Introduzca el nombre de host o dirección IP del servidor VPN.                                                                                                                                                                                                              |
| Configuración del proxy | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\* |

- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

### IKEv2

| **Ajuste**              | **Qué hacer**                                                                   |
| ----------------------- | ------------------------------------------------------------------------------- |
| **Servidor**            | Introduzca el nombre de host o dirección IP del servidor VPN.                   |
| **Identificador local** | El identificador del cliente IKEv2 en alguno de los siguientes formatos:\* FQDN |

- UserFQDN
- Dirección
- ASN1DN                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| Identificador remoto                                                  | Identificador remoto en uno de los siguientes formatos:\* FQDN
- UserFQDN
- Dirección
- ASN1DN                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| Autenticación del equipo                                              | Solo disponible si **Habilitar EAP** no está seleccionado.Seleccione una de las siguientes opciones:\* Certificado
- Secreto compartido                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| Autenticación EAP                                                     | Solo disponible si **Habilitar EAP** está seleccionado.Seleccione una de las siguientes opciones:\* Certificado
- Nombre de usuario/contraseña                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| Secreto compartido                                                    | Solo disponible si se ha seleccionado Secreto compartido para la Autenticación del equipo. Introduzca el secreto compartido para la conexión.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| Credencial                                                            | Solo disponible si se ha seleccionado Certificado para la Autenticación del equipo. Seleccione el certificado que desea utilizar. Este certificado se enviará para autenticación del cliente IKE. Si se usa la autenticación ampliada, este certificado se puede usar también para EAP-TLS.                                                                                                                                                                                                                                                                                                                                                                             |
  \| Activar EAP                                                           | Seleccione esta opción para habilitar la autenticación ampliada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| Cuenta                                                                | Solo disponible si se ha seleccionado «Nombre de usuario/contraseña» para la Autenticación EAP. Introduzca la Id. de cuenta para el servidor VPN.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
  \| Contraseña                                                            | Solo disponible si se ha seleccionado «Nombre de usuario/contraseña» para la Autenticación EAP. Introduzca la contraseña para el servidor VPN.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| Intervalo de detección de pares no funcionales                        | Seleccione una de las siguientes opciones:\* Ninguno (desactivar)
- Bajo (se envía un keepalive 1 vez por hora)
- Medio (se envía un keepalive cada 30 minutos)
- Alto (se envía un keepalive cada 10 minutos)                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| Nombre común de emisor del certificado del servidor                   | (Opcional) Nombre común de un emisor de certificados de servidor, hace que el servidor IKE envíe una solicitud de certificado basada en el emisor de certificados al servidor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| Nombre común del certificado del servidor                             | (Opcional) Nombre común de un emisor de certificados de servidor que se usa para validar el certificado que envía el servidor IKE.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
  \| Utilice los atributos de subred IP4 y IP6                             | (Opcional) Seleccione usar los atributos de subred IP4 y IP6                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
  \| Activar el Protocolo de movilidad y hospedaje múltiple IKEv2 (MOBIKE) | (Opcional) El ajuste predeterminado es 0. MOBIKE (La posibilidad de admitir dispositivos móviles multi-hospedados cuando se conectan a enlaces tanto móviles como Wi-Fi con múltiples direcciones IP) está habilitado. Está habilitado de forma predeterminada. Establézcalo en 1 para desactivar MOBIKE.                                                                                                                                                                                                                                                                                                                                                               |
  \| Activar **Perfect Forward Secrecy (PFS)**                             | (Opcional) Si se establece en 1, habilita PFS para conexiones IKEv2. El ajuste predeterminado es 0.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \| Active la **redirección IKEv2.**                                      | (Opcional) El ajuste predeterminado es 0. La conexión IKEv2 se redirige si se recibe una solicitud de redirección del servidor. Está habilitado de forma predeterminada. Establézcalo en 1 para desactivar la redirección IKEv2.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| Active **NAT keepalive**                                              | Activa la Traducción de direcciones de red (NAT) keepalive, que impide la eliminación de entradas NAT en ausencia de tráfico cuando hay NAT entre sistemas IKE.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
  \| **Intervalo de NAT keepalive**                                        | Si NAT keepalive está activado, este es el tiempo en segundos que se enviarán paquetes keepalive para el dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
  \| **PPK**                                                               | Introduzca la clave poscuántica precompartida (PPK) con servidores VPN compatibles con RFC 8784. Si esta clave está presente, el Identificador PPK debe estar presente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| **Identificador PPK**                                                 | Introduzca el identificador PPK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| **PPK obligatorio**                                                   | Seleccione una de las opciones desplegables:\* **Mandato**: La conexión VPN se establecerá correctamente si el servidor admite RFC 8784 o si acepta el identificador PPK especificado en el Identificador PPK.
- **No mandato**: La conexión VPN no se establecerá si el servidor no admite RFC 8784 o no acepta el identificador PPK especificado en el Identificador PPK.                                                                                                                                                                                                                                                                                              |
  \| **Algoritmo de cifrado**                                              | Seleccione una de las siguientes opciones:\* **DES**
- **3DES**
- **AES-128**
- **AES-256** (opción predeterminada)
- **AES-128 GCM**
- **AES-256 GCM**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| Algoritmo de integridad                                               | Seleccione una de las siguientes opciones:\* **SHA2-256** (opción predeterminada)
- **SHA2-384**
- **SHA2-512**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \| Grupo Diffie Hellman                                                  | Seleccione una de las siguientes opciones:\* **1**
- **2** (opción predeterminada)
- **5**
- **14**
- **15**
- **16**
- **17**
- **18**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
  \| Vigencia en minutos                                                   | Introduzca la vigencia SA (intervalo de reintroducción de clave) en minutos. Los valores válidos van del 10 al 1440.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| Configuración del proxy                                               | Para configurar un proxy, seleccione **Manual** o **Automática**.Si seleccion&#x61;**&#x20;Manual,** estarán disponibles los siguientes campos adicionales:\* **Servidor y puerto**: Introduzca la dirección de la red y el número de puerto asignado al servidor proxy.\*
- **Autenticación**: Introduzca un nombre de usuario válido si es necesario para conectarse al proxy.\*
- **Contraseña**: Introduzca una contraseña válida si es necesaria para conectarse al proxy.\*Si seleccion&#x61;**&#x20;Automática,** estarán disponibles los siguientes campos adicionales:**Dirección URL del servidor proxy**: Introduzca la dirección URL completa para el proxy. |

\*Escriba $ para ver una lista de [**variables**](./Variables.md) compatibles, si las hubiera, para este campo.
