---
title: Administración de funciones
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Las funciones son grupos de permisos empaquetados que permiten otorgar un conjunto de permisos a un usuario administrativo, a la vez que limitan su acceso para controlar áreas específicas de funcionalidad. Ivanti Neurons for MDM proporciona un conjunto de funciones del sistema que se pueden asignar (o editar) y un centro para crear funciones personalizadas. Desde Neurons for MDM 118 puede buscar permisos específicos según la categoría y se muestran todas las opciones que se relacionan con el permiso o rol específico en la IU. Se muestra un tooltip para los permisos que se añaden como permisos dependientes.

La página Gestión de roles y las opciones asociadas están ocultas para los abonados convergentes que tienen acceso a Ivanti Neurons for UEM y Ivanti Neurons for MDM.

Hay dos tipos de permisos disponibles y, por lo tanto, dos tipos de funciones:

- **Roles específicos para un espacio**: los permisos son específicos para un espacio y, por lo tanto, se aplican únicamente a un espacio específico. Algunos ejemplos son la administración de dispositivos y la administración de aplicaciones dentro de un espacio.
- **Roles para todos los espacios**: los permisos pueden, por su naturaleza, aplicarse a todos los roles. Algunos ejemplos son los ajustes a nivel de abonado, como los certifcados MDM y los ajustes del App Catalog.

## Crear una función personalizada

Puede crear funciones personalizadas multiespacio o específicas para cada espacio. Cuando seleccione un permiso, los permisos dependientes se seleccionarán automáticamente. Por consiguiente, un usuario con una función personalizada solo puede realizar las acciones específicas disponibles (como retirar o borrar) cuando el usuario visite la página Dispositivos o la página Detalles del dispositivo.

Cuando se aplica el rol personalizado Ver PIN de registro de usuario, los usuarios pueden ver el PIN de otros usuarios que tienen el mismo nivel de acceso o con menores privilegios y los usuarios no pueden crear PIN para otros usuarios.

La función personalizada recién creada no se puede asignar a nadie automáticamente. El superadministrador de abonados debe asignarla a los usuarios administradores requeridos que, posteriormente, podrán asignarla a otros usuarios según sea necesario.

**Procedimiento**

1. Vaya a **Administrador** > **Administración de roles**.
2. Haga clic en **+Añadir función personalizada**.
3. En la página **Crear rol**, introduzca el **Nombre** del nuevo rol.
4. (Opcional) agregue una descripción para el nuevo rol.
5. En **Tipo de rol**, seleccione una de las siguientes opciones:\* **Función de espacios cruzados**
   - **Función específica para espacios**
6. En **Permisos**, seleccione los permisos granulares requeridos.
7. Consulte la siguiente tabla para conocer los permisos de Administrador y de Usuario.
   Haga clic en **Guardar**.

La tabla siguiente lista los permisos, roles y atributos que puede usar para crear un rol personalizado:

| **Tipo de función**              | **Categoría de permiso**             | **Permisos pormenorizados**     |
| -------------------------------- | ------------------------------------ | ------------------------------- |
| **Función de espacios cruzados** |                                      |                                 |
| **Administrador**                |                                      |                                 |
|                                  | Administrar atributos personalizados | - Añadir atributo personalizado |

- Eliminar atributo personalizado
- Editar atributo personalizado
- Ver atributo personalizado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
  \|                                      | Administradores de asistencia técnica          | \* Añadir administradores de asistencia técnica
- Eliminar administradores de asistencia técnica
- Desactivar administradores de asistencia técnica
- Ver administradores de asistencia técnica y mostrar historial del inicio de sesión                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
  \|                                      | Autoridad de certificados                      | - Añadir Entidad de Certificación
- Eliminar Entidad de Certificación                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
  \|                                      | Conector                                       | \* Añadir registros de Conector
- Eliminar registros de Conector
- Ver Conector
- Actualizar Conector                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
  \|                                      | Gestión LDAP                                   | - Añadir usuario/grupo/OU
- Añadir servidor
- Navegar por el servidor
- Borrar servidor
- Buscar en servidor
- Sincronizar servidor
- Quitar usuario/grupo/OU
- Ver ServicioTodos los permisos de LDAP de esta sección requieren el permiso de Ver conector. Se seleccionará automáticamente en la sección Conector cuando seleccione cualquiera de estos permisos de LDAP.                                                                                                                                                                                                                                                                                                                                                                                                         |
  \|                                      | Gestión de licencias                           | Ver licencias                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
  \|                                      |                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \| **Usuarios**                         |                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \|                                      | Acciones de administración del usuario         | \* Ver usuario
