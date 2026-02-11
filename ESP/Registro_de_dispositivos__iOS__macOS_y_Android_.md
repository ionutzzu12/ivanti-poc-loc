---
title: Registro de dispositivos (iOS, macOS y Android)
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Instalar el perfil de administración manualmente**](./Registro_de_dispositivos__iOS__macOS_y_Android_.md)
- [**Enviar una invitación (iOS, macOS, and Android)**](./Registro_de_dispositivos__iOS__macOS_y_Android_.md)
- [**Pedir a los usuarios finales que se descarguen la aplicación (iOS y Android)**](./Registro_de_dispositivos__iOS__macOS_y_Android_.md)

La mayoría de los usuarios comienzan por registrar un dispositivo. Para iniciar el proceso de registro, puede hacerlo de cualquiera de las siguientes formas:

- Envíe una invitación a uno o más usuarios finales (registro de iReg)
- Pida a los usuarios finales que descarguen Go (registro en la aplicación)

Si la inscripción en MDM de dispositivos iOS y macOS falla con el mensaje Error en la instalación del *perfil El servidor SCEP ha devuelto una respuesta no válida.*. error, el usuario del dispositivo debe reiniciar el proceso de inscripción del dispositivo desde el principio. Esto ocurre sobre todo cuando el usuario del dispositivo tarda más de lo esperado en completar el proceso de inscripción en MDM de dispositivos iOS y macOS después de descargar el perfil en el dispositivo. Póngase en contacto con el servicio de asistencia de Ivanti para obtener más información.

Ivanti Neurons for MDM es compatible con la gestión a nivel de usuario de un solo usuario (usuario local o usuario registrado en Active Directory (AD)) en dispositivos macOS. Los administradores pueden gestionar dispositivos para los usuarios, aplicar perfiles de dispositivos y de usuarios y, por ende, usar la App Store, la distribución de aplicaciones, configuraciones y políticas (como Apps\@Work, restricciones y seguridad).

Para administrar dispositivos macOS con un usuario de AD, el usuario de AD tiene que ser el usuario que ha iniciado sesión durante el registro. Cualquier otro usuario no registrado no podrá ver los perfiles específicos para los usuarios registrados (por ejemplo, las certificaciones de identidad o la VPN). Sin embargo, las configuraciones a nivel de dispositivo sí podrán verlas y usarlas cualquier usuario que haya iniciado sesión.

El usuario [**final debe tener una cuenta**](./Usuarios.md) en Ivanti Neurons for MDM antes de poder iniciar el proceso de registro del dispositivo. Para los usuarios de LDAP, esto significa que deben tener configurados un [**Connctor**](./Conector.md) y un [**servidor LDAP**](./Configuración_del_servidor_LDAP.md) y que el usuario debe importarse del servidor LDAP. Para los usuarios locales, esto implica [**añadir un usuario**](./Usuarios.md).

La URL de inscripción de dispositivos generada en las versiones anteriores de Ivanti Neurons for MDM dejará de funcionar en la versión actual. El administrador deberá regenerar la URL de inscripción de dispositivos para el registro el dispositivo.

## Instalar el perfil de administración manualmente

**Aplicable a:**

- iOS 12.2 hasta la versión más reciente compatible con Ivanti Neurons for MDM.
- macOS 11.0 hasta la versión más reciente compatible con Ivanti Neurons for MDM.

### Registro de dispositivos de iOS

Durante el registro en la aplicación en dispositivos iOS:

- Durante el registro del dispositivo con Go app aparece una página con instrucciones para instalar el perfil.
- Haga clic en la opción **Instalar el perfil descargado** y haga clic en **Entendido**.
- El perfil descargado es válido durante algunos minutos, después de los cuales será obligatorio volver a registrarse.

### Registro del dispositivo macOS

Para el registro del dispositivo macOS en el portal de autoservicio, el usuario debe realizar los siguientes pasos:

**Procedimiento**

1. Iniciar sesión con sus credenciales.
2. En la página Instalar perfil de administración, el perfil se descarga en el sistema local del usuario.
3. Haga doble clic en el perfil descargado para hacerlo visible en las Preferencias del sistema del usuario.Hay un tiempo limitado para que el usuario instale el perfil antes de que quede invalidado.
4. Abra **Perfiles** en Preferencias del sistema. Cuando el perfil se descarga en el dispositivo, los usuarios pueden ver una página web con el enlace Perfiles. Haga clic en **Perfiles** para abrir la aplicación Ajustes.
5. Haga clic en **Instalar** para instalar el perfil de administración.
6. Continúe y termine el procedimiento de instalación. Introduzca la contraseña del sistema cuando se le solicite.

## Enviar una invitación (iOS, macOS, and Android)

Comience el proceso de registro enviando una invitación. Ivanti Neurons for MDM Cloud ofrece las siguientes formas de enviar una invitación a los usuarios finales para que registren un dispositivo:

- En el [**Asistente de inicio**](./Introducción.md)
- al [**añadir uno o más usuarios**](./Usuarios.md)
- en la página Usuarios ([**Acciones > Enviar invitación**](./Invitar_a_usuarios.md))

