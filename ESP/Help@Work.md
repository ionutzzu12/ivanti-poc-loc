---
title: Help@Work
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

**Licencia:** Platinum

**Compatible con:** dispositivos Android y iOS compatibles con Ivanti Neurons for MDM

Utilice Help\@Work para Android/iOS para proporcionar asistencia remota a los usuarios de los dispositivos Android y iOS. Help\@Work para Android/iOS se basa en la aplicación TeamViewer QuickSupport. Necesitará una cuenta de TeamViewer para usar Help\@Work para Android/iOS. Si no tiene ya una cuenta, visite teamviewer.com para obtener más detalles.

Help\@Work transforma la experiencia de soporte técnico para los dispositivos iOS 11.0+ y Android permitiendo que los usuarios pidan ayuda con un solo clic y compartan su pantalla con un representante del soporte técnico. Los usuarios ya no tienen que perder tiempo explicando verbalmente el problema, mientras que el personal informático puede trabajar de forma más eficiente a la hora de solucionar problemas con un dispositivo. Esto no es compatible con los dispositivos iOS «MAM only».

TeamViewer es compatible con los dispositivos de Propietario del dispositivo Android en modo Kiosco.

Los comandos de inicio de TeamViewer dejan de existir si se sale de la aplicación o el dispositivo se reinicia.

En los dispositivos Android, si la aplicación Teamviewer QuickSupport no está instalada, se le pedirá al usuario que descargue la aplicación. En los dispositivos iOS, la aplicación se tiene que insertar mediante el App Catalog o, si ya está instalada en el dispositivo, se debe convertir en aplicación administrada.

La aplicación Teamviewer QuickSupport debe estar en primer plano para que la sesión se aplique a la aplicación. Para el modo Sin atender es necesaria la aplicación del host de TeamViewer.

La versión de la aplicación de escritorio que instala el administrador debe ser compatible con la versión de Quicksupport instalada en el dispositivo del cliente para admitir sesiones remotas.

## Configurar Help\@Work para Androido iOS

A continuación le indicamos los pasos para una única configuración para personalizar y distribuir Help\@Work para Androido iOS:

1. Vaya a la pestaña **Administrador**.
2. En Infraestructura, haga clic e&#x6E;**&#x20;Help\@Work**.
3. **Help\@Work&#x20;**&#x72;equiere TeamViewer. En la sección Activar TeamViewer, active la opción **TeamViewer asistido** o **TeamViewer sin atender (solo Android)** haciendo clic en el botón **Activar ahora**.
4. Revise el acuerdo de licencia de TeamViewer y haga clic en **Aceptar** para continuar. Su licencia corporativa ya está activada. De este modo, TeamViewer identifica los clientes de Ivanti para que su acceso esté garantizado.
5. La opción **Eliminar activación** está disponible al activar el TeamViewer. Cuando hace clic en **Eliminar activación** bajo la sección **Activar TeamViewer**, aparece la ventana **Confirmar la eliminación de la activación** en la pantalla. Haga clic en **Eliminar activación** para eliminar la Activación de TeamViewer, que, a su vez, eliminará la función de Help\@Work en todos los dispositivos compatibles. No obstante, puede activar TeamViewer mediante una cuenta existente o una cuenta distinta en una fase posterior.
   Si quiere eliminar la cuenta de **TeamViewer** en modo Desatendido, debe cancelar el aprovisionamiento de los dispositivos asociados para los que está activado el modo Desatendido. Para desaprovisionar los dispositivos asociados, debe deshacer la distribución de la aplicación **TeamViewer** desde los dispositivos asociados y forzar una conexión. Asegúrese de que la aplicación TeamViewer se elimina de todos los dispositivos y, a continuación, elimine le unión de cuentas desde la consola del administrador.
   Distribuya la aplicación TeamViewer entre los usuarios que desee utilizando el flujo de trabajo estándar de la aplicación para iniciar las sesiones remotas. Esto es específico para los modos **Atendido** y **Sin atender**. Si el administrador quiere controlar el dispositivo, el complemento universal o el complemento específico por modelo/OEM de TeamViewer se debe distribuir también en los dipositivos. Consulte [**Configuración de la aplicación**](./Configuración_de_aplicaciones.md) para ver las instrucciones.

## Iniciar una sesión remota utilizando Help\@Work para Androido iOS

La sesión típica de Help\@Work para Androido iOS empieza por un usuario final que necesita ayuda.

