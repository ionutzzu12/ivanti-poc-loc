---
title: Dispositivos iPad compartidos para empresas
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Los iPad compartidos para empresa están disponibles para las ID administradas de Apple que se creen en Apple Business Manager con iOS 13.4 o versiones compatibles más recientes.

- Los iPad compartidos permiten a las empresas compartir dispositivos entre varios empleados, sin dejar de ofrecer una experiencia personalizada.
- Los empleados pueden iniciar sesión con una ID de Apple administrada para empezar a cargar sus datos, incluidas sus cuentas de correo electrónico, archivos, la biblioteca de iCloud Photo, los datos de aplicaciones y más.
- Los datos se almacenan en iCloud, de manera que los empleados puedan iniciar sesión en los iPad compartidos propiedad de la empresa.

Los iPad compartidos se pueden usar en aplicaciones para sanidad, ventas e industria. Por ejemplo, doctores y enfermeras pueden compartir un iPad, ya que pueden acceder de manera segura al perfil de usuario único diseñado para ellos. En las tiendas de venta al por menor, se puede facultar a los trabajadores de primera línea para que tengan acceso a la información sobre los productos, los recursos y los conocimientos especializados para ayudar a los clientes y ofrecerles mejores experiencias de compra.

Cómo funciona

- Los dispositivos para iPad se agregan a Apple Business Manager y se inscriben mediante un perfil de inscripción automatizado con el modo compartido encendido.
- Los empleados inician sesión en el iPad compartido con una ID de Apple administrada y una contraseña que proporciona la empresa. El administrador de Apple Business Manager puede crear manualmente las cuentas para los usuarios o federar la creación de cuentas a un proveedor de identidades como Entra ID.
- Cada usuario puede tener su perfil personalizado cuando inicia sesión en el iPad compartido. Los administradores pueden distribuir aplicaciones basándose en roles de usuario, responsabilidades y departamento.
- Los usuarios pueden iniciar sesión como usuarios invitados en un iPad compartido. El inicio de sesión del usuario invitado está habilitado por defecto. Un usuario invitado no necesita iniciar sesión con una ID de Apple administrada ni una contraseña. El inicio de sesión del usuario invitado se puede deshabilitar si se selecciona la opción **Permitir la sesión de invitado para iPad compartido** como **Falso** en la configuración de [**Restricciones de iOS**](./Restricciones_de_iOS.md).
- Vaya a Ivanti Neurons for MD&#x4D;**> Dispositivos**, haga clic en el nombre del iPad compartido y haga clic en la pestaña **Usuarios** para ver la lista de usuarios del dispositivo y sus detalles (como la ID de Apple administrada, los Datos disponibles en bytes, los Datos usados en bytes, Tiene datos que sincronizar con Ivanti Neurons for MDM).
- Vaya a la pestaña **Registros**, desde los filtros, seleccione la acción **Notificar lista de usuario** para ver detalles adicionales del usuario.
- El inicio de sesión del usuario invitado de un iPad compartido es distinto al de la administración del usuario invitado de Ivanti Neurons for MDM. Por defecto, la cuenta de usuario invitado está desactivada en Ivanti Neurons for MDM. Para administrar un usuario invitado en un iPad compartido, habilite la cuenta del usuario invitado.
- La grabación de pantalla está disponible desde el Centro de control en los dispositivos de iPad compartidos.
- Ivanti Neurons for MDM admite una variable de sustitución para el ID de Apple gestionado, `${managedAppleID}`. Esta variable del sistema se muestra en la sección de atributos del sistema y en la sección de atributos del dispositivo.
- Ivanti Neurons for MDM Restringe que un administrador cambie la ID de Apple administrada de los usuarios residentes que se iniciaron registrado en el dispositivo de iPad compartido en el pasado junto con los usuarios iniciados actualmente. Si intenta cambiar la ID de Apple administrada, un mensaje de error indica que la ID de Apple administrada del usuario no se puede cambiar puesto que el usuario utiliza un iPad compartido.
- En el caso de las [**Aplicaciones y libros de Apple&#x20;**](./Apps_and_Books_de_Apple.md), las aplicaciones y los libros se instalan en dispositivos de iPad compartidos basados ​​en licencias basadas en dispositivos, independientemente de si las licencias basadas en dispositivos se seleccionan o no.

Requisitos previos

Asegúrese de que se cumplan los siguientes requisitos previos:

- Un iPad compartido requiere una ID de Apple administrada. Los administradores pueden crear las cuentas manualmente o federarlas a un proveedor de identidades como Entra ID.
- Los iPad compartidos deben tener la versión iOS 13.4 o ser compatibles con versiones más nuevas.
- Los dispositivos deben estar asociados con cuentas de Apple Business Manager.
- Los dispositivos deben contener un almacenamiento de 32 GB o más.

Tenga en cuenta los puntos siguientes:

- Ivanti Neurons for MDM evita determinadas configuraciones, como Código de acceso, para los iPad compartidos, puesto que Apple no es compatible con ellas. Estas configuraciones no se insertan en los dispositivos (Dispositivos > haga clic en el enlace del nombre de un dispositivo > pestaña Configuraciones).
- La configuración de [**Código de acceso**](./Configuración_del_código_de_acceso.md) no se aplica a los dispositivos de iPad compartidos, puesto que requieren ID de Apple administradas, que se asocian con las contraseñas, no con códigos de acceso. La acción Desbloquear del portal administrativo de Ivanti Neurons for MDM no borrará el código de acceso de un iPad compartido.
- Seleccione el canal del dispositivo o el canal de usuario durante la distribución de la [**Configuración de restricciones iOS**](./Restricciones_de_iOS.md) a dispositivos de iPad compartidos. Puede distribuir configuraciones separadas e implementar restricciones que solo se aplican al dispositivo o al canal de usuario.
- Ivanti Neurons for MDM verifica las cuentas caducadas y retira los dispositivos con propietarios que son cuentas caducadas. No obstante, para un iPad compartido, el propietario del dispositivo es el último usuario que ha iniciado sesión pero puede que no sea el propietario legal. Si caduca la cuenta de un propietario, Ivanti Neurons for MDM excluye los iPad compartidos de su retirada.
- Go para el cliente de iOS no es compatible para los iPad compartidos.
- Los usuarios no pueden llevar a cabo acciones como retirar y borrar en los iPad compartidos. Solo los administradores pueden llevar a cabo acciones de retirada y borrado desde el portal administrativo de Ivanti Neurons for MDM.
- Los administradores no pueden cambiar el propietario del iPad compartido desde el portal administrativo de Ivanti Neurons for MDM.
- Cero Sign-On no es compatible con dispositivos de iPad compartidos.
- Cuando se habilita el comando ListUsers, todas la ID de usuarios administradas y su hora de conexión se muestran en la Inscripción de dispositivos (parte de Apple Business Manager) en la pestaña **Admin**.

## Configurar un iPad compartido

Puede ajustar un iPad compartido y configurar los ajustes.

**Procedimiento**

1. Vaya a **Administración** > **Apple&#x20;**> **Inscripción de dispositivos.**
2. Añada el dispositivo a Apple Business Manager inscribiéndolo mediante un perfil de inscripción de dispositivos automatizado. Para obtener información sobre este procedimiento, consulte [**Inscripción de dispositivos**](./Inscripción_de_dispositivos.md).
3. En los ajustes de Inscripción de dispositivos, active:\* **Modo supervisado**.
   - **Modo multiusuario** en **iPad compartido para empresa**.
4. (Opcional) Cree una cuenta de usuario local. El dispositivo se registrará para este usuario. La autenticación, ya que este usuario solo aparece una vez durante el registro.
5. Restablecer el iPad compartido.El proceso de registro se inicia solo después del reinicio. El dispositivo tarda unos minutos en registrarse y configurarse como iPad compartido.
6. El propietario legal se asigna a la cuenta de usuario que registró el dispositivo. El administrador puede cambiar el propietario legal desde la página **Dispositivos**.
7. En la pantalla de inicio de sesión del dispositivo, introduzca las credenciales de ID de Apple administrada del usuario.\* De manera similar a los dispositivos de macOS, puede enviar las configuraciones de iPad compartidos a través del dispositivo o de los canales de usuario.
   - Las variables de sustitución de usuarios no se sustituyen en las configuraciones (incluida la configuración de aplicaciones administradas) que se envían en el canal del dispositivo.
   - Si el usuario activo de un iPad compartido no es un usuario administrado, la ID de Apple administrada no pertenece a ningún usuario del portal administrativo de Ivanti Neurons for MDM, el dispositivo no se asignará a nadie. Los usuario no estarán administrados: el administrador no puede enviar configuraciones del canal del usuario desde Ivanti Neurons for MDM.
   - Por defecto, el usuario invitado predeterminado creado por Ivanti Neurons for MDM está desactivado. Cuando un usuario invitado inicia sesión, el dispositivo no se asigna a ningún usuario y el usuario no se administra. Si el usuario invitado se debe administrar, el usuario invitado predeterminado creado por Ivanti Neurons for MDM debe estar habilitado y el dispositivo se debe asignar al usuario invitado predeterminado después de que el usuario invitado inicie sesión. A continuación, se puede administrar el usuario.
   - La información del propietario del dispositivo se muestra en la página Ivanti Neurons for MDM > **Dispositivos** y en los registros de dispositivos (página de detalles del dispositivo > **Registros**).

## Gestionar los propietarios legales de los iPad compartidos

Usted busca y visualiza los propietarios legales de los iPad compartidos mediante sus ID de correo electrónico desde la página del listado del dispositivo. Puede cambiar los propietarios legales de los iPad compartidos mediante la reasignación de los propietarios legales existentes a los nuevos propietarios legales. Si se reasigna el propietario legal de un iPad no compartido, Ivanti Neurons for MDM ignora la asignación.

Procedimiento

1. Vaya a **Dispositivos**.
2. Haga clic en el icono del engranaje y agregue la columna **Propietario legal** a la página de la lista de dispositivos.
3. Seleccione los iPad compartidos.
4. Haga clic en **Acciones > Asignar al propietario legal**.

## Enviar un correo electrónico al propietario legal de un dispositivo de iPad compartido

Puede enviar correos electrónicos al propietario legal de un iPad compartido.

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Haga clic en el nombre del iPad compartido.
3. Haga clic en el icono del **correo electrónico**.
4. Escriba el correo electrónico.
5. Haga clic en **Enviar**.

## Uso del atributo del modo multiusuario

Puede usar el atributo Modo multiusuario de los iPad compartidos en Ivanti Neurons for MDM.

**Procedimiento**

1. En la página **Dispositivos**, use el atributo **Modo multiusuario**.
2. Haga clic en **Búsqueda avanzada** y cree una regla para encontrar los dispositivos que usan el atributo **Modo multiusuario**.
3. En la página **Dispositivos > Grupos de dispositivos**, cree un grupo de dispositivos dinámicos para los iPad compartidos mediante el atributo **Modo multiusuario**. Por ejemplo, se puede utilizar este grupo como filtro de distribución para distribuir las configuraciones.
4. En la página **Políticas**, cree una política personalizada para los iPad compartidos mediante el atributo **Modo multiusuario**.
5. En **Aplicaciones > Filtro\*\*\*\*de distribución**, use el atributo **Modo multiusuario** para limitar el número de aplicaciones disponibles para su instalación.

- Ivanti Neurons for MDM no es compatible con el modo multiusuario para los dispositivos Apple School Manager. No se recomienda activar el ajuste e insertar el perfil de Inscripción de dispositivos a los dispositivos de Apple School Manager.
- La configuración de Inicio de sesión segura de múltiples usuarios no se aplica a los iPad compartidos.

## Eliminar usuarios de un iPad compartido

Puede eliminar una o varias cuentas de usuarios desde los iPad compartidos. En la pestaña Lista de usuarios, la etiqueta **Activo** se muestra para el usuario activo actualmente. La opción Eliminar no se puede aplicar al usuario que ha iniciado sesión en estos momentos en el iPad compartido. Los usuarios pueden eliminarse desde los **Dispositivos** o desde la pestaña **Usuarios**.

**Eliminar usuarios desde la pestaña Dispositivos**

**Procedimiento**

1. Vaya a la pestaña **Dispositivos** > **Detalles del dispositivo**.
2. Vaya a la pestaña **Usuarios**. Se muestra la lista de usuarios.
3. Haga clic en **Eliminar todos los usuarios**.
4. Haga clic en el signo menos "**-**" para eliminar usuarios específicos.\* (Opcional) En la ventana **Eliminar usuario**, seleccione la opción **Forzar la eliminación del usuario aunque esté pendiente la sincronización de los datos se hayan sincronizado con Ivanti Neurons for MDM** y haga clic en **Sí**.
   Seleccionar **Forzar Eliminar usuario aunque esté pendiente la sincronización de datos con Ivanti Neurons for MDM** forzará la eliminación del usuario aunque los datos no se hayan sincronizado aun con el portal administrativo de Ivanti Neurons for MDM.

**Eliminar usuarios desde la pestaña Usuarios**

**Procedimiento**

1. Vaya a la pestaña **Usuarios**.
2. Seleccione un usuario o varios, vaya al menú desplegable de **Acciones**, haga clic en **Eliminar**. Aparece un mensaje de confirmación. Después de confirmar, se emite el comando de eliminar usuario en los dispositivos.
3. Vaya a **Registros del dispositivo** en los detalles del dispositivo y verifique que el comando Eliminar usuarios se envía a los usuarios seleccionados del iPad compartido.

## Iniciar sesión a los usuarios desde un dispositivo de iPad compartido

El administrador puede cerrar las sesiones de los usuarios de un iPad compartido.

**Procedimiento**

1. En la página **Dispositivos**, seleccione un iPad compartido.
2. Seleccionar **Forzar Cierre de Sesión** del menú **Acciones**. Una solicitud emergente solicita la confirmación sobre la sesión de usuarios de registro del dispositivo de iPad compartido.
3. Haga clic en **OK** para forzar el cierre de sesión.
