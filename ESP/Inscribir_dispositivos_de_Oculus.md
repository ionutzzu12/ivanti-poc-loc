---
title: Inscribir dispositivos de Oculus
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM ahora puede administrar dispositivos de Quest for Business (dispositivos Oculus). Actualmente, Meta es compatible con dispositivos de Oculus for Business (OFB) y Quest for Business (QFB) para MDM. Debe llevar a cabo algunas tareas básicas en la consola Meta para hacer que los dispositivos estén listos para MDM y, a continuación, registrarse con Ivanti Neurons for MDM.

Puede inscribir la flota de dispositivos Oculus en el Gestor de dispositivos de la consola de Meta Workplace. Debe iniciar sesión en el Oculus Business Workplace mediante las credenciales compartidas con el correo electrónico registrado. En la página de Inicio, se mostrará la información de Todos los dispositivos en la sección de Flota de dispositivos. La sección de Flota de dispositivos proporciona una vista general de todos los dispositivos disponibles en Administración de dispositivos. Estos detalles incluyen el Nombre de dispositivo, Estado de dispositivo, SO (Sistema operativo), Modelo, etc.

Esta sección contiene los siguientes temas:

- Requisitos previos para inscribir los dispositivos Oculus
  - [**Cómo ajustar una aplicación de MDM en el Administrador de dispositivos**](./Inscribir_dispositivos_de_Oculus.md)
  - [**Cómo ajustar el dispositivo Oculus**](./Inscribir_dispositivos_de_Oculus.md)
    Registre un dispositivo OFB con MobileIron Go
  - [**En la consola de Ivanti Neurons for MDM**](./Inscribir_dispositivos_de_Oculus.md)
  - [**En clientes de Go**](./Inscribir_dispositivos_de_Oculus.md)

## Requisitos previos para inscribir los dispositivos Oculus

### Cómo ajustar una aplicación de MDM en el Administrador de dispositivos

Los dispositivos/auriculares se proporcionan y actualizan con, al menos, la versión **28** de **Oculus for Business**. En la consola de Meta, el administrador debe ajustar un MDM en el Administrador de dispositivos y asignar los dispositivos Oculus al servicio MDM específico.

**Procedimiento**

1. En la página de inicio de **Oculus Business Workplace** , seleccione **Aplicaciones**.
2. En la **Biblioteca de aplicaciones**, haga clic en la aplicación MDM de terceros que desee instalar y, a continuación, haga clic en **Actualizar**.
3. Seleccione el MDM correcto para la aplicación en la lista de **Administración de dispositivos móviles** y, a continuación, haga clic en **Actualizar aplicación**.
4. Haga clic en el auricular del dispositivo Oculus en el que desee instalar el MDM. La información del dispositivo aparecerá en pantalla.
5. En la pestaña **Acerca de**, baje hasta **Administrador de dispositivos móviles**.
6. Haga clic en el botón **Editar** que hay junto a la opción **Autoridad de MDM**.
7. Por defecto, se seleccionará la opción Administrador de dispositivos de Oculus. Debe seleccionar la aplicación MDM Authority y seleccionar **MobileIron Go** en la lista de aplicaciones de MDM Authority.
   Haga clic en **Guardar**. El dispositivo se restablece automáticamente y, a continuación, deberá configurar el dispositivo Oculus mediante la aplicación de configuración.

### Cómo ajustar el dispositivo Oculus

Puede agregar dispositivos de auriculares de Oculus Quest 2 mediante la aplicación de Configuración del dispositivo. Esta aplicación debe compartirse con los usuarios necesarios para que estos puedan descargar e instalar la aplicación en sus dispositivos Android.

**Procedimiento**

1. En la sección **Flota de dispositivos**, haga clic en **Dispositivos sin configurar**.
2. Haga clic en **Obtener la aplicación de configuración**. La página **Enviar enlace de descarga** aparece en la pantalla.
3. Seleccione uno o más miembros del equipo en la lista o haga clic en **Agregar destinatario** para seleccionar en la lista.
4. Haga clic en **Enviar enlace**. Los usuarios seleccionados recibirán un correo electrónico con un enlace para instalar la aplicación de **Configuración del dispositivo**.
5. Haga clic en el enlace **Descargar la aplicación de configuración del dispositivo** en el correo electrónico para instalar la **Aplicación de configuración del dispositivo** en su dispositivo Android.
6. Después de descargarla, esta aplicación no aparecerá en la tienda de aplicaciones de su dispositivo. Debe obtenerlo desde la sección de Descargas del dispositivo e instalarlo.
   Abra la aplicación **Oculus for Business** desde su dispositivo Android.
7. ENCIENDA los dispositivos Oculus pulsando el botón de encendido durante 2 segundos.
8. Active el Bluetooth y coloque el dispositivo Android cerca de los dispositivos Oculus hasta que se complete la configuración.
9. Busque dispositivos Oculus mediante el Bluetooth de su dispositivo Android.
10. Cuando se encuentre el dispositivo Oculus necesario, debe conectarlo a una red WiFi para completar la configuración.
11. Haga clic en **Introducir información de Wi-Fi** y proporcione el Nombre de la red y la contraseña y haga clic en **Guardar**. Ahora, el dispositivo Oculus está conectado a la red WiFi.
12. Haga clic en **Iniciar configuración**. Aparece una notificación en pantalla indicando el progreso de la configuración, y no debe cerrar la aplicación ni manipular los auriculares durante la configuración.
    Aparece una confirmación en pantalla. Puede seguir buscando más dispositivos mediante el botón **Encontrar más dispositivos**.

## Registrar un dispositivo OFB con MobileIron Go

### En la consola de Ivanti Neurons for MDM

Se puede registrar un dispositivo OFB con MobileIron Go en la consola de Ivanti Neurons for the MDM. No obstante, la configuración del modo Work Managed Device Non-GMS (AOSP) (en **Configuraciones**) debe distribuirse a estos grupos de dispositivos OFB.

### En clientes de Go

Se puede registrar un dispositivo OFB en el cliente de MobileIron Go. Debe llevar a cabo las tareas siguientes para registrar el dispositivo OFB:

- Después de completar la configuración mediante la aplicación de configuración de OFB, continúe con las instrucciones en pantalla del auricular de OFB y complete la configuración del dispositivo.
- La aplicación MobileIron Go se inicia automáticamente y debe proporcionar las credenciales de inicio de sesión para completar el registro siguiente las instrucciones de MDM.

Ahora, el dispositivo está aprovisionado en modo DO y está ajustado para administrarse con MDM.
