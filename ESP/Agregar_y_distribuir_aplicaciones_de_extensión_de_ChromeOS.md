---
title: Agregar y distribuir aplicaciones de extensión de ChromeOS
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

El administrador puede agregar aplicaciones de extensión de ChromeOS desde el Catálogo de aplicaciones y distribuir estas aplicaciones a los dispositivos de ChromeOS.

**Procedimiento**

1. Vaya a **Aplicaciones** > **Catálogo de aplicaciones**.
2. Haga clic en **+Añadir**.
3. Seleccione **ChromeOS** en la lista. La página **Agregar información de aplicación de ChromeOS** aparece en pantalla.
4. Proporcione los siguientes datos: **Nombre de la aplicación**: nombre de la aplicación de extensión de ChromeOS; **ID de extensión**: puede obtener esta información en la tienda web de Chrome.
5. Haga clic en **Siguiente**. La página **Configuración de aplicaciones** aparece en la pantalla. Ahí podrá seleccionar una actualización inmediata que se producirá la próxima vez que se ingrese el dispositivo o bien puede elegir que la aplicación se actualice automáticamente cuando haya disponibles nuevas versiones.
6. Seleccione una de las opciones de distribución de aplicaciones y proporcione la información necesaria.
   La distribución de la aplicación ChromeOS solo es compatible con grupos de usuarios LDAP.
   Cuando se haya identificado la aplicación de extensión de ChromeOS, debe distribuir la aplicación siguiente el mismo proceso que siguió para distribuir cualquier otra aplicación. Cuando distribuya la aplicación de extensión de Android, asegúrese de seleccionar los Grupos de usuarios a los que desee distribuir la aplicación y realice una instalación en segundo plano en el dispositivo.

Ajustes de instalación permite a los administradores controlar la instalación en segundo plano final y es necesario para forzar la aplicación en dispositivos de ChromeOS. Los Grupos de usuarios se deben seleccionar aquí.

Puede editar la información de una aplicación de extensión de ChromeOS o eliminar una aplicación de extensión de ChromeOS del catálogo de aplicaciones. Debe seguir un proceso similar al que sigue para editar o eliminar cualquier otra aplicación del Catálogo de aplicaciones.

### Editar una extensión de ChromeOS

1. Vaya a **Aplicaciones > Catálogo de aplicaciones > Detalles**.
2. Haga clic en **Editar**. Realice los cambios necesarios y haga clic en **Guardar**.
