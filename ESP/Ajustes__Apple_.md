---
title: Ajustes (Apple)
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Los administradores pueden configurar, activar y desactivar diferentes ajustes de los dispositivos Apple.

## Registro silencioso (solo para macOS)

El registro silencioso para dispositivos macOS está bloqueado en Habilitado. Esto afecta a los registros de todos los dispositivos nuevos del abonado y es compatible con Mobile\@Work 1.4 y versiones más recientes compatibles.

## Ajustes del perfil

Los administradores pueden activar o desactivar el envío de correos electrónicos a los usuarios finales y notificaciones a los clientes de macOS y Go for iOS si el perfil de MDM no está instalado. La característica de notificaciones del perfil de MDM está activada de forma predeterminada.

Procedimiento

1. Vaya a **Admin. > Ajustes**.
2. Seleccione o deseleccione la opción **Enviar correo electrónico al usuario y notificación al cliente si el perfil de MDM no está instalado**.
3. Seleccione el máximo número de correo electrónicos y notificaciones entre 1 y 4.
4. Haga clic en **Guardar**.

## Actualizaciones del sistema operativo para la inscripción automatizada de dispositivos (solo iOS)

Los administradores pueden activar las actualizaciones del sistema operativo iOS para la inscripción automatizada de dispositivos. Si esta opción está activada, los dispositivos de la Inscripción de dispositivos usarán la configuración de [**Actualizaciones de software**](./Actualizaciones_de_software.md) en lugar del ajuste de actualización del sistema operativo programado en el perfil de Inscripción de dispositivos.

Esta opción está desactivada por defecto, en cuyo caso se utiliza el ajuste de programar la actualización del sistema operativo en el perfil de Inscripción de dispositivos. La activación de este ajuste es permanente y no se puede desactivar. Este ajuste eliminará el ajuste de la actualización del SO programada en todos los perfiles disponibles de Inscripción de dispositivos.

Los dispositivos supervisados que no sean de la Inscripción de dispositivos utilizan la configuración de las Actualizaciones de software.

Procedimiento

1. Vaya a **Admin. > Ajustes**.
2. Seleccione o deseleccione la opción **Usar la configuración de actualización de software para la inscripción de dispositivos automatizada**.
3. Haga clic en **Sí** para confirmar.
4. Haga clic en **Guardar**.

## Inicio de sesión seguro multiusuario

Los administradores pueden borrar la contraseña del dispositivo cuando el usuario cierra la sesión en el clip web «Inicio de sesión seguro multiusuario» en los dispositivos compartidos iOS seleccionando la opción «**Borrar la contraseña cuando el usuario cierre sesión**» en la sección «**Inicio de sesión seguro multiusuario**» en Administrador > Apple > Ajustes

## Ajustes de prioridades para la configuración de restricciones

El administrador puede habilitar la prioridad para múltiples configuraciones de restricciones para iOS y macOS seleccionando las opciones **Configuración de restricciones para iOS** o **Configuración de restricciones para macOS** en la sección **Ajustes de prioridad para la configuración de restricciones** en la sección **Administrador > Apple > Ajustes**. Esta opción está desactivada de forma predeterminada. Para obtener más información sobre cómo funciona la prioridad, consulte [**Priorizar configuraciones**](./Priorizar_configuraciones.md)

Procedimiento

1. Vaya a **Administrador > Apple > Ajustes**.
2. En la sección **Ajustes de prioridades para la configuración de restricciones**, seleccione la opción **Configuración de restricciones de iOS** o **Configuración de restricciones de macOS**.
3. Haga clic en **Guardar** para activar la prioridad. Aparecerá el banner «**Se han activado los ajustes de prioridades para la configuración de restricciones (iOS o macOS)**». Antes de que la prioridad esté **Aprobada**:\* **Edite el resumen de distribución (si procede)**: cuando se activa la configuración de la prioridad, el resumen de distribución para la configuración de restricciones seleccionada se cambia de «**Aplicar a los dispositivos de otros espacios**» a «**Aplicar a todos los dispositivos de otros espacios como máxima prioridad**» por defecto.
   - **La prioridad por defecto se asigna en el orden de creación**: para la configuración del tipo de restricción seleccionada, la prioridad por defecto existente se asignará en el orden de creación.
   - **Suspensión de la gestión de la configuración**: la gestión de la configuración de restricciones seleccionada (por ejemplo, la configuración de restricciones de iOS) se suspende hasta que usted apruebe la prioridad.Una vez activada la prioridad, cualquier cambio en las restricciones no se procesa hasta que se apruebe. Antes de aprobarla, el administrador puede editar la distribución, el resumen de la distribución o la prioridad de las configuraciones de restricciones en la sección **Configuraciones**.
4. Seleccione la opción **Aprobar** para que la prioridad entre en vigor.
5. Haga clic en **Guardar**.La opción **Aprobación** no está disponible cuando se deselecciona una opción de configuración de Restricciones de iOS o macOS; los cambios se aplican de inmediato.

Cuando el ajuste de la prioridad está desactivado, no hay ninguna prioridad asociada a las configuraciones. Todas las configuraciones de restricción se transfieren al dispositivo, si procede (en la siguiente sincronización del dispositivo).

- **Resumen de distribución (si procede)**: cuando se desactiva el ajuste de prioridad para la configuración de restricciones, el resumen de distribución cambia de Aplicar a todos los dispositivos de otros espacios de dispositivos como máxima prioridad o Aplicar a todos los dispositivos de otros espacios de dispositivos como prioridad más baja a «Aplicar a los dispositivos de otros espacios».
- **Ninguna prioridad asignada**: se elimina la prioridad asignada para la configuración de restricciones seleccionada
