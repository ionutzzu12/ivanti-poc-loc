---
title: Sincronizar y obtener comentarios de aplicaciones
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Puede enviar una solicitud a una aplicación instalada en dispositivos Android para obtener información detallada sobre el estado de configuración actual de la aplicación. Cuando se envía una solicitud, se recibe un informe de comentarios de configuración de la aplicación para el dispositivo.

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Haga clic en el dispositivo para el que desea enviar la solicitud.
3. Haga clic en **Acciones**.
4. Seleccione **Sincronizar y recuperar los comentarios de la aplicación**. La petición se envía para sincronizar y recuperar los comentarios de configuración de la aplicación. Se actualizará el campo «Última sincronización de comentarios sobre la aplicación» que hay junto a «Último ingreso del cliente».
5. En la pestaña **Aplicaciones instaladas**, haga clic en el vínculo **Ver detalles** para la aplicación en la columna **Comentarios sobre aplicaciones**. Aparecerá la ventana **Comentarios sobre la aplicación**.**Clave**: proporciona información detallada y la ubicación de los ajustes notificados (en la configuración de la aplicación administrada de la aplicación) basándose en los comentarios que se han recibido desde las aplicaciones.**Sello temporal**: hora y fecha de la clave.**Gravedad**: indica la importancia de la clave. Ejemplo: 'Info', 'Error'.**Mensaje**: el tipo de mensaje recibido de los comentarios sobre configuración de la aplicación. Ejemplo: ‘Error’.**Datos**: detalles de los datos recibidos de los comentarios sobre configuración de la aplicación.

### Visualizar los comentarios sobre la configuración de aplicaciones desde el App Catalog

Se puede ver el informe de comentarios sobre la configuración de la aplicación para cada aplicación en particular desde el App Catalog.

**Procedimiento**

1. Vaya a **Aplicaciones > Catálogo de aplicaciones**.
2. Seleccione la aplicación de la que desea ver los detalles.
3. Haz clic en la pestaña **Comentarios sobre configuración de aplicaciones**. La columna **Recuento de dispositivos** muestra el número de dispositivos (hipervínculo) para cada clave del informe de comentarios sobre la configuración de la aplicación.
4. Haga clic en el hipervínculo de número de dispositivos para ver los detalles de los dispositivos. Por ejemplo, al hacer clic en el hipervínculo 5, se muestran los detalles de 5 dispositivos. Se muestran los siguientes detalles para la combinación de 'Clave' y 'Gravedad', que aparece encima de la tabla:**Dirección de correo electrónico**: especifica el nombre de usuario. Al hacer clic en el enlace del nombre de usuario, se accede a la pestaña **Aplicaciones instaladas** en **Dispositivos > Detalle del dispositivo**.**Tipo de dispositivo**: especifica el modelo del dispositivo.**OS**: número de versión del OS Android.**Número de serie**: número de serie del dispositivo.**Sello temporal**: hora y fecha en que se actualizó por última vez.**Mensaje**: el tipo de mensaje recibido de los comentarios sobre configuración de la aplicación. Ejemplo: ‘Error’.**Datos**: detalles de los datos recibidos de los comentarios sobre configuración de la aplicación.

Se pueden ver las notificaciones de errores de los comentarios sobre configuración de la aplicación para el dispositivo Android haciendo clic en el icono de la campana (arriba a la derecha) o desde la página **Panel > Notificaciones**. Al hacer clic en el enlace de notificación, se accede a la pestaña **Comentarios sobre configuración de la aplicación** y se puede ver el informe de comentarios de la aplicación.

El informe de comentarios sobre configuración de la aplicaciones se eliminará y no se mostrará cuando el dispositivo se borre o se retire. Esta tarea en segundo plano que se ejecuta cada 24 horas purga los datos de más de 7 días de antigüedad.
