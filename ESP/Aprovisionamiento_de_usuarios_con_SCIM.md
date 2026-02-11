---
title: Aprovisionamiento de usuarios con SCIM
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Aprovisionamiento de usuarios**](./Aprovisionamiento_de_usuarios_con_SCIM.md)
- [**Generar un token desde Ivanti Neurons for MDM**](./Aprovisionamiento_de_usuarios_con_SCIM.md)
- [**Cambie el estado del Token**](./Aprovisionamiento_de_usuarios_con_SCIM.md)
- [**Ver el estado del token desde Pruebas de auditoría**](./Aprovisionamiento_de_usuarios_con_SCIM.md)
- [**Configurar los atributos de Aprovisionamiento de SCIM**](./Aprovisionamiento_de_usuarios_con_SCIM.md)

## Aprovisionamiento de usuarios

El aprovisionamiento de usuarios utiliza el protocolo SCIM para sincronizar un IdP con Ivanti Neurons for MDM y permite la sincronización parcial de usuarios y grupos. El aprovisionamiento de usuarios utiliza el protocolo SCIM para crear y actualizar automáticamente objetos de usuario y grupo procedentes de un IdP a Ivanti Neurons for MDM. Al igual que la integración actual con Entra ID y Okta, el proceso de aprovisionamiento de usuarios y grupos está automatizado; si se realizan cambios en el usuario o grupo en IdP, los mismos cambios se reflejan en Ivanti Neurons for MDM.

Dado que el valor del nombre de usuario es único en Ivanti Neurons for MDM, si el usuario ya está aprovisionado, el atributo Nombre principal del usuario no se puede actualizar en el IdP.

## Generar un token desde Ivanti Neurons for MDM

Para iniciar el aprovisionamiento de usuarios para un IdP, genere un token y la URL de destino desde Ivanti Neurons for MDM.

Asegúrese de que guarda el token y la URL de destino.

Se pueden generar un máximo de 2 tokens en cualquier momento.

**Procedimiento**

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a **Administración&#x20;**>**&#xA0;Identidad&#x20;**>**&#x20;Aprovisionamiento de usuarios**.
3. Seleccione Proveedor de identidades (IdP) en la lista desplegable.
4. Para generar un nuevo token, haga clic en **Generar**. Aparece un mensaje de notificación, haga clic en **Generar**. Se abre una nueva página con detalles del token y de la URL SCIM de destino.
5. Haga clic en **Copiar** para copiar el token o la URL de SCIM.
6. Actualizar la página. La página **Aprovisionamiento de usuarios** muestra la tabla Estado del token.

## Cambie el estado del Token

Puede cambiar el estado de un token existente.

**Procedimiento**

1. Haga clic en el menú desplegable **Seleccionar** de la página **Aprovisionamiento de usuarios de Entra ID**.
2. Haga clic en **Seleccionar** y lleve a cabo los cambios siguientes en el token:\* **Establecer en Activo**
   - **Establecer en Inactivo**
   - **Renovar**
   - **Quitar**

## Ver el estado del token desde Pruebas de auditoría

Puede ver los registros de acciones/eventos que se dieron en un token SCIM desde la sección Pruebas de auditoría. El token SCIM puede tener uno de los estados siguientes:

- Token SCIM creado: se ha creado un token SCIM.
- Token SCIM activado: se ha activado el token SCIM.
- Token SCIM desactivado: se ha desactivado el token SCIM.
- Token SCIM Renovado: se ha renovado el token SCIM.
- Token SCIM eliminado: se ha eliminado el token SCIM.

La columna DETALLES también enumera el nombre del proveedor SCIM (IDP), como Azure, Okta, etc. que facilita la comunicación con Ivanti Neurons for MDM.

## Configurar los atributos de Aprovisionamiento de SCIM

Esta sección describe cómo crear atributos personalizados y de empresa para un IdP durante el aprovisionamiento de usuarios.

## Asignación de atributos

Una vez establecida la conexión, puede asignar los atributos entre IdP y Ivanti Neurons for MDM. Ivanti Neurons for MDM es compatible con los siguientes atributos de usuario:

### Atributos centrales

- id
- Nombre de usuario
- Nombre en pantalla
- activo
- Nombre
- Apellido
- correos electrónicos
  Para Entra ID IdP, se admite IdP externo.

### Lista de atributos para los que se permite la operación de actualización

- displayName
- correos electrónicos
- Nombre
- Apellido
- activo
- urn\:ietf\:params\:scim\:schemas\:extension\:ivanti:2.0\:User
- urn\:ietf\:params\:scim\:schemas\:extension\:enterprise:2.0\:User

### Atributo personalizado

**Esquema**: urn\:ietf\:params\:scim\:schemas\:extension\:ivanti:2.0\:User:\<CustomAttribute123Name>

### Atributo de empresa

Actualmente solo se admite el atributo Departamento.

**Esquema**: urn\:ietf\:params\:scim\:schemas\:extension\:enterprise:2.0\:User\:department
