---
title: Atributos
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Utilice la página Atributos para llevar a cabo las tareas siguientes:

- Administre los tipos de información que puede registrar con usuarios, dispositivos y aplicaciones.
- Visualizar los tipos de estándares de información que Ivanti Neurons for MDM monitoriza.

Los atributos de usuario personalizados incluyen información como Departamento o una ID interna. Cada atributo tiene una variable correspondiente que puede usar para crear grupos o distribuir configuraciones.

Durante la creación de los criterios de grupos de reglas de usuario, si los atributos personalizados tienen un valor numérico, Ivanti Neurons for MDM no es compatible con las operaciones de integrales.

## Creación de atributos personalizados

Puede crear atributos personalizados desde el portal administrativo de Ivanti Neurons for MDM.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Inicie sesión en el portal administrativo.
:::

:::WorkflowBlockItem
Vaya a **Administrador** > **Sistema** > **Atributos**.
:::

:::WorkflowBlockItem
En **Atributos personalizados**, haga clic en **+Añadir**.
:::

:::WorkflowBlockItem
En el campo **Nombre del atributo**, introduzca el texto que vaya a representar el atributo.
:::

:::WorkflowBlockItem
el texto que introduzca se utilizará para crear la variable correspondiente en el campo **Uso**.

Seleccione cualquier tipo de atributo de las siguientes opciones de **Tipo de atributo**.
:::

