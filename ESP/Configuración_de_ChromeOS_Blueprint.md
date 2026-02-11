---
title: Configuración de ChromeOS Blueprint
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

La configuración de ChromeOS Blueprint tiene los ajustes siguientes:

- Ajustes del dispositivo
- Ajustes de usuario y explorador
- Ajustes de Sesión de invitado administrado

Puede aplicar la configuración de ChromeOS en Grupos de usuarios específicos (también denominados Unidades organizativas). Cuando intente distribuir la configuración de ChromeOS Blueprint, solo estará disponible la sección Grupos de usuarios y todos los Grupos de usuarios de LDAP asociados con la consola de administración de Google autorizada se enumerará en la sección. Puede seleccionar uno o más grupos de la lista y aplicar la configuración.

**Procedimiento**

1. Vaya a **Configuraciones > Añadir**.
2. Seleccione **Google ChromeOS** en la sección SO. La pestaña **Configuración de ChromeOS Blueprint** aparece en la pantalla.
3. Haga clic en **ChromeOS Blueprint**. La página **Crear configuración de ChromeOS Blueprint** aparece en la pantalla.
4. Introduzca un nombre para la configuración en el cuadro **Nombre**.
5. En los Ajustes de configuración, puede modificar los Ajustes del dispositivo, el Usuario y los Ajustes del explorador, y los ajustes de la sesión de invitado administrada, como necesite, así como alternar el botón "Enviar al dispositivo" para aplicar los ajustes modificados.
6. Haga clic en **Siguiente**.
7. Seleccione **Personalizado** para las opciones de distribución.
8. Solo los grupos de usuarios de LDAP estarán disponibles para distribuir la configuración.
   En el caso de distribuir la configuración a todos, se puede hacer solo para los Grupos de usuario de LDAP disponibles en Ivanti Neurons for MDM y en la consola del administrador de Google.
   Seleccione uno o más grupos y haga clic en **Hecho**.

Cuando la configuración distribuida no se distribuye, la configuración aplicada no se revertirá.

Puede cargar los archivos en la configuración de ChromeOS Blueprint.
