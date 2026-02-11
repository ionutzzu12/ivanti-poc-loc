---
title: Inventario de aplicaciones
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Filtrar cómo se muestran las aplicaciones**](./Inventario_de_aplicaciones.md)
- [**Mostrar los dispositivos instalados para una aplicación**](./Inventario_de_aplicaciones.md)
- [**Visualizar la lista de aplicaciones**](./Inventario_de_aplicaciones.md)
- [**Visualización de las aplicaciones Win32 o Win32 Store instaladas en un dispositivo**](./Inventario_de_aplicaciones.md)
- [**Creación de un permiso de vista personalizada**](./Inventario_de_aplicaciones.md)
- [**Exportar un inventario de aplicaciones**](./Inventario_de_aplicaciones.md)

El inventario de aplicaciones es la lista de aplicaciones detectadas en los dispositivos inscritos. Como administrador, puede usar esta página para obtener información sobre las aplicaciones que se están utilizando en los dispositivos inscritos. Puede responder preguntas como las siguientes:

- ¿Qué aplicaciones son las más populares?
- ¿Los dispositivos iOS obtienen las aplicaciones directamente desde la App Store?
- ¿Cuántos usuarios de Android han descargado una aplicación interna opcional?
- ¿Cuántos dispositivos están utilizando una versión obsoleta de una aplicación?

## Filtrar cómo se muestran las aplicaciones

Al mostrar la página **Dispositivos > Inventario de aplicaciones**, aparecen enumeradas todas las aplicaciones. Para reducir esta lista a ciertas aplicaciones, utilice los filtros (panel izquierdo). Por ejemplo, para limitar la lista y que aparezcan solo las aplicaciones privadas de Google Play, seleccione **Privadas** en la sección **Origen**.

Se puede ver el inventario de aplicaciones en todos o en varios dispositivos espaciales seleccionando varios espacios de la lista desplegable. Al pasar el cursor sobre las aplicaciones mostradas, se muestran los recuentos de los dispositivos. Se puede hacer clic en el recuento de una aplicación para que muestre todos los dispositivos que contienen la aplicación. Cada registro del inventario de la aplicación se agrupará por espacios.

Puede buscar mediante el nombre de la aplicación o el ID del paquete.

Si ha seleccionado varios espacios, al pasar el ratón por el valor **Total** de la columna **# Instalado**, se muestra el número de instalaciones por espacio de dispositivo.

## Mostrar los dispositivos instalados para una aplicación

Haga clic en el número **Gestionado**, **No gestionado** o **Total** que aparece en la columna **# Instalado**.

## Visualizar la lista de aplicaciones

Haga clic en el **n.º solicitado** que hay junto a la aplicación en el inventario de aplicaciones para ver los dispositivos que solicitaron la aplicación. Esto solo es aplicable a dispositivos solo MAM.

## Visualización de las aplicaciones Win32 o Win32 Store instaladas en un dispositivo

El inventario de aplicaciones muestra las aplicaciones Win32 o Win32 Store en un dispositivo si la [**configuración de privacidad**](./Configuración_de_privacidad.md) para ese dispositivo permite la recopilación de información para todas las aplicaciones del mismo. Puede configurar la política de privacidad del dispositivo.

**Procedimiento**

1. Determine qué configuración de privacidad es aplicable al dispositivo deseado siguiendo las indicaciones de [**Dispositivos**](./Dispositivos.md).
2. Vaya a **Configuraciones**.
3. Para la configuración de privacidad que anotó en el paso 1:1) Seleccione la configuración.
   2\) Haga clic en Editar.
   3\) En **Recopilar inventario de aplicaciones,** seleccione **Para todas las aplicaciones del dispositivo**.
   4\) Haga clic en **Hecho**.

El CSP Win32AppInventory devuelve la lista de todas las aplicaciones Win32 y Win32 Store instaladas en el dispositivo cada 24 horas tras la ejecución de los análisis de inventario en el dispositivo.

## Creación de un permiso de vista personalizada

Puede especificar permisos de vista personalizados para los usuarios.

**Procedimiento**

1. Vaya a **Administrador**.
2. Vaya a **Administración de funciones**.
3. Haga clic en **Añadir función personalizada**.
4. Seleccione la opción **Función específica para espacios** .
5. Introduzca el nombre de usuario en el campo **Nombre**.
6. En el menú **Dispositivos**, haga clic en **Inventario de aplicaciones**.
7. Seleccione la casilla **Vista**.
8. En el menú **Dispositivos**, haga clic en **Acciones del dispositivo**.
9. Haga clic en **Guardar**.
10. Vaya a **Usuarios** en el menú principal.
11. Haga clic en el nuevo usuario que ha creado.
12. Haga clic en **Asignar funciones**.
13. Seleccione la casilla **aplicación | Específica para el espacio** y haga clic en **Siguiente**.
14. La página **Resumen** mostrará los permisos asignados a la función creada.
15. Haga clic en **Hecho**.
16. Inicie la sesión como nuevo usuario.
17. Haga clic en **Dispositivos** en el menú principal.
18. Haga clic en **Inventario de aplicaciones**.
19. La página **Inventario de aplicaciones** mostrará ahora solo las aplicaciones permitidas para el usuario.

## Exportar un inventario de aplicaciones

Como administrador, puede solicitar informes del Inventario de aplicaciones mediante la opción **Exportar a CSV**.

**Procedimiento**

1. Vaya a **Dispositivos > Inventario de aplicaciones**.
2. Seleccione un inventario de la lista.
3. Haga clic en **Exportar a CSV**.
4. Seleccione una de las siguientes opciones:\* **Exportar aplicaciones a CSV** para exportar todas las aplicaciones del inventario de aplicaciones.
   - **Exportar dispositivos a CSV** para exportar una aplicación específica según la tabla siguiente:|                 |                                                                                                                                        |
     \| --------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
     \| **Opción**      | **Descripción**                                                                                                                        |
     \| ID de paquete   | Introduzca el ID de paquete de la aplicación.                                                                                          |
     \| ¿Desea exportar | Seleccione una de las siguientes opciones:\* Total instalado
     - Administrado
     - Sin administrar
     - Solicitado (para dispositivos MAM-Only) |
5. Haga clic en **Exportar**.

El administrador verá una ventana emergente que le informará de que el informe exportado tardará un tiempo en procesarse. Una vez enviada la solicitud, el administrador debe esperar a que se complete la solicitud para enviar otra solicitud. Cuando el informe está listo, el administrador recibirá un mensaje para que descargue o elimine el informe que se ha generado. El administrador también recibirá un correo electrónico con un enlace para descargar el informe.

Si no puede ver la página **Inventario de aplicaciones**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración de dispositivos
- Dispositivo solo lectura
