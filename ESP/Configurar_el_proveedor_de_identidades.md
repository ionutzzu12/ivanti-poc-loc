---
title: Configurar el proveedor de identidades
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Licencia::Variable\{key="PrimaryMI.license2" type="variable"}

Configure un proveedor de identidades (IdP) para autenticar los usuarios que desean registrar dispositivos con Ivanti Neurons for MDM, acceder a este portal de administración o acceder al portal de autoservicio. Es necesario un directorio de usuarios compatible con LDAP en el entorno local. Ivanti Neurons for MDM funciona con cualquier IdP compatible con SAML 2.0. Se ha verificado que Microsoft Entra ID Authentication (Entra ID), Microsoft ADFS (Active Directory Federation Services), Okta, OneLogin, PingOne y PingFederate de Ping Identity funcionan con Ivanti Neurons for MDM.

Anteriormente, si se configuraba SAML auth/IdP, la autenticación SAML se utilizaba tanto para el registro de dispositivos como para la autenticación del portal. Ahora se ha habilitado un interruptor para elegir diferentes métodos de autenticación para el acceso al Portal de administración y el Registro de dispositivos. El interruptor solo es aplicable para el registro de dispositivos.

Durante el registro del dispositivo, el administrador puede omitir la opción del proveedor de identidad y dar al usuario la opción de autenticarse mediante un PIN, en lugar de usar la página del proveedor de identidad.

## Información general

- Si está usando Microsoft AD u otro directorio de LDAP local, tendrá que configurar Conector para conectarse e importar usuarios a Ivanti Neurons for MDM. Configure Conector o [**LDAP**](./Configuración_del_servidor_LDAP.md) si todavía no lo ha hecho.
- Cuando se añade un IdP, la autenticación del usuario cambia automáticamente de LDAP a IdP.
- Solo está permitido un proveedor de IdP.
- En caso de que su IdP se vuelva inaccesible, utilice la cuenta del Administrador de abonados (TA, en inglés) de Ivanti Neurons for MDM para acceder a este Portal de administración y solucionar el problema. La cuenta de TA es una cuenta local y no requiere autenticación externa. La cuenta de TA se crea cuando se aprovisiona su Ivanti Neurons for MDM y se proporciona información al contacto técnico de su organización o equivalente. Si no tiene la información de su cuenta de TA, contacte con su representante de asistencia técnica.
- Ivanti Neurons for MDM es compatible con Microsoft Entra ID (Entra ID) para autenticar usuarios durante el registro de dispositivos Windows 10.Establezca el tipo de autenticación para los usuarios de su LDAP utilizando las herramientas proporcionadas por su proveedor de IdP. El esquema de autenticación de su IdP tendrá prioridad sobre los ajustes de Ivanti Neurons for MDM. Los ajustes de autenticación se pueden encontrar aquí: **Usuarios > Ajustes del usuario > Ajuste del Registro de dispositivos > Tipo de autenticación del Registro de un dispositivo**.
- Las inscripciones en la inscripción de dispositivos de Apple y en dispositivos Configurator no emplean IdP para autenticar a los usuarios.
- Para configurar un proveedor de identidad para que funcione en el registro de dispositivos iOS y macOS de Apple Business Manager, debe activar los ajustes **Activar la inscripción personalizada** y los ajustes relacionados **página web alojada con Ivanti** que se encuentran en **Admin > Apple > Inscripción de dispositivos >&#x20;***editar un perfil de inscripción de dispositivos*. Consulte [**Inscripción de dispositivos**](./Inscripción_de_dispositivos.md) para obtener más información:

::Image[]{src="Resources/Images/idp001.png" signedSrc="Resources/Images/idp001.png" size="32" caption alt isUploading="false" sha initialPath="Resources/Images/idp001.png" githubPath="Resources/Images/idp001.png" position="flex-start" indent="2"}

## Tipos de configuración de IdP

La página de identidad de Ivanti Neurons for MDM le guía por la configuración de los siguientes tipos de proveedores de IdP:

- **Configuración de Ivanti Neurons for MDM IdP**: Los proveedores de Ivanti Neurons for MDM IdP compatibles son Entra ID, OneLogin, Okta y PingOne.
- **Configuración del IdP local**: los proveedores de IdP locales son ADFS 3.0, PingFederate 8.2.1 y PingFederate 8.1.3.
- **Configuración de IdP genérico**: esta es una ruta de configuración genérica que puede utilizar si no usa Microsoft ADFS, Okta, OneLogin ni PingFederate.

## Configuración de un proveedor de identidad (IdP)

**Procedimiento**

