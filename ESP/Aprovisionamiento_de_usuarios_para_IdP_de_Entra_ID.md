---
title: Aprovisionamiento de usuarios para IdP de Entra ID
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Aprovisionar a los usuarios y grupos asignados**](./Aprovisionamiento_de_usuarios_para_IdP_de_Entra_ID.md)
- [**Aprovisionar a todos los usuarios y grupos asignados**](./Aprovisionamiento_de_usuarios_para_IdP_de_Entra_ID.md)
- [**Verificar el aprovisionamiento de usuarios asignados**](./Aprovisionamiento_de_usuarios_para_IdP_de_Entra_ID.md)
- [**Aprovisionamiento de usuarios para IdP de Entra ID**](./Aprovisionamiento_de_usuarios_para_IdP_de_Entra_ID.md)
- [**Editar ajustes**](./Aprovisionamiento_de_usuarios_para_IdP_de_Entra_ID.md)
- [**Configure los atributos personalizados y de empresa**](./Aprovisionamiento_de_usuarios_para_IdP_de_Entra_ID.md)
- [**Notas importantes: SCIM&#xA0;**](./Aprovisionamiento_de_usuarios_para_IdP_de_Entra_ID.md)

## Establecer una conexión con Ivanti Neurons for MDM

Después de crear los usuarios y grupos en su aplicación Entra ID Enterprise, puede establecer la conexión entre Entra ID e Ivanti Neurons for MDM.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Inicie sesión en el portal Entra ID.
:::

:::WorkflowBlockItem
Vaya a **Aplicación de empresa** > haga clic en **+ Crear su propia aplicación**. Se abre la ventana Crear su propia aplicación.
:::

:::WorkflowBlockItem
Especifique el nombre de su aplicación (**Predeterminado: No galería**) y haga clic en **Crear**. Por ejemplo, Aprovisionamiento de usuario de Ivanti Neurons for MDM.
:::

:::WorkflowBlockItem
Vaya a **Aprovisionamiento** > **Editar aprovisionamiento** > **Credenciales del administrador**.
:::

:::WorkflowBlockItem
Copie y pegue la URL del SCIM de destino del portal de administración Ivanti Neurons for MDM en el campo **URL del abonado** del portal Entra ID.
:::

:::WorkflowBlockItem
Copie y pegue el código de acceso de Ivanti Neurons for MDM en el campo **Secret Token** del portal Entra ID.
:::

:::WorkflowBlockItem
Dé uno de los siguientes pasos:
:::

:::WorkflowBlockItem
- Seleccione **Sincronizar solo los usuarios y grupos asignados**. Para más información, consulte Aprovisionar usuarios y grupos asignados
- Seleccione **Sincronizar todos los usuarios y grupos**. Para obtener más información, consulte Aprovisionar todos los usuarios y gruposSeleccione la opción Sincronizar todos los usuario y grupos para migrar los usuario.
  Haga clic en **Comprobar conexión**. Una ventana emergente con una marca verde confirma la conexión.
:::

:::WorkflowBlockItem
Haga clic en **Guardar**.
:::

:::WorkflowBlockItem
Amplíe **Asignaciones** en la página **Aprovisionar** en el portal de Entra ID.
:::

:::WorkflowBlockItem
Haga clic en **Aprovisionar a usuarios de Entra ID**. Se abre la página de Asignación de atributos.
:::

:::WorkflowBlockItem
Haga clic en **Borrar** para borrar los atributos no admitidos.
:::
::::

## Aprovisionar a los usuarios y grupos asignados

Una vez establecida la conexión entre Entra ID y Ivanti Neurons for MDM, puede aprovisionar usuarios o grupos.

Al aprovisionar grupos, Entra ID no añade miembros de los grupos anidados al grupo seleccionado. Entra ID añade los miembros inmediatos y los nombres de grupo sólo al grupo y no a los miembros del subgrupo durante el proceso de sincronización.

**Procedimiento**

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. En la aplicación, vaya a **Usuarios y grupos** > haga clic en **+ Agregar usuario/grupo**. Se abre la página de Añadir Asignación.
3. Busque el usuario o el grupo desde el campo **Búsqueda**, haga clic en **Seleccionar**, y luego en **Asignar**. Se abre la página Usuarios y grupos.
4. Seleccione la casilla del usuario o grupo correspondiente.
5. Haga clic en**Aprovisionamiento** y luego haga clic en**Iniciar aprovisionamiento**. Se muestran los detalles de la configuración correcta.

## Aprovisionar a todos los usuarios y grupos asignados

Una vez establecida la conexión entre Entra ID e Ivanti Neurons for MDM, puede aprovisionar usuarios o grupos.

**Procedimiento**

- Haga clic en**Aprovisionamiento** y luego haga clic en**Iniciar aprovisionamiento**. La página se abre con los detalles del aprovisionamiento exitoso y el usuario será aprovisionado en Ivanti Neurons for MDM

## Verificar el aprovisionamiento de usuarios asignados

Una vez que un usuario asignado haya sido aprovisionado en el portal Entra ID, verifique el aprovisionamiento en el portal administrativo Ivanti Neurons for MDM.

**Procedimiento**

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a la pestaña **Usuarios** debajo del menú principal. El usuario que fue aprovisionado estará presente en la lista de usuarios de esta página.El proceso de aprovisionamiento puede durar hasta una hora.

## Verificar el aprovisionamiento de grupos

Una vez aprovisionado un grupo en el portal Entra ID, verifique el aprovisionamiento en Ivanti Neurons for MDM.

**Procedimiento**

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a la pestaña **Usuarios** > **Grupos de usuarios**. El grupo que se aprovisionó estará presente en la lista de los grupos de esta página.El proceso de aprovisionamiento puede durar hasta una hora.

## Editar ajustes

Este tema le ayuda a configurar los ajustes de Entra ID.

**Procedimiento**

1. Vaya a **Administrador > Microsoft Azure > Aprovisionamiento de usuarios de Entra ID**.
2. Haga clic en **Generar token** y copie el token.
3. Actualizar la página. Se abre la página ajustes de Entra ID.
4. Haga clic en **Editar ajustes**.
5. Ajuste **Invitar automáticamente a los usuarios importados desde Entra ID**: administre si los usuarios importados de Entra ID a Ivanti Neurons for MDM son invitados automáticamente a registrarse por correo electrónico.
6. Establecer **ID de Apple gestionada**: esta opción está desactivada por defecto. Haga clic en el botón de alternancia para activarlo y sincronizar el ID de Apple gestionado para los usuarios de Entra ID.\* **Dirección de correo electrónico del usuario**
   - (Opcional) seleccione la opción «Incluir el subdominio "appleid"» para evitar conflictos con los ID de Apple existentes.
7. (Opcional) Haga clic en **Añadir atributo personalizado**: especifique los atributos de usuario personalizados que desee aplicar a la administración de dispositivos desde su servicio de directorio. Cada atributo puede estar referenciado por $\{attributeName} en los campos de configuración que admitan variables. El uso de esta opción requiere una implementación uniforme de los atributos personalizados en los servidores de Entra ID. Si un servidor de Entra ID incluido en la implementación no usa este atributo, es posible que las características dependientes de este atributo no funcionen como deberían. La columna **Tipo de atributo** muestra el atributo **IDP** en la tabla **Atributos personalizados** de la sección **Editar**.
8. Haga clic en **Guardar\*\*\*\*cambios** después de modificar los ajustes de Entra ID.

## Configure los atributos personalizados y de empresa

**Procedimiento**

1. Vaya a **Administración&#x20;**>**&#xA0;Identidad&#x20;**>**&#x20;Aprovisionamiento de usuarios**.
2. En **Editar ajustes**, haga clic en **+Agregar atributo personalizado**.
3. Introduzca un nombre en el campo **Nombre del atributo** (por ejemplo, custAttr1) y haga clic en **Guardar cambios**. El atributo se lista y está disponible en la página **Administrador** > **Sistema** > **Atributo**. El atributo se indica como un atributo IdP y solo puede llevar a cabo la acción Eliminar.
4. Inicie sesión en el portal **Entra ID**.
5. Vaya a **Inicio**> **Aplicación Enterprise** > Haga clic en la aplicación SCIM.
6. Haga clic en **Aprovisionar a usuarios de Entra ID** en la sección **Asignaciones**.
7. Marque la casilla **Mostrar opciones avanzadas**.
8. Haga clic en **Editar la lista de atributos de customappsso**.
9. Introduzca una nueva entrada para el atributo personalizado que creó en la interfaz de usuario de Ivanti Neurons for MDM.
10. Añada el esquema para el atributo Personalizado/Empresa (Departamento) como se indica a continuación\:Atributo personalizado: **urn\:ietf\:params\:scim\:schemas\:extension\:ivanti**:&#x32;**.0\:User:\<custAttr1>**&#x63;onsulte el paso 3.Atributo de empresa: **urn\:ietf\:params\:scim\:schemas\:extension\:enterprise**:&#x32;**.0\:User\:department**
11. Haga clic en **Guardar cambios**.
12. Haga clic en **Agregar nueva asignación** y seleccione los atributos Origen y Destino en el menú desplegable:
13. Haga clic en **Aceptar** y en **Guardar asignación**.
14. Vaya a **Inicio**>**&#x20;Aplicación Enterprise** > Haga clic en la aplicación SCIM > **Usuarios y grupos**.
15. Haga clic en nombre de usuario. Se abre la página Perfil.
16. Verifique si el valor asociado con el atributo aparece en la página de Perfil.
17. (Opcional) haga clic en una aplicación de SCIM > Aprovisionamiento > Aprovisionamiento bajo demanda, busque el usuario específico y haga clic en Aprovisionamiento. Para validar las nuevas asignaciones de atributos llevadas a cabo en los pasos anteriores.
18. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
19. Vaya a **Usuario** > **Usuarios**.
20. Seleccione el usuario, haga clic en la pestaña **Atributos** y verifique el valor del atributo. El atributo se asigna para un usuario específico.

### Consideraciones sobre la migración: Entra ID User Source to User Provisioning SCIM

- Al migrar de Entra ID User Source a Entra ID User Provisioning (SCIM), seleccione Sync All Users and Groups (Sincronizar todos los usuarios y grupos).
- Una vez actualizados los usuarios y grupos con una fuente de Entra ID SCIM, vuelva a la página Aprovisionamiento de Azure en Azure y establezca los usuarios y grupos específicos que gestionará el Aprovisionamiento de usuarios Entra ID mediante la opción Sincronizar solo usuarios y grupos asignados.
- Ivanti Neurons for MDMCuando se completa la sincronización, puede eliminar a los usuarios y los grupos que no están definidos en Azure desde las listas de Usuarios y grupos.
- Cuando se inicia la migración, la página Entra ID User Source es accesible en un estado de solo lectura.

### Consideraciones sobre la migración: SCIM de aprovisionamiento LDAP a usuario

**Requisitos previos**:

:::Paragraph{listStyleType="decimal" indent="2"}
La opción **Activar este servidor LDAP** está seleccionada de forma predeterminada. Esta opción no debe estar seleccionada antes de la migración.
:::

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
Cree una aplicación empresarial en Entra ID, añada los usuarios/grupos LDAP sincronizados (los mismos usuarios/grupos LDAP presentes en Ivanti) a la aplicación SCIM. Inicie el aprovisionamiento.
:::

**Consideraciones clave para la migración de LDAP a SCIM**

- LDAP no captura toda la información de usuarios/grupos sincronizados, mientras que SCIM registra eventos de usuarios/grupos en registros de auditoría.
- El usuario LDAP con atributo personalizado tiene el tipo ldap definido, mientras que para SCIM, es IdP. Así pues, cuando los usuarios con atributos personalizados se migran de LDAP a SCIM, se debe crear el atributo personalizado de IdP correspondiente en la aplicación SCIM y los usuarios se migrarán. Cuando el usuario desee actualizar el atributo personalizado ldap más adelante, el valor del atributo ldap.custom no se actualizará en MDM después de la migración. Se actualizará el valor del atributo IdP.
- Migrar usuarios LDAP que estén asociados con uno o varios atributos personalizados, específicamente "ldap.custAttr1", que indica el registro del dispositivo LDAP y la configuración (Configuración del certificado de identidad) enviada al dispositivo con el tipo SAN correspondiente al valor del LDAP. atributo personalizado.
- Migrar un usuario LDAP donde el ID de Apple administrado está asociado con la dirección de correo electrónico. Por lo tanto, antes de la migración de LDAP a SCIM, si el usuario desea conservar el valor del ID de Apple administrado del usuario de LDAP, el ID de Apple administrado en SCIM debe estar habilitado y la configuración debe ser guardado.
- Cuando se elimina el usuario LDAP en el servidor LDAP, el usuario sigue activo pero el indicador Sin sincronización está establecido en verdadero para ese usuario LDAP sincronizado en particular. En el caso de SCIM, cuando se elimina un usuario aprovisionado, el estado del usuario se desactiva.
- Una vez que SAML esté configurado para el proveedor de identidad (IdP) para usuarios SCIM, todos los usuarios de diversas fuentes, como local y LDAP, se autenticarán a través de SAML. Solo se pueden agregar usuarios locales a una lista de excepciones para evitar el flujo de autenticación del IdP. Esta configuración se puede administrar en la página SAML en **Administrador** > **Identidad** > **SAML**.
- Una vez que se configura SAML para los usuarios de IDP (SCIM) migrados, se puede omitir el registro del dispositivo (no a través de IDP) para otros usuarios de distintas fuentes, como locales y LDAP. Esto se puede administrar en **Usuarios** > **Configuración de usuario**.
- En LDAP, se admiten usuarios, grupos y unidades organizativas, mientras que en SCIM, se admiten usuarios y grupos, pero no unidades organizativas.
- El proceso de aprovisionamiento de grupos anidados no es compatible con SCIM.

### Notas importantes: SCIM 

- La dirección de correo electrónico es un campo obligatorio para el aprovisionamiento y la migración de usuarios o miembros.
- SCIM proporciona aprovisionamiento unidireccional desde Microsoft Entra ID a Ivanti Neurons for MDM. Ivanti Neurons for MDM no ofrece ninguna opción de sincronización. Si elimina un grupo o usuario aprovisionado SCIM de Ivanti Neurons for MDM, asegúrese de eliminar también el usuario o grupo de Microsoft Entra ID.
- Puede utilizar un atributo (origen o destino) sólo una vez en la ventana de asignación de aplicaciones SCIM en Microsoft Entra ID. No se puede asignar dos veces la misma fuente a un atributo de destino específico.
- Los usuarios inactivos no se pueden aprovisionar o migrar a Ivanti Neurons for MDM mediante SCIM.
- Actualmente, Ivanti Neurons for MDM no es compatible la notificación de eventos SCIM.
- La duración de la migración o el aprovisionamiento depende del número de usuarios o grupos implicados.
- Microsoft Azure controla el intervalo de aprovisionamiento y es de aproximadamente 40 minutos o más.
- Durante el reaprovisionamiento, Microsoft Entra ID solo reintentará las entradas que hayan fallado. Puede descargar los registros de aprovisionamiento para verificar los usuarios que han tenido éxito o han fallado en el aprovisionamiento desde Microsoft Entra ID.
- En SCIM no se permiten grupos duplicados de diferentes fuentes.
- Cuando un usuario aprovisionado se elimina de Microsoft Entra ID, el usuario se desactiva en Ivanti Neurons for MDM.
- Cuando un grupo de usuarios aprovisionado se elimina de Microsoft Entra ID, el grupo se elimina en Ivanti Neurons for MDM y los miembros independientes que pertenecen al grupo eliminado se desactivan y se asocian a Grupo de todos los usuarios.
- Cuando un miembro aprovisionado de un grupo aprovisionado se elimina en Microsoft Entra ID, el miembro se desactiva en Ivanti Neurons for MDM; sin embargo, el miembro sigue asociado al grupo en Ivanti Neurons for MDM.
- Cuando se elimina una asignación de atributo (atributo de empresa o atributo personalizado) de una aplicación, el valor del atributo eliminado se sigue reflejando en Ivanti Neurons for MDM.
- Cuando un atributo de usuario de un usuario aprovisionado se actualiza con un valor en blanco o vacío, el valor actualizado del atributo no se refleja en Ivanti Neurons for MDM.
- Si los atributos de usuario FName y LName (name.formatted) están en blanco durante la migración o actualización de Microsoft Entra ID a SCIM, la migración o actualización falla.
- Si elimina un usuario en Entra ID, la API SCIM correspondiente no elimina el usuario permanentemente, sino que realiza un borrado suave y cambia el estado del usuario de activo a inactivo. Si desea eliminar permanentemente el usuario, inicie sesión en el portal administrativo de Ivanti Neurons for MDM y elimine manualmente el usuario inactivo/deshabilitado.
- Cuando ya existe un usuario local en Ivanti Neurons for MDM con un ID de usuario determinado, se aprovisionará un usuario similar con el mismo ID de usuario desde Entra ID a MDM, la fuente de usuario se actualizará de Local a SCIM Entra ID.
- Entra ID con suscripción "Entra ID Premium P1" tiene el privilegio de aprovisionar el grupo requerido para ser asignado y aprovisionado.