Para iniciar una sesión de Help\@Work con el dispositivo del usuario:

::::WorkflowBlock
:::WorkflowBlockItem
En Ivanti Neurons for MDM, vaya a **Dispositivos**.
:::

:::WorkflowBlockItem
En la página de la lista de dispositivos, haga clic en el dispositivo que necesita asistencia técnica.
:::

:::WorkflowBlockItem
En el menú Acciones, haga clic en **Iniciar control remoto de TeamViewer** para dispositivos Android o **Visualización remota** para dispositivos iOS. Verá dos opciones:
:::

:::WorkflowBlockItem
- Modo atendido (predeterminado): esta opción requiere tener instalada la aplicación **Compatibilidad rápida con TeamViewer** y que esté en la lista blanca del dispositivo de destino.
- Modo desatendido (disponible solo en Android): esta opción requiere que la aplicación **TeamViewer Host** esté instalada y en la lista blanca del dispositivo de destino.
  Si desea incluir los nombres de host en la lista blanca o anular la política de seguridad de contenidos, póngase en contacto con el equipo de asistencia.

La opción de modo Sin atender funciona también en modo Kiosco. Se debe habilitar desde la página de integración de TeamViewer. El control remoto Sin atender requiere que la aplicación del host TeamViewer esté en el dispositivo, la activación de una vez en un dispositivo y una licencia de complemento MI. Para la activación única, el aviso de permiso se mostrará cuando la aplicación de host de TeamViewer se instale y se inicie por primera vez. Si lo desea, el administrador puede usar la aplicación de TeamViewer de "Inicio automático (ajustes de Configuración de aplicaciones administradas)" después del a instalación. El número de licencias se calcula en base a la distribución de la aplicación del host de TeamViewer. Si la aplicación del host de TeamViewer se distribuye en un dispositivo, se consume una licencia de sesión de host remoto sin atender. Además de la aplicación del host de TeamViewer, es posible que necesite las otras aplicaciones complementos y se deben permitir en el modo kiosco y kiosco compartido. Es posible que sean necesarios otros complementos según el modelo y el fabricante del dispositivo.

Los dispositivos de Google Pixel no continúan con este permiso y requieren el consentimiento de permiso para cada sesión.

Si el administrador tiene un token válido de TeamViewer, el cliente de escritorio se inicia con una sesión de asistencia al dispositivo. En caso contrario, el administrador deberá iniciar sesión con TeamViewer y conceder permisos.
:::
::::

Para iniciar rápidamente una sesión remota, los administradores pueden iniciar sesión en la aplicación de escritorio de antemano.

## Instalar TeamViewer

Instale la aplicación de TeamViewer en su escritorio para poder acceder y proporcionar asistencia técnica a los dispositivos remotos de sus usuarios. Para instalar TeamViewer:

1. Descargue aquí el paquete de instalación para la versión completa de TeamViewer para Mac, Windows o Android:[**https://www.teamviewer.com/en/download/**](https://www.teamviewer.com/en/download/)
2. Inicia el programa de instalación de TeamViewer.
3. Seleccione **Instalación básica**.
4. Seleccione **Uso empresarial/comercial**.
5. Haga clic en **Aceptar - finalizar**.

## Solicitar una cuenta de TeamViewer

Debe tener una cuenta de TeamViewer para poder proporcionar asistencia técnica con TeamViewer. Para obtener una cuenta de TeamViewer:

1. Vaya a [**https://login.teamviewer.com/**](https://login.teamviewer.com/LogOn#register).
2. Introduzca su correo electrónico, nombre y contraseña.
3. Haga clic en **Registrarme**.
4. Utilice la cuenta de correo electrónico que introdujo en el paso 2 para recibir un mensaje de correo de activación de su cuenta en TeamViewer.
5. Complete las instrucciones que aparecen en el correo electrónico para activar su cuenta de TeamViewer.

## Confirmar la Id. de la sesión de TeamViewer

TeamViewer genera una Id. de la sesión cuando se establece la conexión entre el ordenador del administrador y el dispositivo móvil del usuario.

1. Cuando se genera la ID de sesión, Ivanti Neurons for MDM la pasa a la aplicación TeamViewer QuickSupport utilizando la configuración de la aplicación administrada, que a su vez utiliza esta ID de sesión para invocar el cliente de TeamViewer en el dispositivo. En el caso de iOS, la ID de sesión caduca a los 30 minutos.
2. Se solicita al usuario que acepte el EULA de TeamViewer.
