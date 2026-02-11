---
title: Configuración de ajustes de la APN de Android
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

Las Configuraciones de ajustes de la APN de Android le permiten establecer las configuraciones de Nombre del punto de acceso (APN) necesarias en los dispositivos de una red pública. Esta configuración es aplicable a los dispositivos administrados por Android Enterprise Work y a los dispositivos administrados con perfil de trabajo en el dispositivo propiedad de la empresa (en la versión 9.0 de Android o en las versiones más recientes compatibles).

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Configuración \*\*\*\*> +Añadir**.
:::

:::WorkflowBlockItem
Seleccione la configuración **Ajustes de la APN de Android**.
:::

:::WorkflowBlockItem
Introduzca un nombre para la configuración.
:::

:::WorkflowBlockItem
Introduzca una descripción.
:::

:::WorkflowBlockItem
En la sección Ajuste de la configuración, configure las siguientes opciones:
:::

:::WorkflowBlockItem
| Ajuste                         | Descripción                                                                            |
| ------------------------------ | -------------------------------------------------------------------------------------- |
| **Nombre de la entrada**       | Escriba el nombre de los ajustes del punto de acceso.                                  |
| **Nombre del punto de acceso** | Escriba el nombre del punto de acceso.                                                 |
| **Tipo de punto de acceso**    | Seleccione el tipo de punto de acceso de las siguientes opciones:\* **Predeterminado** |

- **DUN**
- **IMS**
- **De emergencia**
- MMS
- **HIPRI**
- **CBS**
- **MCX**
- **SUPL**
- **FOTA**
- **IA**                                                                                                                                       |
  \| **Tipo de MVNO**                      | Seleccione el tipo de Operador de Red Virtual Móvil (MVNO, Mobile Virtual Network Operator) de las siguientes opciones:\* **Ninguna**
- **SPN**
- **IMSI**
- **GID**
- **ICCID**                                                                                                                                                          |
  \| **Bearer**                            | Seleccione el tipo de servicio al portador utilizado para la transmisión de datos de las siguientes opciones:\* **1xRTT**
- **CDMA**
- **EDGE**
- **EHRPO**
- **EVDO**
- **EVDO A**
- **EVDO B**
- **GPRS**
- **GSM**
- **HSDPA**
- **HASP**
- **HSPAP**
- **HSUPA**
- **IDEN**
- **IWLAN**
- **LTE**
- **NR**
- **TD\_SCDMA**
- **UMTS** |
  \| **Protocolo de APN**                  | Seleccione el protocolo APN necesario para la APN. A continuación se enumeran las opciones disponibles:\* **Ninguna**
- **IPV4**
- **IPV6**
- **IPV4/IPV6**
- **NON\_IP**
- **PPP&#x20;**(Protocolo de punto a punto)
- **NO ESTRUCTURADO**                                                                                               |
  \| **Protocolo de itinerancia de APN**   | Seleccione el protocolo de itinerancia de la APN necesario para la APN. A continuación se enumeran las opciones disponibles:\* **Ninguna**
- **IPV4**
- **IPV6**
- **IPV4/IPV6**
- **NON\_IP**
- **PPP&#x20;**(Protocolo de punto a punto)
- **NO ESTRUCTURADO**                                                                          |
  \| **Activar/desactivar APN**            | Active la configuración de la APN.                                                                                                                                                                                                                                                                                                       |
  \| **Id. del operador**                  | Introduzca el valor numérico de la Id. del operador.                                                                                                                                                                                                                                                                                     |
  \| **Tipo de autenticación**             | Seleccione el tipo de protocolo de autenticación de las siguientes opciones:\* **Ninguna**
- **PAP** (protocolo de autenticación de contraseña)
- **CHAP** (protocolo de autenticación por desafío mutuo)
- **PAP o CHAP**                                                                                                                |
  \| **Nombre de usuario**                 | Introduzca el nombre de usuario para iniciar sesión.                                                                                                                                                                                                                                                                                     |
  \| **Contraseña**                        | Introduzca la contraseña para iniciar sesión.                                                                                                                                                                                                                                                                                            |
  \| **Confirmar contraseña**              | Vuelva a introducir la contraseña para la confirmación.                                                                                                                                                                                                                                                                                  |
  \| **Número de puerto**                  | Introduzca el número de puerto (valor numérico entre 1 y 65535).                                                                                                                                                                                                                                                                         |
  \| **Dirección de proxy**                | Escriba la dirección de proxy.                                                                                                                                                                                                                                                                                                           |
  \| **Código de teléfono móvil del país** | Introduzca el código de país para teléfono móvil.                                                                                                                                                                                                                                                                                        |
  \| **Código de la red móvil**            | Introduzca el código de la red móvil                                                                                                                                                                                                                                                                                                     |
  \| **Dirección del proxy MMS**           | Escriba la dirección del proxy MMS.                                                                                                                                                                                                                                                                                                      |
  \| **Número de puerto de MMS**           | Introduzca el número de puerto MMS (valor numérico entre 1 y 65535)                                                                                                                                                                                                                                                                      |
  \| **Dirección del servidor MMS (mmsc)** | Escriba la dirección del servidor MMS.                                                                                                                                                                                                                                                                                                   |
  Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione una de las siguientes opciones de distribución:
:::

:::WorkflowBlockItem
- **Todos los dispositivos**
- Ningún dispositivo (predeterminada)
- **Personalizado**
  Haga clic en **Hecho**.
:::
::::

No se puede agregar otra configuración de APN con los mismos valores para los siguientes campos si ya existe una configuración de APN con estos valores para el dispositivo:

- Código de teléfono móvil del país
- Código de la red móvil
- Nombre del punto de acceso
- Dirección de proxy
- Número de puerto
- Dirección del proxy MMS
- Número de puerto de MMS
- Dirección del servidor MMS
- Activar/desactivar APN
- Tipo de MVNO
- Protocolo de APN
- Protocolo de itinerancia de APN

La Configuración de ajustes de la APN de Android anulará los ajustes de APN si ya se han configurado en el dispositivo manualmente o por parte del operador de red.
