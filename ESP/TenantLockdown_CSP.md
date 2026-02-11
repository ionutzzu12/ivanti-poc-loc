---
title: TenantLockdown CSP
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

El administrador puede bloquear todos los dispositivos Windows a los abonados utilizando la función TenantLockdown CSP. Para utilizar esta función, los dispositivos deben estar inscritos mediante la opción Autopilot. Esta configuración puede realizarse a nivel de dispositivo.

En los modos Autopilot Self-deployed y User-driven, el administrador puede bloquear los dispositivos directamente a los abonados. Esto es útil cuando los dispositivos son robados o se pierden. En estos casos, incluso si el dispositivo se restablece, el usuario se verá obligado a conectarse al abonado y la creación de cuentas locales no se admite en el modo Auto-desplegado. Pero si hay que impedir la creación de cuentas en el modo dirigido por el usuario, el administrador debe habilitar la opción **Ocultar** en el ajuste **Cambiar opciones de cuenta** durante la configuración del perfil del Autopilot.

El administrador puede habilitar el CSP de TenantLockdown creando una Configuración de Restricciones de Windows y seleccionando la opción **Requerir que los usuarios se conecten a la red durante la configuración del dispositivo (se requiere el perfil de Autopilot)** en **Otras Restricciones**.

Para eliminar un dispositivo del CSP de TenantLockdown, el administrador debe eliminar manualmente el dispositivo del grupo o cambiar las restricciones.
