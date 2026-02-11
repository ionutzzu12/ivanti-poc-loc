---
title: Listas de aplicaciones (plists)
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

**Licencia: Silver**

Puede crear listas de aplicaciones obligatorias, en la lista de permitidos y en la lista de bloqueados para usarlas con la [**política de aplicaciones permitidas**](./Supervisar_y_controlar_las_aplicaciones_permitidas.md), donde podrá usar estas listas para especificar medidas que se aplicarán si las aplicaciones instaladas de un dispositivo no cumplen los requisitos indicados en las listas de aplicaciones. No se pueden editar las listas de aplicaciones una vez creadas porque se puede remitir a estas listas de aplicaciones en las [**políticas de aplicaciones permitidas**](./Supervisar_y_controlar_las_aplicaciones_permitidas.md). Del mismo modo, no se pueden eliminar listas de aplicaciones a las que se haya remitido desde las políticas de aplicaciones permitidas.

## Crear lista de aplicaciones

Procedimiento

1. Haga clic en **Administración**\*\*>**Infraestructura**>\*\***Listas de aplicaciones**.
2. Haga clic en **Crear nueva lista**.
3. En el cuadro **Nombre de la lista de aplicaciones**, introduzca un nombre para la lista.
4. Seleccione el tipo de lista, **Lista blanca**, **Lista negra** u **Obligatorio**.
5. En la sección **Agregar aplicaciones**, seleccione el tipo de aplicación, **App Store**, **OS X store**, **Google Play** o **Catálogo de aplicaciones**.
6. Introduzca los criterios de búsqueda para limitar sus opciones.
7. Utilice las casillas para seleccionar las aplicaciones. Puede utilizar búsquedas múltiples y habilitar más de una casilla.
8. Haga clic en la pestaña **Ver aplicaciones** para ver la lista de aplicaciones que ha seleccionado hasta el momento.
   Haga clic en **Guardar**.

Ahora ya puede usar esta lista cuando configure la política de [**Aplicaciones permitidas**](./Supervisar_y_controlar_las_aplicaciones_permitidas.md).

Si no puede ver la página **Lista de aplicaciones**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Sistema de solo lectura