1. Vaya a **Administración&#x20;**> **Identidad** > **Autenticación con SAML**.
2. Haga clic en un tipo de configuración de proveedor de identidad:\* **Configuración de la IDP de Ivanti Neurons for MDM**
   - **Configuración de la IDP interna**
   - **Configuración de la IDP genérica**
3. Seleccione el correspondiente IdP. Si ha seleccionado **Configuración de la IDP genérica** en el paso 3, omita este paso y continúe desde el paso 5.
4. Siga las instrucciones en pantalla que aparecen para su IdP elegida.
5. Haga clic en **Hecho**.

Los administradores pueden iniciar sesión única durante un máximo de 2 horas desde su autenticación inicial con el IdP.

### Establecer las tareas que puede que necesite completar

Según su IdP elegida, se le guiará a través de las siguientes páginas y pasos asociados:

| **IdP**    | **Procedimiento** |
| ---------- | ----------------- |
| - Entra ID |                   |

- Okta
- OneLogin
- PingOne               | \* Generar una clave para cargar a su IdP.
- Iniciar sesión en su IdP y cargar una clave generada.
- Exporte un archivo de metadatos de su IdP e impórtelo a Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
  \| - ADSF 3.0
- PingFederate 8.2.1
- PingFederate 8.1.3 | \* Descargar el archivo de metadatos desde Ivanti Neurons for MDM.
- Configurar una «Relación de confianza para usuario autenticado» en ADFS o una «Conexión SP» en PingFederate e importar el archivo de metadatos de Ivanti Neurons for MDM.
- Exporte el archivo de metadatos de su IdP e impórtelo a Ivanti Neurons for MDM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \| - IdP genérica                                       | ::::WorkflowBlock

:::WorkflowBlockItem
Descargar el archivo de metadatos desde Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Siga las instrucciones que proporciona su proveedor de IdP para configurar el servidor de IdP o el servicio para comunicarse con el servicio de Ivanti Neurons for MDM como "Proveedor de servicios". Esto puede incluir:
:::

:::WorkflowBlockItem
1. Cargar el archivo de metadatos del paso 1 anterior a su IdP. Este archivo de configuración contiene la información esencial que permite a Ivanti Neurons for MDM, como proveedor de servicios SAML 2.0, comunicarse con su proveedor de identidad SAML 2.0. Las URL, certificados y ajustes estándar SAML 2.0 están incluidos en el archivo de metadatos.Ivanti Neurons for MDM espera una IdP compatible con SAML 2.0 para poder importar y procesar los metadatos XML exportados desde un Proveedor de servicios.
2. Configurar su IdP para que utilice RSA-SHA1 para firmar solicitudes de autenticación SAML. La información sobre el certificado de firmas utilizado para verificar las solicitudes de autenticación está incluido en el archivo de metadatos descargado en el paso 1.
3. Configuración de la IdP para que incluya un nombre de usuario en las respuestas de SAML que se envían a Ivanti Neurons for MDM. Especifique el nombre de usuario del elemento \[Name Id] de la respuesta SAML del IdP.
   Exporte un archivo de metadatos de su IdP e impórtelo a Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
(Opcional): incluir el nombre de usuario en la Solicitud de autenticación con SAML: para incluir el nombre de usuario del usuario que va a autenticarse en la solicitud de autenticación y para eliminar la información de un usuario adicional cuando se autentica una IdP. Si activa esta opción, es posible que se produzcan errores de autenticación. Si está seguro de la validación de IdP, seleccione la opción **Entiendo el impacto de este cambio** y ajuste **Incluir nombre de usuario en la solicitud de autenticación con SAML** como **ACTIVO**.Ivanti Access es una IdP validada para este ajuste.
:::

\:::: |

## Habilitar a los usuarios locales omitir la autenticación de IDP

Cuando se cae la conectividad de un IdP o Ivanti Neurons for MDM y es necesario solucionar el problema desde el lado de Ivanti Neurons for MDM, algunos administradores necesitan poder iniciar sesión en Ivanti Neurons for MDM sin depender de sistemas externos, como LDAP o IdP, para la autenticación. Solo los usuarios locales con funciones de administrador del sistema pueden omitir la autenticación IdP.

Crear una lista de usuarios locales para omitir la autenticación IdP

**Procedimiento**

1. Haga clic en **Administrador > Identidad**.
2. En la sección «Omisión de la autenticación IdP para los usuarios locales», haga clic en **+Añadir usuarios.**
3. De la lista que muestra solo los usuarios locales con funciones de administración del sistema, seleccione algunos usuarios.
4. Haga clic en **Guardar**.

Para eliminar a un usuario de la lista de usuarios locales que pueden omitir la autenticación IdP, haga clic en el icono eliminar que hay junto a la entrada que desee eliminar.

Si no puede ver la página de Identidades, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Sistema de solo lectura
