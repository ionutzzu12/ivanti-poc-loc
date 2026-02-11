---
title: ChromeOS e Ivanti Neurons for MDM
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

ChromeOS es un sistema operativo basado en Linux creado y distribuido por Google. Ivanti Neurons for MDM es compatible con los dispositivos que funcionen en Android, Windows, iOS y macOS. Esta compatibilidad ahora se ha ampliado también a los dispositivos de ChromeOS. Ivanti Neurons for MDM proporciona una solución sencilla y unificada para la gestión de movilidad con la que configurar y administrar los dispositivos de ChromeOS. Ivanti proporciona una solución unificada, sencilla y muy completa para dispositivos de ChromeOS similar a los flujos de trabajo de administración que están disponibles para iOS, Android, Windows y Mac en Ivanti Neurons for MDM. El administrador puede conectarse a Ivanti Neurons for MDM con su Google Cloud (también denominado consola del administrador de Google) mediante una sencilla integración desde **Administrador > Google > Gestión de ChromeOS**.

### Requisitos previos

1. Debe tener una cuenta de administrador de Google.
2. Los usuarios de LDAP y las UO se deben importar en la consola de administración de Google. Ivanti Neurons for MDM solo es compatible con UO importadas de una fuente de LDAP. Las OU locales no son compatibles.
3. El administrador debe tener sincronizadas las unidades organizativas (grupos de usuarios) en Ivanti Neurons for MDM. Esto se puede hacer mediante la configuración del servidor de LDAP y agregando las unidades organizativas.

### Autorización de Google

Los dispositivos de ChromeOS disponibles en la consola del administrador de Google no se pueden registrar directamente en Ivanti Neurons for MDM. Como alternativa, estos dispositivos se registran con Google y la información de estos dispositivos se sincroniza entre Google y Ivanti Neurons for MDM. El administrador debe autorizar a Google para importar los dispositivos y llevar a cabo otras acciones, como asignar aplicaciones, configuraciones, etc.

**Procedimiento**

1. Vaya a **Administrador -> Google > Gestión de ChromeOS**.
2. Haga clic en **Autorizar Google**.
3. Seleccione la cuenta de Administrador de Google que desee autorizar.
4. Haga clic en **Continuar** para aceptar los permisos que proporcionarán los servicios necesarios.
   La configuración **ChromeOS configurado correctamente** aparece en la pantalla. También puede encontrar la información del dominio bajo la confirmación.

### Sincronizar dispositivos de ChromeOS desde Google

El administrador debe sincronizar los dispositivos de ChromeOS desde la consola del administrador de Goodle. Al usar la consola de administración de Google para acceder a los dispositivos de ChromeOS por primera vez, el administrador debe sincronizar manualmente los dispositivos mediante la opción Sincronizar ahora en la página de administración de ChromeOS.

Después de sincronizar los dispositivos manualmente por primera vez, las sincronizaciones siguientes se producirán automáticamente cada hora.

### Eliminación de la integración de la consola de administración de Google con Ivanti Neurons for MDM

Eliminar la integración revoca el token OAuth que recibimos de Google para acceder a los recursos de Google. Elimina los dispositivos de ChromeOS, el inventario asociado a configuración de Blueprint y configuración de aplicaciones, y los metadatos de inscripción. No se eliminarán la configuración del Blueprint ni las aplicaciones cargadas.

En caso de que la inscripción del abonado no se elimine, puede abrir un billete para comprobar el problema.

**Procedimiento**

1. Vaya a **Administrador -> Google > Gestión de ChromeOS**.
2. En la sección de registro de ChromeOS Ivanti Neurons for MDM, haga clic en **Eliminar**.
   Aparecerá una ventana emergente en la pantalla que indicará si desea proceder con la operación de Borrado, y se borrarán todos los dispositivos asociados a esta integración. Seleccione **Aceptar**.
