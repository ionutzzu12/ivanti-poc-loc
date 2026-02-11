---
title: Desbloquear un dispositivo
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Desbloquear dispositivos Android**](./Desbloquear_un_dispositivo.md)
- [**Desbloquear AppConnect para aplicaciones Android**](./Desbloquear_un_dispositivo.md)
- [**Desbloquear un dispositivo iOS**](./Desbloquear_un_dispositivo.md)
- [**Desbloquear dispositivos de ChromeOS**](./Desbloquear_un_dispositivo.md)

Para desbloquear un dispositivo:

Puede eliminar el bloqueo de pantalla de un dispositivo. El desbloqueo funciona de forma algo diferente dependiendo del dispositivo.

**Procedimiento**

1. Vaya a **Dispositivos > Dispositivos**.
2. Seleccione los dispositivos.
3. Haga clic en **Acciones**.
4. Seleccione **Desbloquear**.
5. También puede hacer clic sobre el enlace del nombre del dispositivo para acceder a la página Detalles del dispositivo y hacer clic en el icono **Desbloquear**

::Image[]{src="Unlock_device_icon.png" signedSrc="Unlock_device_icon.png" size="10" caption alt isUploading="false" sha initialPath="Unlock_device_icon.png" githubPath="Unlock_device_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
y en **Aceptar**.
:::

## Desbloquear dispositivos Android

Cuando se recibe el comando Desbloquear, la aplicación Android intenta restablecer el código de acceso. En los modos Administrador del dispositivo y Propietario del dispositivo, el código de desbloqueo se restablece, mientras que en los modos Personal habilitado en el Propietario del perfil y Propietario de la empresa, se restablece el código de desbloqueo del perfil de trabajo.

El comando de desbloqueo proporciona una opción para que el administrador establezca el código de desbloqueo con una combinación de caracteres alfanuméricos. La opción predeterminada, que establece el código de desbloqueo en "0000", se puede realizar en varios dispositivos. Sin embargo, la nueva opción, Código de desbloqueo personalizado para Android, se puede realizar en un dispositivo de cada vez. El número mínimo de caracteres debe ser 6 y el máximo 8. Esta opción está disponible en la pestaña **Acciones**, así como en la página **Detalles del dispositivo**. Cuando selecciona la opción Desbloquear en la pestaña **Acciones** o en la página **Detalles del dispositivo**, puede ver las dos opciones siguientes.

- Predeterminada
- (Solo Android) Proporcionar un código de desbloqueo: puede proporcionar un código de desbloqueo de esta sección y hacer clic en **Desbloquear**.\* Omitir solicitud de restablecimiento del código de acceso en el dispositivo: seleccione esta opción para omitir el restablecimiento del código de acceso si la configuración del código de acceso se envía a un dispositivo.

Después de configurar el código de desbloqueo, el administrador puede encontrarlo en las páginas **Pruebas de auditoría** y **Registros del dispositivo**.

El desbloqueo Directboot solo funciona para la opción de desbloqueo por defecto, código de desbloqueo '0000'. El código de desbloqueo personalizado para el arranque directo no es compatible.

## Desbloquear AppConnect para aplicaciones Android

En las aplicaciones AppConnect, el comando **Desbloqueo de AppConnect** ayuda a desbloquear contenedores que hayan sido bloqueados porque los usuarios estaban intentando iniciar sesión varias veces con códigos de acceso incorrectos. Este desbloqueo no desbloqueará el dispositivo en sí.

## Desbloquear un dispositivo iOS

Cuando se recibe el comando Desbloquear, la aplicación iOS elimina el código de acceso de dispositivo. Si la [**configuración del código de acceso**](./Configuración_del_código_de_acceso.md) especifica que es necesario un nuevo código de acceso, se solicitará al usuario del dispositivo que establezca un nuevo código de acceso que cumpla con las reglas definidas en la configuración de códigos de acceso. El usuario debe realizar este cambio en los 60 minutos posteriores. De lo contrario, la aplicación forzará al usuario a que establezca un nuevo código de acceso.

## Desbloquear dispositivos de ChromeOS

Cuando un dispositivo de ChromeOS se selecciona y se hace clic en la opción **Desbloquear**, aparece una ventana en la pantalla con el mensaje : "Desbloquear puede borrar un código de acceso existente para habilitar el acceso de un usuario al dispositivo. Desbloquear es distinto según la plataforma". Haga clic en **Desbloquear** y el estado del dispositivo se actualizará a "Desbloquear enviado", y el estado actualizado se visualizará después de la sincronización periódica del dispositivo.
