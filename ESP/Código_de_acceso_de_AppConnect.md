---
title: Código de acceso de AppConnect
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Cambiar/restablecer un código de acceso**](./Código_de_acceso_de_AppConnect.md)
- [**Generar un PIN de un solo uso para restablecer un código de acceso de Secure Apps para dispositivos iOS**](./Código_de_acceso_de_AppConnect.md)

Si lo desea, puede establecer que sea obligatorio un código de acceso de AppConnect, también conocido como el código de acceso de las aplicaciones seguras. Con un inicio de sesión único con el código de acceso de AppConnect, el usuario del dispositivo puede acceder a todas las aplicaciones seguras. En el Portal de administración, se pueden configurar las reglas para el código de acceso de AppConnect. El código de acceso de AppConnect no es igual que el código de acceso que se utiliza para desbloquear el dispositivo.

## Cambiar/restablecer un código de acceso

Los usuarios pueden cambiar o restablecer el código de acceso para aplicaciones seguras en la aplicación Secure Apps Manager para dispositivos Android y en la aplicación Go para iOS, siempre que se haya permitido en la configuración de AppConnect. Para dispositivos iOS:

**Procedimiento**

1. Abra la aplicación Go para iOS.
2. Haga clic en **Secure Apps**.
3. Haga clic en **Autenticación**.
4. Haga clic en **Cambiar código de acceso de Secure Apps** y siga las instrucciones para cambiar/restablecer el código de acceso.

Para dispositivos Android:

1. Abra la aplicación Secure Apps Manager.
2. Haga clic en **Cambiar código de acceso** en el menú de opciones.
3. Haga clic en **¿Olvidó su contraseña?** para restablecer el código de acceso.

## Generar un PIN de un solo uso para restablecer un código de acceso de Secure Apps para dispositivos iOS

Los administradores pueden configurar Ivanti Neurons for MDM para permitir que los usuarios de dispositivos iOS restablezcan su código de acceso de aplicaciones seguras (AppConnect) cuando se lo olviden. Cuando se configura esta opción, los usuarios de dispositivos que se registraron con Ivanti Neurons for MDM mediante un nombre de usuario y contraseña pueden introducir dichas credenciales en Go 3.1.0 para iOS o versiones más recientes compatibles para autenticarse y, a continuación, restablecer el código de acceso de sus aplicaciones seguras. No obstante, los usuarios de dispositivos que hayan olvidado la contraseña y el PIN necesitarán un mecanismo diferente para autenticarse.

**Procedimiento**

1. En Ivanti Neurons for MDM, el administrador activa la opción **Código de acceso de Secure Apps** en la configuración predeterminada de iOS AppConnect (o en cualquier otra configuración de iOS AppConnect).
2. El usuario genera un PIN de un solo uso para un dispositivo iOS específico en el portal de autoservicio del usuario haciendo clic en la opción **Restablecer código de acceso de Secure Apps** y siguiendo las instrucciones. El PIN de un solo uso es válido durante 30 minutos.
3. En Go para iOS en un dispositivo, el usuario sigue las instrucciones para restablecer un código de acceso olvidado de Secure Apps.
4. Cuando se le soliciten sus credenciales de usuario, este deberá introducir su nombre de usuario y el PIN de un solo uso en lugar de su código de acceso normal.
5. A continuación, el usuario podrá restablecer su código de acceso de las aplicaciones seguras.
