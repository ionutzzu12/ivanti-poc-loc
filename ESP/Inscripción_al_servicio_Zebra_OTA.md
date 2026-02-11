---
title: Inscripción al servicio Zebra OTA
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

Una vez inscrito en el servicio Zebra OTA (Over the Air), se puede activar la configuración de Zebra OTA para recibir y actualizar los detalles del firmware de los dispositivos Zebra registrados en Ivanti Neurons for MDM.

Procedimiento

1. Vaya a **Administración > Infraestructura > Zebra OTA**. Aparecerá la página **Servicio OTA Zebra**.
2. En **Enlace al servicio OTA de Zebra**, haga clic en **Comenzar**.
3. Introduzca sus credenciales de Zebra OTA para iniciar sesión y siga los pasos para solicitar una aprobación para hacer uso de los servicios de Zebra.
4. Haga clic en **Completar verificación** para obtener la confirmación de la conexión al servicio Zebra. Cuando se confirme la conexión, el estado de la inscripción correcta se muestra en la página Servicio Zebra OTA.

Para revocar la inscripción, haga clic en **Revocar** en la columna **Acciones** . La acción **Revocar** elimina todas las configuraciones OTA de Zebra de las configuraciones existentes. Para volver a inscribirse con Zebra OTA, haga clic en **Actualizar**. La acción de actualizar no tiene ningún impacto en las configuraciones existentes.

Después de la inscripción, puede habilitar la configuración del firmware de Zebra que recibe el cliente Go y se aplica a los dispositivos Zebra (que se ejecutan en la versión 8.0 de Android o versiones más recientes compatibles) en el modo Propietario de dispositivo. Cuando se aplica la configuración, se descarga el firmware y se instala en el dispositivo según lo programado en la configuración. Para obtener más información sobre cómo activar la configuración del firmware de Zebra, consulte [**Configuración de actualización del sistema**](./Configuración_de_la_actualización_del_sistema.md).

Una vez completada la actualizaciones del firmware, puede ver el estado de actualización del firmware en el dispositivo Zebra en la columna **Actualización del sistema** de la página Dispositivos. A continuación se enumeran los posibles estados:

- **Desconocido**: no admitido por el cliente o el sistema operativo
- **Actual**: el dispositivo tiene la actualización más reciente disponible
- **Pendiente**: se aplica la configuración de actualización del sistema pero no se ha descargado ni aplicado la actualización
- **En descarga**: la actualización del sistema se está descargando para el cliente
- **Disponible**: la actualización del sistema está actualmente disponible para el dispositivo.
- **Error**: error en la descarga o instalación.

La columna **Versión de la revisión de Zebra** que hay en la página Dispositivos muestra la información de la revisión de Zebra del dispositivo.

La **Versión de Zebra Patch** no es compatible con dispositivos de Android 11 y posteriores. Solo es compatible la **Actualización completa de Zebra**.
