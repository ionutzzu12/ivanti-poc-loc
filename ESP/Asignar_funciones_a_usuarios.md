---
title: Asignar funciones a usuarios
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Puede dar a los usuarios acceso a datos de Ivanti Neurons for MDM y funciones mediante la asignación de [**roles**](./Funciones_del_usuario.md). Puede asignar funciones directamente a los usuarios o a grupos de usuarios. Al asignar una función a un grupo de usuarios, se da esa función a todos los usuarios de ese grupo.

El rol de usuario de solo lectura no se asigna por defecto a los usuarios.La página Roles y las opciones asociadas están ocultas para los abonados que tienen acceso a Ivanti Neurons for UEM y Ivanti Neurons for MDM.

Los usuarios no pueden asignar los permisos que ya no tienen. Los permisos y las funciones que no están asignados a los usuarios no se muestran para su selección. En este caso, se mostrará un mensaje de error. Cuando un administrador de Ivanti Neurons for MDM o un administrador asociado intenta asignar roles a un administrador socio, Ivanti Neurons for MDM muestra un mensaje que indica que un administrador asociado debe llevar a cabo esta operación en el Portal del proveedor de servicios.

Para obtener más información sobre las funciones, consulte [**Roles\_Management.htm**](./Administración_de_funciones.md).

**Procedimiento:**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a:
:::

:::WorkflowBlockItem
- **Usuarios > Usuarios***o*
- Usuarios > Grupos de usuarios.
  Seleccione uno o más usuarios o grupos de usuarios.
:::

:::WorkflowBlockItem
Haga clic en **Acciones**.
:::

:::WorkflowBlockItem
En la página de detalles del Usuario o la página de detalles del Grupo de usuarios, haga clic en **Asignar funciones&#x20;***o*En la página Lista de usuarios o Lista de grupos de usuarios, seleccione **Anexar funciones**.
:::

:::WorkflowBlockItem
Seleccione una o más de las siguientes funciones que desee asignar:
:::

:::WorkflowBlockItem
- Administración del sistema | Multiespacio
- Sistema de solo lectura | Multiespacio
- Gestión de usuarios | Multiespacio
- Solo lectura del usuario | Multiespacio
- Importación del usuario e invitación de LDAP | Multiespacio
- Administración de dispositivos | Específico del espacio
- Dispositivo de solo lectura | Específico del espacio
- Administración de aplicaciones y contenidos | Específico del espacio
- Solo lectura de aplicaciones y contenidos | Específico del espacio
- Acciones de dispositivos | Específico del espacio
- Operaciones ISE de Cisco | Multiespacio
- Administración de tareas programadas | Multiespacio
- Servicios de plataformas comunes (CPS) | Multiespacio
- Gestión de la migración de bajo impacto en los usuarios | Multiespacio
- Inscripción de dispositivos personalizados | Multiespacio
- Editar Editar Microsoft Graph | Multiespacio
- Enviar/Cancelar borrado | Multiespacio
- Ver Microsoft Graph | Multiespacio
- Administrar integración de Access | Multiespacio
  Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Si los roles seleccionados están unidos por Espacio, entonces los Espacio seleccione todos los roles unidos a Espacios.
:::

:::WorkflowBlockItem
Si solo hay un espacio (Espacio predeterminado), el paso Especificar espacio se omitirá cuando se asigne una función vinculada al espacio.

La página de resumen mostrará el nombre del espacio para el turno vinculado al espacio como espacio predeterminado.

Revise el resumen de las funciones que va a asignar y haga clic en **Hecho**.
:::
::::

## Dar permiso al personal de soporte técnico para que usen las acciones básicas de los dispositivos

Las funciones de soporte técnico, por lo general, permiten al personal visualizar datos. No obstante, algunas organizaciones prefieren incluir las acciones básicas de los dispositivos:

- Forzar ingreso
- Bloquear
- Desbloquear
- Enviar mensaje
- Retirar
- Borrar

**Procedimiento**

Puede dar permiso a las acciones.

1. Vaya a **Usuarios > Usuarios**\* &#x6F;**\* Usuarios > Grupos de usuarios**.
2. Seleccione uno o más usuarios o grupos de usuarios.
3. Haga clic en **Acciones**.
4. En la página de detalles del usuario o la página de detalles del grupo de usuarios, seleccione **Asignar funciones&#x20;***o*Desde la página de Lista de usuarios o Lista de grupos de usuarios, seleccione **Anexar roles**.
5. Seleccione **Solo lectura del dispositivo**.
6. Seleccione **Acciones de dispositivos**.
7. Haga clic en **Hecho**.

Asegúrese de que ha seleccionado Dispositivo de solo lectura antes de seleccionar las Acciones del dispositivo para los usuarios que tengan permisos inesperados.
