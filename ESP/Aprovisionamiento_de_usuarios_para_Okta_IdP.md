---
title: Aprovisionamiento de usuarios para Okta IdP
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Establecer una conexión con Ivanti Neurons for MDM**](./Aprovisionamiento_de_usuarios_para_Okta_IdP.md)
- [**Aprovisionar a usuarios y grupos**](./Aprovisionamiento_de_usuarios_para_Okta_IdP.md)
- [**Verificar el aprovisionamiento de usuarios asignados**](./Aprovisionamiento_de_usuarios_para_Okta_IdP.md)
- [**Verificar el aprovisionamiento de grupos**](./Aprovisionamiento_de_usuarios_para_Okta_IdP.md)
- [**Editar ajustes**](./Aprovisionamiento_de_usuarios_para_Okta_IdP.md)
- [**Configure los atributos personalizados/de empresa en el aprovisionamiento de usuarios de SCIM**](./Aprovisionamiento_de_usuarios_para_Okta_IdP.md)

## Establecer una conexión con Ivanti Neurons for MDM

********Ivanti Neurons for MDMDespués de crear los usuarios y grupos en su aplicación Okta, puede establecer la conexión entre Okta y .

**Procedimiento**

1. Inicie sesión en **Okta**.
2. Vaya a **Aplicaciones** > **Aplicaciones** > **Navegue por App Catalog**.
3. Busque **Agregar aplicación de prueba de SCIM 2.0** (titular del token de OAuth) e instale la aplicación.
4. Haga clic en la aplicación y vaya a **Aprovisionamiento** > **Integración**.
5. Haga clic en **Editar** y proporcione la url base y pegue el token generado.
6. Haga clic en **Guardar**.
7. Vaya a **Aprovisionamiento** y haga clic en **Editar**.
8. Habilite las acciones de usuario necesarias y haga clic en **Guardar**.

## Aprovisionar a usuarios y grupos

Una vez establecida la conexión entre **Okta** y Ivanti Neurons for MDM, puede aprovisionar usuarios o grupos.

**Procedimiento**

1. Vaya a **Asignaciones** > **Asignar** > **Asignar a personas** o **Asignar a grupo**.
2. 2\. Seleccione o busque un usuario o grupo existente y haga clic en **Asignar**.
3. Repita el proceso para añadir más **Usuarios** o **Grupos**.
4. Haga clic en **Hecho**.
5. Seleccione el grupo y pulse **forzar Grupo por nombre** para guardar y sincronizar el grupo.

## Verificar el aprovisionamiento de usuarios asignados

Después de aprovisionar a un usuario asignado en el portal Okta, verifique el aprovisionamiento del usuario en el portal administrativo Ivanti Neurons for MDM.

**Procedimiento**

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a la pestaña **Usuarios** que hay bajo el menú principal. El usuario aprovisionado estará presente en la lista de usuarios de esta página.

## Verificar el aprovisionamiento de grupos

Después de que se aprovisione un grupo en el portal de Okta, verifique el aprovisionamiento en Ivanti Neurons for MDM.

**Procedimiento**

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a la pestaña **Usuarios** y haga clic en **Grupos de usuarios**. El grupo aprovisionado estará presente en la lista de los grupos de esta página.

## Editar ajustes

Este tema le ayuda a configurar los ajustes de Okta.

**Procedimiento**

1. Vaya a **Administración&#x20;**>**&#xA0;Identidad&#x20;**>**&#x20;Okta de aprovisionamiento de usuarios**.
2. Haga clic en **Editar ajustes**.
3. Ajustar **Invitar automáticamente a los usuarios importados desde Okta**: administre si los usuarios importados de Okta a Ivanti Neurons for MDM son invitados automáticamente a registrarse por correo electrónico.
4. (Opcional) Haga clic en **Añadir atributo personalizado**: especifique los atributos de usuario personalizados que desee aplicar a la administración de dispositivos desde su servicio de directorio. Cada atributo puede estar referenciado por $\{attributeName} en los campos de configuración que admitan variables. El uso de esta opción requiere una implementación uniforme de los atributos personalizados en los servidores de Okta. Si un servidor Okta incluido en la implementación no usa el atributo personalizado, es posible que las características que dependen de este atributo personalizado no funcionen como deberían. La columna **Tipo de atributo** muestra el atributo **IDP** en la tabla **Atributos personalizados** de la sección **Editar**.
5. Haga clic en **Guardar\*\*\*\*cambios** después de modificar los ajustes de Okta.

## Configure los atributos personalizados/de empresa en el aprovisionamiento de usuarios de SCIM

**Procedimiento**

1. Vaya a **Administración&#x20;**>**&#xA0;Identidad&#x20;**>**&#x20;Aprovisionamiento de usuarios**.
2. Haga clic en **Editar ajustes**.
3. Introduzca el atributo personalizado (por ejemplo, custAttr1) y haga clic en **Guardar cambios**.
4. Desde el Portal de Okta, haga clic en **Directorio** > **Editor de perfiles**.
5. Haga clic en **Aplicación de prueba SCIM 2.0** aplicación **Usuraio (titular del token de OAuth)**.
6. Haga clic en **Agregar atributo**.
7. Añada los valores de atributo personalizados siguientes, por ejemplo: \* Nombre en pantalla (el mismo valor de atributo personalizado que proporcionamos en N-MDM, consulte el paso 3).
   - Nombre Variable : custAttr1
   - Nombre externo: custAttr1
   - Nombre de espacio externo: **urn\:ietf\:params\:scim\:schemas\:extension\:ivanti**:&#x32;**.0\:User**
   - Permiso de usuario : (Lectura / Escritura)
8. Haga clic en **Guardar atributo**.
9. Haga clic en **Editor de perfiles** > **Asignaciones**. Verá dos secciones para las asignaciones (SCIM y Okta).
10. Asigne los atributos personalizados creados en N-MDM a los atributos definidos en Okta y guarde las asignaciones.
11. Vaya a **Usuarios** y haga clic en el usuario deseado.
12. Para editar los atributos, haga clic en **Perfil** > **Editar**.
13. Vaya a **Aplicaciones** > aplicación **Aplicación de prueba de SCIM 2.0 (titular del token OAuth)**.
14. En la pestaña **Asignaciones**, haga clic en **Asignar** y seleccione **Asignar a personas**.La ventana **Asignar aplicación de prueba de SCIM 2.0 (Titular del token de OAuth) a Personas** aparece en la pantalla.
15. Seleccione el usuario deseado y haga clic en **Asignar**.
16. Haga clic en **Hecho**.

Para verificar el atributo personalizado y su asignación en Ivanti Neurons for MDM:

- Vaya a **Usuarios** > **Usuario** (cualquier usuario específico) > **Atributos**. Asegúrese de que el atributo personalizado asignado para Okta está visible en la sección Atributos de usuario.