:::WorkflowBlockItem
- **Usuario**
- **Dispositivo**
- **Aplicación**
- **IDP** (para más información, consulte [**Aprovisionamiento de usuarios con SCIM&#x20;**](./Aprovisionamiento_de_usuarios_con_SCIM.md)o [**Conecte Ivanti Neurons for MDM con Entra ID User Source**](./Conecte_Ivanti_Neurons_for_MDM_con_Entra_ID_User_Source.md))
  Si el tipo de atributo es Dispositivo, seleccione una de las siguientes opciones de **Tipo de datos**:- **Numérico**
- **Texto**
:::

:::WorkflowBlockItem
Haga clic en **Añadir**.

El atributo de usuario personalizado creado se muestra en la sección **Administrador añadido** en la página Atributos.
:::
::::

la combinación de atributos personalizados $\{deviceattribute} + $\{custom-attribute} + $\{userattribute} + $\{Static String} se admite en cualquier orden.

## Cambiar el nombre de un atributo personalizado

Al cambiar el nombre de un atributo personalizado, se cambiará también el nombre de todas las referencias a dicho atributo personalizado que se estén usando en las siguientes entidades:

- Política personalizada
- Grupo de usuarios
- Grupo de dispositivos
- Filtro de distribución de aplicaciones
- Espacios

no se actualizarán las referencias al atributo personalizado en ninguna otra entidad como las configuraciones, plantillas de invitaciones por correo electrónico, correos electrónicos y mensajes push en medidas de cumplimiento de políticas, entre otros.

**Procedimiento**

1. En **Administrador añadido**, haga clic en **+Editar&#x20;**&#x6A;unto al atributo del que desea cambiar el nombre.
2. En el campo **Nombre del atributo**, introduzca el nuevo nombre que vaya a representar el atributo.
3. el texto que introduzca se utilizará para crear la variable correspondiente en el campo **Uso**.
   Haga clic en **Guardar**.

## Eliminar un atributo personalizado

Si elimina un atributo personalizado, también eliminará sus valores de todos los usuarios o dispositivos asociados. Esto no puede revertirse.

No se pueden eliminar los atributos personalizados si el atributo se está usando en cualquiera de las siguientes entidades:

- Política personalizada
- Grupo de usuarios
- Grupo de dispositivos
- Filtro de distribución de aplicaciones
- Espacios

Antes de intentar eliminar el atributo personalizado, quítelo de las entidades.

Si el atributo que está intentando eliminar no tiene referencias de ninguna de las entidades anteriores, al hacer clic en **Eliminar** junto al atributo aparecerá un mensaje emergente para confirmar la acción. Confirme la acción y haga clic en **Eliminar**.

Los nombres de campo de los siguientes atributos personalizados se ordenan en los creadores de reglas aplicables:

- Atributo personalizado de LDAP
- Atributo personalizado del usuario
- Atributo personalizado del dispositivo
- Atributos IDP personalizados
- Atributos de aplicaciones personalizados

## Ver los atributos del sistema

Los atributos del sistema son atributos predefinidos que se pueden usar en las configuraciones como variables. La lista completa se proporciona en la sección **Atributos del sistema** de la página **Administrador&#x20;**>**&#x20;Sistema&#x20;**>**&#x20;Atributos**. Los atributos del sistema incluyen los siguientes tipos de atributos:

- Atributos del usuario
- Atributos del dispositivo
- Atributos de la plantilla de correo electrónico
- Atributos del sistema
- Atributos de la marca de hora
- Atributos personalizados del usuario de Entra ID
- Atributos de políticas

## Atributos del usuario

Utilice los atributos del usuario para especificar la información sobre los usuarios.

| Clave                          | Descripción                                                                                |
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

## Atributos del dispositivo

Utilice los atributos del dispositivo para especificar la información acerca de un dispositivo móvil.

| Clave                            | Descripción                                                                                      |
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
|                                  | Número de teléfono 2                                                                             |
|                                  | ICCID 2                                                                                          |

Cuando se crea un atributo personalizado y se hace referencia a este en la configuración de una aplicación administrada, si se actualiza el valor del atributo, el atributo que se referencia en la configuración de la aplicación administrada también se actualiza y la configuración de la aplicación administrada se volverá a enviar al dispositivo.

Cuando se actualizan los atributos Personalizado o Dispositivo y la configuración se envía a un dispositivo, la configuración de marca de Android Kiosk también debe actualizarse.

## Atributos de la aplicación

Use os atributos de la aplicación para especificar la información sobre las aplicaciones y crear grupos de aplicaciones personalizadas.

| Clave             | Descripción                                              |
| ----------------- | -------------------------------------------------------- |
| $\{appAdded}      | Fecha en que se agregó la aplicación a AppCatalog        |
| $\{appName}       | Nombre de la aplicación                                  |
| $\{appOsPlatform} | Sistema operativo de la aplicación                       |
| $\{appPackageId}  | Grupo de aplicaciones o ID del paquete                   |
| $\{appSource}     | Describe la fuente desde la que se importó la aplicación |
| $\{IsVpp}         | Describe si una aplicación de iOS o macOS es VPP o no    |

### Atributos de la plantilla de correo electrónico

| Clave                    | Descripción                   |
| ------------------------ | ----------------------------- |
| $\{policyMessageContent} | Cuerpo del correo electrónico |
| $\{policyMessageTitle}   | Asunto del correo electrónico |

### Atributos de la marca de hora

| Clave de variable | Descripción                                     |
| ----------------- | ----------------------------------------------- |
| $\{timestampMS}   | Marca de hora actual (milisegundos desde epoch) |

### Atributos de plantilla de políticas

| Clave                        | Descripción                                                                                                           |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| $\{nameOfPolicy}             | Nombre de política infringido                                                                                         |
| $\{nextAction}               | Siguiente acción de cumplimiento en capas (distinto a esperar y retirar) que se llevará a cabo tras enviar el mensaje |
| $\{nonComplianceTime}        | Número de días que el dispositivo ha estado en un estado de no compatibilidad                                         |
| $\{policyViolationFirstTime} | La marca de hora cuando se desencadenó por primera vez la infracción de políticas (formato UTC DD-MM-AAAA)            |
| $\{ruleConditions}           | Definición de la regla (Cadena de consulta tal y como aparece ahora)                                                  |

Temas relacionados:

- [**Asignar atributos personalizados a los usuarios**](./Asignar_atributos_personalizados_a_los_usuarios.md)
- [**Asignar atributos personalizados a los dispositivos**](./Asignar_atributos_personalizados_a_los_dispositivos.md)
- [**Eliminar atributos personalizados de los usuarios**](./Eliminar_atributos_personalizados_de_los_usuarios.md)
- [**Eliminar atributos personalizados de los dispositivos**](./Eliminar_atributos_personalizados_de_los_dispositivos.md)
