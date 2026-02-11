---
title: Añadir usuarios
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Añadir usuarios**](./Añadir_usuarios.md)
- [**Añadir múltiples usuarios**](./Añadir_usuarios.md)
- [**Añadir múltiples usuarios cargando un archivo**](./Añadir_usuarios.md)
- [**Añadir un administrador**](./Añadir_usuarios.md)
- [**Usuario «nadie»**](./Añadir_usuarios.md)
- [**Visualizar la información del PIN para el registro del dispositivo**](./Añadir_usuarios.md)

Puede añadir un solo usuario o varios usuarios a la vez. Una vez que haya añadido varios usuarios, le recomendamos que [**filtre**](./Encontrar_y_filtrar_usuarios.md) la visualización para mostrarle solamente los que le interesan.

A continuación mencionamos otras cosas que puede hacer con los usuarios en esta página:

- [**Asignarlos**](./Asignar_usuarios_a_grupos_de_usuarios.md) a un grupo de usuarios o [**eliminarlos&#x20;**](./Quitar_usuarios_de_grupos_de_usuarios.md)de este
- [**enviar un mensaje**](./Enviar_un_mensaje.md)
- [**invitarlo a registrarse**](./Invitar_a_usuarios.md)
- [**asignar funciones**](./Asignar_funciones_a_usuarios.md)
- [**cambiar una contraseña**](./Cambiar_una_contraseña.md)
- [**eliminar**](./Eliminar_a_un_usuario.md)
- [**generar un pin**](./Registro_de_dispositivo_por_generación_de_PIN.md)

Todos los perfiles del propietario del dispositivo están asignados a una cuenta de dispositivo. Las cuentas de dispositivos no tienen ninguna restricción en el número de dispositivos asignados. Los perfiles de trabajo (propiedad del empleado) son cuentas del usuario asignadas.

## Añadir a un usuario

**Procedimiento**

1. Vaya a **Usuarios.**
2. Haga clic en **+ Añadir** (arriba a la derecha).
3. Seleccione **Un solo usuario**.
4. Complete el formulario con la información del usuario:\* Dirección de correo electrónico
   - Nombre
   - ApellidosEl campo del nombre de usuario muestra la dirección de correo electrónico que ha introducido. En la mayoría de los casos, no debe editar este campo predeterminado. Para obtener más información, consulte [**Cuándo editar un nombre de usuario**](./Editar_un_nombre_de_usuario.md)\* Nombre en pantallaSi desea cambiar el nombre en pantalla de este usuario, edite el texto predeterminado en el campo **Nombre en pantalla**.
5. Si desea asignar una contraseña, ingrésela en los campos **Contraseña&#x20;**&#x79; **Confirmar contraseña**.
   - Si asigna una contraseña, debe comunicársela al usuario para que pueda registrar sus dispositivos.
   - Si no asigna ninguna contraseña, el usuario tendrá que crear una contraseña cuando registre sus dispositivos.
6. Seleccione **Configuración regional** en la lista desplegable.
7. Introduzca **ID de Apple administrada**. Puede incluir «appleid» como subdominio para la ID de Apple administrada con el fin de evitar cualquier conflicto con las ID de Apple existentes. Por ejemplo, [**usuario@appleid.sudominio.com**](mailto\:usuario@appleid.sudominio.com). El subdominio tiene que ser un subdominio verificado válido de Apple Business Manager.
8. No puede actualizarse la cuenta con una Id de Apple administrada diferente si hay un dispositivo inscrito como usuario activo con la Id de Apple administrada de la cuenta actual.
   (Opcional) Asigne uno o más grupos de usuarios. La ID de Apple administrada no se puede actualizar cuando hay un dispositivo con el estado «Activo» y «Retirada pendiente».
9. Si desea configurar otras características antes de invitar a este usuario, desactive la opción **Enviar esta invitación ahora**. De lo contrario, se enviará el correo electrónico con la invitación cuando haga clic en **Hecho**.
10. Haga clic en **Hecho** para añadir al usuario.

En el caso de los dispositivos Android, las cuentas de dispositivos están diseñadas para dispositivos administrados de un solo uso, en los que una sola cuenta de servicio local puede utilizarse para inscribir un gran número de dispositivos. Al crear un nuevo usuario, debe estar activada la Cuenta de dispositivo empresarial Android disponible en **Administrador > Google > Android Enterprise**. Las cuentas de dispositivo están activadas de forma predeterminada (en lugar de las cuentas de usuario) para las inscripciones de cuentas de Google Play gestionadas por el propietario del dispositivo.

Marque la casilla **Cuenta de dispositivo con Android Enterprise** para permitir que se asigne automáticamente una Cuenta de dispositivo Google a las inscripciones de dispositivos administrados en el trabajo con Android Enterprise vinculadas a esta cuenta.

Al editar un usuario local o LDAP para dispositivos Android, a los dispositivos de la cuenta de Google Play administrada por el propietario del dispositivo de Android Enterprise asociados al usuario se les asignarán cuentas de dispositivo en el siguiente registro de dispositivos, siempre que se cumplan las siguientes condiciones:

- Que esté activada esta función seleccionando la casilla **Cuenta de dispositivo con la versión corporativa de Android**.
- Que la aplicación Go del dispositivo Android tenga la versión 47 o posterior.

## Añadir múltiples usuarios

**Procedimiento** :

1. Vaya a **Usuarios.**
2. Haga clic en **+ Añadir** (arriba a la derecha).
3. Seleccione **Usuarios múltiples**.
4. Puede introducir direcciones de correo electrónico **Manualmente** de manera predeterminada. Escriba o peque las direcciones de correo electrónico de los usuarios separadas por comas.
5. Por ejemplo: [**jperez@miempresa.com**](mailto\:jperez@miempresa.com), [**lruiz@miempresa.com**](mailto\:lruiz@miempresa.com), [**nvillalba@miempresa.com**](mailto\:nvillalba@miempresa.com)
   Si desea configurar otras características antes de invitar a este usuario, desactive la opción **Enviar esta invitación ahora**.
6. De lo contrario, se enviará el correo electrónico con la invitación cuando haga clic en **Hecho**.
   Haga clic en **Hecho** para añadir a los usuarios.

## Añadir múltiples usuarios cargando un archivo

**Procedimiento**:

1. Vaya a **Usuarios.**
2. Haga clic en **+ Añadir** (arriba a la derecha).
3. Seleccione **Usuarios múltiples**.
4. Seleccione **Cargar CSV**.
5. Haga clic en **Descargar plantilla CSV**.
6. Edite la plantilla con la siguiente información para cada usuario:\* Id. de usuario (obligatoria)
   - dirección de correo electrónico (obligatoria)
   - contraseña
   - nombre
   - apellidos
   - Nombre en pantalla
   - grupos de usuarios
   - atributos personalizados
7. Esta es la misma información que usted introduce al [**añadir a un solo usuario**](./Añadir_usuarios.md). No supere las 10 000 entradas en el archivo.
   Guarde el archivo.
8. Arrástrelo al área de cargas o seleccione **Cargar CSV** para seleccionar el archivo.
9. Una vez que aparezca la información cargada sobre el usuario, haga las modificaciones pertinentes.
10. Haga clic en **Siguiente** (abajo a la derecha).
11. Si no desea enviar invitaciones directamente, seleccione **No enviar invitaciones.**
12. Haga clic en **Hecho**.

## Añadir un administrador

**Procedimiento** :

1. Haga clic en **Añadir** (arriba a la derecha).
2. Seleccione **Un solo usuario**.
3. Complete el formulario con la información del usuario:\* Dirección de correo electrónico
   - Nombre
   - Apellidos
4. El campo **nombre de usuario** muestra la dirección de correo electrónico que ha introducido.
   Si desea cambiar el nombre para mostrar de este usuario, edite el texto predeterminado en el campo **Nombre para mostrar**.
5. Asigne una contraseña en el campo **Contraseña**.
6. Introduzca de nuevo la contraseña en el campo **Confirmar contraseña**.
7. Haga clic en **Hecho** para añadir al usuario.
8. Comunique la contraseña a la persona que le ayudará a administrar los dispositivos.

## Usuario «nadie»

El usuario «nadie» es un usuario predeterminado que no puede eliminarse. El servicio aplica este usuario a los dispositivos que no tienen ningún usuario asociado, como por ejemplo los dispositivos retirados.

## Visualizar la información del PIN para el registro del dispositivo

Mientras se añaden nuevos usuarios, a los administradores les aparecerá la información del PIN generado para el registro si el Tipo de autenticación del registro de dispositivos está establecida en Solo PIN. Esta información puede resultar útil para asistir a los usuarios con inscripciones de dispositivos.

- Para usuarios individuales, el PIN aparece a través de la acción **Usuarios > Invitar usuario a registrarse** y también en la sección Información del PIN de la página Detalles del usuario.
- Para múltiples usuarios, los PIN aparecen en forma de columna en la página Lista de usuarios además de las columnas «Estado del PIN» (válido o caducado), «PIN emitido», y «PIN caduca».

Si no puede realizar las tareas en la página **Usuarios**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Administración de usuarios
