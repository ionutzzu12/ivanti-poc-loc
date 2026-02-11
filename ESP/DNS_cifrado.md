---
title: DNS cifrado
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

**Licencia:** Gold

**Aplicable a:**

- iOS 14.0 o versiones más recientes compatibles.
- macOS 11.0 o versiones más recientes compatibles.
- visionOS 1.1 o versiones más recientes compatibles.

La configuración del DNS cifrado que le permitirá mejorar la seguridad sin necesidad de configurar la VPN.

Esta sección contiene los siguientes temas:

- [**Configuración de DNS cifrado**](./DNS_cifrado.md)
- [**Ajustes de la configuración de DNS cifrado**](./DNS_cifrado.md)

## Configuración de DNS cifrado

**Procedimiento**

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **DNS** en el campo de búsqueda y, a continuación, haga clic en la configuración de **DNS cifrado**.
4. Introduzca un nombre y describa la configuración.
5. Introduzca los [**Ajustes de la configuración de DNS cifrado**](./DNS_cifrado.md).
6. Haga clic en **Siguiente**.
7. Seleccione la opción **Habilitar esta configuración**.
8. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
   - Ningún dispositivo (predeterminada)
   - personalizada
9. Haga clic en **Hecho**.

## Ajustes de la configuración de DNS cifrado

Utilice los ajustes de la siguiente tabla para configurar el DNS cifrado. Para obtener más información sobre estos ajustes, consulte [**Documentación de Apple**](https://developer.apple.com/documentation/devicemanagement/dnssettings).

| **Ajuste**         | **Descripción**                                                                                                                                          |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Ajustes de DNS** | Un diccionario que define una configuración para un servidor DNS cifrado.                                                                                |
| Protocolo de DNS   | Especifique el protocolo de transporte cifrado que se utiliza para comunicarse con el servidor DNS. Seleccione uno de los siguientes protocolos:\* HTTPS |

- TLS                                                                                                                                                                                                                                                                                                                                                       |
  \| URL del servidor                                       | La plantilla URI de un servidor DNS mediante HTTPS, tal como se define en RFC 8484. Esta URL debe utilizar el esquema https\:// y el nombre de host o la dirección en la URL se van a utilizar para validar el certificado del servidor. Si no se indican Direcciones del servidor, se va a utilizar el nombre de host o la dirección en la URL para determinar las direcciones del servidor. Esta clave debe estar presente únicamente si el protocolo de DNS es HTTPS.                                            |
  \| Direcciones del servidor                               | Una lista no ordenada de cadenas de direcciones IP del servidor DNS. Estas direcciones IP pueden ser una combinación de direcciones IPv4 e IPv6.Haga clic en **Añadir** para añadir una dirección de servidor o varias.                                                                                                                                                                                                                                                                                             |
  \| Dominios complementarios de coincidencia               | Una lista de cadenas de dominio utilizadas para determinar qué consultas DNS usará el servidor DNS. Si no se proporciona este conjunto, todos los dominios utilizarán el servidor DNS.Haga clic en **Añadir** para añadir un dominio o más.                                                                                                                                                                                                                                                                         |
  \| Prohibir a los usuarios desactivar los ajustes del DNS | Prohíbe a los usuarios deshabilitar los ajustes del DNS. Esta clave solo está disponible en dispositivos supervisados.                                                                                                                                                                                                                                                                                                                                                                                              |
  \| **Reglas de requisitos**                               | Un conjunto de reglas que define los ajustes de DNS. Si no hay reglas implementadas, el sistema siempre aplicará los ajustes de DNS.Haga clic en **+ Añadir reglas de requisitos** para añadir un conjunto o más de reglas de requisitos.                                                                                                                                                                                                                                                                           |
  \| Red                                                    | La acción que se debe realizar si este diccionario coincide con la red actual. Seleccione una de las siguientes acciones:\* **Conectar:** se aplican Ajustes de DNS cuando el diccionario coincida.
- **Desconectar:** no se aplican Ajustes de DNS cuando el diccionario coincida.
- **Evaluar la conexión:** se aplican Ajustes de DNS con excepciones por dominio cuando el diccionario coincida.                                                                                                                 |
  \| Evaluar la conexión                                    | Esta opción de red tiene los siguientes ajustes:\* **Acción de dominio**: comportamiento de los ajustes de DNS para los dominios especificados. Seleccione una de las siguientes acciones:- **No conectar nunca**: no utilizar los Ajustes de DNS para los dominios especificados.
  - **Conectar si es necesario**: permitir el uso de Ajustes de DNS para los dominios especificados.
- **Dominios**: los dominios para los que se aplica esta evaluación. Haga clic en **+ Añadir** para añadir un dominio o más. |
  \| **Reglas**                                             | Haga clic en **+ Añadir** para añadir una regla o más para hacer coincidir los siguientes parámetros con los valores especificados correspondientes.                                                                                                                                                                                                                                                                                                                                                                |
  \| Coincidencia de dominio DNS                            | Un conjunto de nombres de dominio. Esta regla coincide si alguno de los nombres de dominio en la lista especificada coincide con algún dominio en la lista de dominios de búsqueda del dispositivo.                                                                                                                                                                                                                                                                                                                 |
  \| Coincidencia de dirección de servidor DNS              | Un conjunto de direcciones IP. Esta regla coincide si alguno de los servidores DNS especificados de la red coincide con alguna entrada del conjunto.                                                                                                                                                                                                                                                                                                                                                                |
  \| Coincidencia SSID                                      | Un conjunto de SSID que coinciden con la red actual. Si la red no es una red wifi o si el SSID no aparece en este conjunto, la coincidencia no se realiza.Omita esta clave y el conjunto correspondiente para coincidir con cualquier SSID.                                                                                                                                                                                                                                                                         |
  \| Coincidencia del tipo de interfaz                      | Un tipo de interfaz. Si se especifica, esta regla coincide únicamente si el hardware de la interfaz de red primaria coincide con el tipo especificado. Seleccione uno de los siguientes tipos:\* Ethernet
- Wi-Fi
- Móvil                                                                                                                                                                                                                                                                                            |
  \| Sondeo de la cadena de la URL                          | Una URL para realizar sondeos. Si esta URL se obtiene correctamente (con la devolución de un código de estado 200 HTTP) sin redireccionar, esta regla coincidirá.                                                                                                                                                                                                                                                                                                                                                   |