- Actualizar usuario
- Enviar mensaje al usuario
- Añadir/asignar funciones al usuario
- Crear usuario
- Eliminar Usuario
- Invitar usuario
- Ver PIN de registro de usuario                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \|                                      | Asignar atributo personalizado del usuario     | - Borrar atributo
- Ver atributos
- Añadir/editar atributo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
  \|                                      | Grupos de usuarios                             | \* Ver Grupo de usuarios
- Editar grupo de usuarios
- Añadir/asignar funciones al Grupo de usuarios
- Crear grupo de usuarios
- Eliminar grupo de usuarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \|                                      | Gestión de informes                            | - Crear informe
- Editar informe
- Ejecutar informe
- Borrar registro de informe
- Ver informe
- Borrar informe
- Descargar registro de informes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| **Dispositivos**                     |                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \|                                      | Inscripción en masa                            | \* Crear inscripción en masa
- Actualizar inscripción en masa
- Asignar usuario a la inscripción en masa
- Ver inscripción en masa
- Eliminar inscripción en masa                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| **Función específica para espacios** |                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \| **Dispositivos**                     |                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \|                                      | Acciones de dispositivos                       | - Asignar dispositivo al usuario
- Eliminar bloqueo de activación de dispositivos
- Eliminar dispositivo
- Deshabilitar Modo perdido de dispositivo
- Habilitar Modo perdido de dispositivo
- Ingreso forzoso del dispositivo
- Bloquear dispositivo
- Desbloquear dispositivo
- Cierre de sesión forzado del dispositivo
- Reinstalar aplicaciones del sistema de dispositivos
- Reiniciar el dispositivo
- Programar actualizaciones de dispositivos iOS
- Renunciar a la propiedad de un dispositivo
- Retirar dispositivo
- Cancelar Retirar dispositivo
- Apagar el dispositivo
- Ver el dispositivo
- Borrar dispositivo
- Cancelar Borrar dispositivo
- Actualizar la versión de SO del dispositivo
- Asignación en masa a través de la Carga
- Iniciar sesión de TeamViewer |
  \|                                      | Asignar atributo del dispositivo personalizado | \* Añadir/editar atributo personalizado del dispositivo
- Eliminar atributo personalizado del dispositivo
- Ver atributo personalizado del dispositivoTodos los permisos de Asignar atributo del dispositivo personalizado de esta sección requieren el permiso de Lectura de dispositivos. Se seleccionará automáticamente en la sección Acciones del dispositivo cuando seleccione cualquiera de estos permisos de Asignación de atributos del dispositivo personalizado.                                                                                                                                                                                                                                                                                                          |
  \|                                      | Configuraciones del dispositivo                | - Excluir perfil
- Insertar perfil
- Insertar perfil excluido
- Reinstalar tras error                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
  \|                                      | Grupos de dispositivos                         | \* Añadir un nuevo Grupo de dispositivos
- Eliminar grupo de dispositivos
- Editar grupo de dispositivos
- Ver grupo de dispositivos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
  \|                                      | Inscripción en masa                            | - Crear inscripción en masa
- Actualizar inscripción en masa
- Asignar usuario a la inscripción en masa
- Ver inscripción en masa
- Eliminar inscripción en masa                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \|                                      | Inventario de aplicaciones                     | \* Ver inventario de aplicaciones                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
  \| **Configuraciones**                  |                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \|                                      | Configuraciones                                | - Ver/exportar configuraciones
- Editar/Priorizar configuraciones
- Añadir/Duplicar configuraciones
- Borrar configuraciones                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| **Políticas**                        |                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
  \|                                      | Políticas                                      | \* Ver políticas
- Editar/Priorizar políticas
- Añadir/Duplicar políticas
- Eliminar políticas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

|   |
| - |
|   |

Para editar una función, vaya a la página Administración, Administración de funciones y haga clic en el icono de editar que está en **Acciones** junto al nombre de la función. Un usuario no puede cambiar una función de espacios cruzados a función específica para espacios y viceversa.

**Temas relacionados**:

- Para asignar una función personalizada a un usuario, consulte [**Asignar funciones**](./Asignar_funciones_a_usuarios.md).
- Consulte [**Funciones de usuario**](./Funciones_del_usuario.md) para ver una lista de funciones predeterminadas.
- [**Uso de Informes personalizados**](./Uso_de_Informes_personalizados.md)
