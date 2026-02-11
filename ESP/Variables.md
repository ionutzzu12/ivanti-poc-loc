---
title: Variables
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Puede utilizar variables en ciertos campos de la configuración para representar valores específicos para un usuario concreto. Cualquier campo que admita variables mostrará una lista de variables admitidas si escribe $ en el campo. Esta sección contiene los siguientes temas:

- [**Variables de la cuenta de usuario compatibles**](./Variables.md)
- [**Variables de dispositivos compatibles**](./Variables.md)

## Variables de la cuenta de usuario compatibles

### Variables del usuario

::Image[]{src="awvariables.png" signedSrc="awvariables.png" size="18" caption alt isUploading="false" sha initialPath="awvariables.png" githubPath="awvariables.png" position="flex-start"}

| **Clave de variable**          | **Descripción del valor**                                                                  |
| ------------------------------ | ------------------------------------------------------------------------------------------ |
| $\{department}                 | atributo departamento (requiere Entra ID)                                                  |
| $\{edipi}                      | Intercambio electrónico de datos: identificador personal                                   |
| $\{managedAppleId}             | Id. de Apple administrada del usuario                                                      |
| $\{sAMAccountName}             | Atributo sAMAccountName (requiere Active Directory)                                        |
| $\{userCN}                     | Atributo Nombre común (NC) extraído del nombre distintivo (requiere LDAP)                  |
| $\{userDisplayName}            | Nombre en pantalla                                                                         |
| $\{userDN}                     | Nombre distintivo (requiere LDAP)                                                          |
| $\{userEmailAddressDomain}     | La parte del dominio de la dirección de correo electrónico (la parte de después de la "@") |
| $\{userEmailAddressLocalPart}> | La parte local de la dirección de correo electrónico (la parte de antes de la "@")         |
| $\{userEmailAddress}           | Dirección de correo electrónico                                                            |
| $\{userFirstName}              | Nombre                                                                                     |
| $\{userLastName}               | Apellido                                                                                   |
| $\{userLocale}                 | Configuración regional                                                                     |
| $\{userOU}                     | Atributo de unidad organizativa (OU) extraído del nombre distintivo (requiere LDAP)        |
| $\{userREALM}                  | Información de Kerberos Realm (requiere Active Directory)                                  |
| $\{userUIDDomain}              | El dominio que forma parte de la ID de inicio de sesión (la parte tras la "@")             |
| $\{userUIDLocalPart}           | La parte local del ID de inicio de sesión (la parte de antes de la "@")                    |
| $\{userUID}                    | ID de inicio de sesión (formato de la dirección de correo electrónico)                     |
| $\{userUPN}                    | Atributo userPrincipalName (requiere Active Directory)                                     |

## Variables de dispositivos compatibles

Utilice las variables del dispositivo para especificar la información acerca de un dispositivo móvil.

### Variables del dispositivo

![](Resources/Images/VariableSubstitution.png)

| **Clave de variable**            | **Descripción del valor**                                                                        |
| -------------------------------- | ------------------------------------------------------------------------------------------------ |
| $\{clientLastCheckin}            | Fecha de la última vez que se conectó el cliente (conexión más reciente: bien MDM o cliente)     |
| $\{deviceAltSN}                  | Número de serie alternativo                                                                      |
| $\{deviceClientDeviceIdentifier} | Identificador que usa la aplicación del cliente                                                  |
| $\{deviceGUID}                   | Identificador de dispositivo único global                                                        |
| $\{deviceIccIdentifier}          | ICCID                                                                                            |
| $\{deviceIMEI2}                  | IMEI2                                                                                            |
| $\{deviceIMEI}                   | IMEI                                                                                             |
| $\{deviceIMSI}                   | IMSI                                                                                             |
| $\{deviceLastCheckin}            | Fecha de la última vez que se conectó el dispositivo (conexión más reciente: bien MDM o cliente) |
| $\{deviceMdmChannelId}           | Identificador de dispositivos internos                                                           |
| $\{deviceMdmDeviceIdentifier}    | Identificador usado para MDM                                                                     |
| $\{deviceMEIdentifier}           | MEID                                                                                             |
| $\{deviceModel}                  | Modelo                                                                                           |
| $\{deviceName}                   | Nombre del dispositivo                                                                           |
| $\{devicePhoneNumber}            | Número de teléfono del dispositivo                                                               |
| $\{devicePK}                     | Identificador de dispositivo único del cluster                                                   |
| $\{deviceSN}                     | Número de serie                                                                                  |
| $\{deviceUDID}                   | iOS UDID                                                                                         |
| $\{deviceWifiMacAddress}         | Dirección MAC de Wi-Fi                                                                           |

### Variables de la plantilla de correo electrónico

| **Clave de variable**    | **Descripción del valor**     |
| ------------------------ | ----------------------------- |
| $\{policyMessageContent} | Cuerpo del correo electrónico |
| $\{policyMessageTitle}   | Asunto del correo electrónico |

### Variables de la marca de hora

| **Clave de variable** | **Descripción del valor**                       |
| --------------------- | ----------------------------------------------- |
| $\{timestampMS}       | Marca de hora actual (milisegundos desde epoch) |

### Variables de plantilla de políticas

| **Clave de variable**        | **Descripción del valor**                                                                                             |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| $\{nameOfPolicy}             | Nombre de política infringido                                                                                         |
| $\{nextAction}               | Siguiente acción de cumplimiento en capas (distinto a esperar y retirar) que se llevará a cabo tras enviar el mensaje |
| $\{nonComplianceTime}        | Número de días que el dispositivo ha estado en un estado de no compatibilidad                                         |
| $\{policyViolationFirstTime} | La marca de hora cuando se desencadenó por primera vez la infracción de políticas (formato UTC DD-MM-AAAA)            |
| $\{ruleConditions}           | Definición de la regla (Cadena de consulta tal y como aparece ahora)                                                  |

**Temas relacionados:**