Si el usuario final pierde la invitación, puede compartir la URL que se listó en la invitación. Asegúrese de que agrega **/go** al final de la URL.

Los usuarios finales que tengan una cuenta de Ivanti Neurons for MDM con una contraseña no necesitan una invitación para iniciar el proceso de registro. Puede enviarles la URL que se lista en la invitación.

## Pedir a los usuarios finales que se descarguen la aplicación (iOS y Android)

La aplicación Go está disponible para dispositivos de Android y de iOS. Puede proporcionar instrucciones a los usuario finales sobre cómo descargar la aplicación desde una tienda de aplicaciones pública e iniciar el proceso de registro desde la aplicación. La invitación del correo electrónico contiene la información siguiente:

- Un vínculo a la página de registro
- Un PIN de un solo uso (si lo ha ajustado el administrador)
- Instrucciones básicas para los pasos siguientes

Si ya ha establecido una contraseña para la cuenta, ahora puede enviar la contraseña a la dirección de correo electrónico corporativo del usuario final. Si está utilizando LDAP para la autenticación, informe al usuario final de que son necesarias credenciales de red.

Si el usuario no completa la instalación del perfil de MDM durante el registro, Ivanti Neurons for MDM enviará periódicamente notificaciones push al dispositivo para pedir al usuario que complete el proceso de registro.

El usuario puede usar el nombre de usuario y la constraseña o escanera el código QR para iniciar el registro del dispositivo desde Go app. Los detalles son los siguientes:

- **Nombre de usuario**: dirección de correo electrónico
- **Contraseña**: si se especifica en los [**Ajustes de usuarios**](./Ajustes_del_usuario.md) y el administrador define una contraseña temporal
- **Código QR**: genere el código QR desde el portal de autoservicio de Ivanti Neurons for MDM. Cuando intenta escanear el código QR mediante la opción **Escanear código QR**, aparece un aviso en la pantalla que solicita al usuario que dé permiso de acceso a la cámara del dispositivo. Después de dar permiso, la cámara escanea el código QR y se registra el dispositivo. Esta opción es compatible con Android 9 o posterior, iOS 14 y versiones posteriores.

Como usuario final, si recibe un correo electrónico de registro en su dispositivo móvil, pulse el enlace para empezar el proceso de registro. Si recibe un correo electrónico en un equipo de sobremesa o portátil, introduzca la URL en el navegador del dispositivo móvil para iniciar el proceso de registro.  

Si aun no tiene definida una contraseña para su cuenta de usuario de Ivanti Neurons for MDM o si [**Ajustes de usuario**](./Ajustes_del_usuario.md) requieren un PIN de registro, se incluye un PIN de un solo uso. Después de ingresar el PIN, al usuario final se le pedirá que establezca una contraseña para la cuenta si no existe ya una.

Para dispositivos de Android Enterprise, cuando se completa el registro, se desinstalan los certificados de CA instalados manualmente en un perfil de trabajo de los dispositivos de la empresa o de los dispositivos administrados de trabajo.

### Reinscripción de dispositivos iOS

Si desea volver a inscribir su dispositivo, puede hacerlo de la siguiente manera:

1. Iniciar el cliente Go en el dispositivo.
2. Vaya a **Configuración** > **Solución de problemas** > **Vuelva a registrar el dispositivo**. El proceso de reinscripción se inicia y muestra algunas solicitudes de confirmación.
3. Pulse **Sí** en las indicaciones.

Si pulsa **Cancelar** durante la instalación del perfil, el proceso de inscripción se detiene y el servidor Ivanti Neurons for MDM desactiva el MDM del dispositivo.

Para reiniciar el proceso de reinscripción debe volver a instalar el perfil ya descargado. El perfil descargado solo es válido durante unos minutos, después debe realizar la reinscripción desde el cliente Go.

**Re-registrando dispositivos Android**

El administrador puede volver a registrar un dispositivo mediante las operaciones de retirar, borrar o eliminar sin borrar manualmente la entrada activa existente. Este método es más útil, concretamente, para re-registros donde la nueva entrada y la entrada existente pertenecen al mismo abonado. La página de Dispositivos muestra el estado de los dispositivos en el portal administrativo de Ivanti Neurons for MDM de la manera siguiente:

- **Activo**: el dispositivo se ha registrado correctamente
- **Retirado**: el dispositivo se restablece y se mostrará el estado retirado
- **Borrado**: el dispositivo se restablece y se mostrará el estado borrado
- **Restablecer**: se restablece el dispositivo y quedará en estado activo en el servidor hasta el próximo registro

La página de Audit Trails lista el registro del dispositivo, el re-registro y los estados retirados de dispositivos Android. Para obtener más información, consulte [**Trabajar con widgets**](./Trabajar_con_widgets.md).

Para Android 9.x y versiones anteriores, se mostrará una única entrada después de volver a registrarse. En el caso de Android 10.x y versiones posteriores, se mostrarán múltiples entradas. No obstante, solo la entrada más reciente estará activa y las anteriores quedarán en estado retirado.
