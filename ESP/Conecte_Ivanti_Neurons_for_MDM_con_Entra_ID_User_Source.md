---
title: Conecte Ivanti Neurons for MDM con Entra ID User Source
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Para trabajar con Entra ID (Entra ID), debe configurar Ivanti Neurons for MDM con detalles sobre su cuenta de Microsoft Entra ID. Se requiere una cuenta existente y configurada de Microsoft Entra ID. Esta solución requiere un conector local o LDAP.

Esta sección contiene los siguientes temas:

- [**Casos de uso**](./Conecte_Ivanti_Neurons_for_MDM_con_Entra_ID_User_Source.md)
- [**Uso de Entra ID**](./Conecte_Ivanti_Neurons_for_MDM_con_Entra_ID_User_Source.md)
- [**Configuración de Entra ID**](./Conecte_Ivanti_Neurons_for_MDM_con_Entra_ID_User_Source.md)

## Casos de uso

Puede conectar Ivanti Neurons for MDM con Entra ID para uno de los siguientes casos de uso:

- Trabajar con Microsoft Office 365
- Configure Microsoft Entra ID, Microsoft ADFS u otro proveedor de identidades (IdP) SAML 2.0 para la autenticación de usuarios.
- Configure Microsoft Entra ID como su fuente de usuario
- Sincronice usuarios desde Microsoft Entra ID y comience. Todos los usuarios y grupos de su dominio de Entra ID se sincronizarán con su instancia Ivanti Neurons for MDM.Se muestra una notificación en la página **Notifications** si se produce un error en la sincronización de Entra ID debido a los siguientes motivos:\* El servicio de Entra ID no está disponible
  - No están sincronizados con Entra ID todos los atributos del usuario
  - Algunos atributos del usuario no están sincronizados con Entra ID
- Actualmente no se admiten los entornos con múltiples IdP.
- Si no está utilizando Microsoft Entra ID como su fuente de usuarios, puede usar las cuentas locales u obtener los usuarios del LDAP. Para ello, es obligatorio utilizar un conector de Ivanti Neurons for MDM para acceder a los recursos locales del LDAP.
- Actualmente no se admite el uso de Microsoft Entra ID únicamente para la autenticación de usuarios ni el uso de un LDAP local para el directorio de usuarios.

## Uso de Entra ID

Para utilizar Entra ID, configure su proveedor de identidad para la autenticación de usuarios en uno de los siguientes métodos:

- Para utilizar Microsoft Entra ID tanto para el origen como para la autenticación de usuarios, configure Entra ID como su IdP. Vaya a **Administrador > Identidad > Configuración de IdP de Ivanti Neurons for MDM** y seleccione **Entra ID** en el menú.
- Para utilizar Microsoft Entra ID para el origen de usuarios y ADFS para la autenticación de usuarios, configure ADFS como su IdP. Vaya a **Administrador > Identidad >\*\*\*\*Configuración de IdP local&#x20;**&#x79; seleccione ADFS en el menú.
- Para utilizar un IdP SAML 2.0 distinto de Entra ID y utilizar ADFS para la autenticación de usuarios, vaya a  **Administración > Identidad >****Configuración de IdP genérica** y siga las instrucciones de la página.

Para obtener más información, consulte [**Configurar el proveedor de identidades**](./Configurar_el_proveedor_de_identidades.md).

## Configuración de Entra ID

Este tema le ayuda a configurar los ajustes de Entra ID.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Administración > Microsoft Azure > Fuente de usuarios de Entra ID**.
:::

:::WorkflowBlockItem
Especifique los siguientes detalles:
:::

:::WorkflowBlockItem
1. **Nombre de Entra ID**.
2. **Intervalo de sincronización**: Modifique la frecuencia con la que Ivanti Neurons for MDM sincroniza los datos de usuario de su Entra ID.
3. **Habilitar este Entra ID**: Utilice esta opción para habilitar o deshabilitar la instancia de Entra ID.
4. Seleccione **Invitar automáticamente a los usuarios importados desde Entra ID**: administrar si los usuarios importados desde Entra ID hasta Ivanti Neurons for MDM son invitados automáticamente a registrarse por correo electrónico.
5. Seleccione **ID de Apple administrada**: Elija sincronizar ID de Apple administrada para los usuarios de Entra ID.\* **Ninguna**
   - **Patrón**:\* **Dirección de correo electrónico del usuario**
     - **userUPN**
     - (Opcional) seleccione la opción «Incluir el subdominio "appleid"» para evitar conflictos con los ID de Apple existentes.
6. (Opcional) Haga clic en **Añadir atributo personalizado**: especifique los atributos de usuario personalizados que desee aplicar a la administración de dispositivos desde su servicio de directorio. Cada atributo puede estar referenciado por $\{attributeName} en los campos de configuración que admitan variables. El uso de esta opción requiere una implementación uniforme de los atributos personalizados en los servidores de Entra ID. Si un servidor de Entra ID incluido en la implementación no usa este atributo, es posible que las características dependientes de este atributo no funcionen como deberían.
   Haga clic en **Guardar** después de modificar los ajustes de Entra ID.
:::
::::
