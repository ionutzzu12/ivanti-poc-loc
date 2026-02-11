---
title: Encontrar y filtrar usuarios
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Buscar a un usuario**](./Encontrar_y_filtrar_usuarios.md)
- [**Uso de la Búsqueda avanzada para los usuarios**](./Encontrar_y_filtrar_usuarios.md)
- [**Cargando las consultas de Búsqueda para los usuarios**](./Encontrar_y_filtrar_usuarios.md)
- [**Filtrar usuarios**](./Encontrar_y_filtrar_usuarios.md)

## Buscar a un usuario

Una vez que haya añadido muchos usuarios, puede ser útil usar filtros o búsquedas para encontrar rápidamente la entrada de un usuario.

**Procedimiento**

1. Vaya a **Usuarios.**
2. Escriba los caracteres en el cuadro cuadro de búsqueda.

## Uso de la Búsqueda avanzada para los usuarios

Puede utilizar la opción de Búsqueda avanzada para buscar usuarios en función de reglas para identificar y ver los usuarios con criterios específicos. Las opciones de reglas se pueden anidar juntas utilizando las opciones CUALQUIERA (O) o TODOS (Y). Los usuarios que coinciden con las reglas se muestran debajo de la sección. Las regla se pueden crear con los operadores siguientes:

- comienza con
- termina con
- contiene
- no contiene
- no comienza con
- no termina con
- es menor que
- es mayor que
- se encuentra en el intervalo
- es igual a
- no es igual a

Desde Neurons for MDM 118elIvanti Neurons for MDM portal del Administrador se muestra el número de grupos de usuarios duplicados y el número de GUID correspondiente para identificar los grupos duplicados cuando se selecciona el atributo Nombre del grupo de usuarios en el creador de reglas. Además, una tabla bajo esta regla muestra la lista de los grupos de usuarios duplicados y sus detalles, como el Nombre del Grupo de Usuarios, el GUID, la Fuente y el nombre distinguido (DN).

**Procedimiento**

1. En la página Usuarios, haga clic en el enlace **Búsqueda avanzada**.
2. Haga clic en **Cualquiera** si los usuarios deben coincidir con al menos una de las reglas o en **Todas** si los usuarios deben coincidir con todas las reglas.
3. Crear una regla que defina los criterios de búsqueda, como Grupo de usuarios, Atributo de usuario personalizado y Atributo LDAP personalizado.
4. (Opcional) Haga clic en + para crear reglas adicionales, si fuera necesario.
5. (Opcional) Haga clic en **Guardar** para guardar la consulta.
6. Haga clic en **Buscar**. En la página se muestran la lista de usuarios que coinciden con los criterios de búsqueda.

## Cargando las consultas de Búsqueda para los usuarios

**Procedimiento**

1. En la página Usuarios, haga clic en el enlace **Búsqueda avanzada**.
2. Haga clic en el icono «Carpeta». Aparecerá la ventana **Búsqueda avanzada**. La lista de las consultas de búsqueda creadas se muestra en la sección **Cargar consulta**. En esta sección se muestran los siguientes detalles:\* **Nombre de la consulta**: el nombre de la consulta cargada.
   - **Contenido de la consulta** muestra el contenido de las reglas que definen la consulta de búsqueda.
   - **Acciones**: seleccione la acción que se realizará en la consulta.
3. Haga clic en **Cargar consulta** en la columna **Acciones** para ver la lista de usuarios que coinciden con los criterios definidos en la consulta cargada.Para borrar una consulta cargada, haga clic en el icono «Borrar».

## Filtrar usuarios

La barra de navegación lateral de Filtros tiene una lista con varias secciones que le ayudan a buscar un usuario concreto en la lista total de usuarios. El asistente de Administrar filtros contiene la lista de todas la secciones que puede seleccionar para que se muestren en la barra de navegación de Filtros.

**Procedimiento**

1. Vaya a **Usuarios.**
2. Haga clic en las casillas relevantes de las secciones que se listan en el asistente de Administrar filtros. Puede buscar las siguientes opciones:\* Administradores
   - Estado de Google
   - Estado de la invitación
     - Completa (el usuario la recibió y respondió).
     - Caducada (el usuario no respondió a tiempo).
     - No invitado (no ha invitado a este usuario).
     - Pendiente (Pendiente de la respuesta del usuario).
       Caducidad de la contraseña- Caduca el (la opción de usuarios con caducidad de la contraseña está ajustada en una fecha concreta).
     - Nunca (la opción de usuarios con caducidad de la contraseña está ajustada en «nunca»).
   - Grupo de usuarios (Seleccione los grupos de usuarios de su interés).
   - Fuente de usaurio\* LDAP
     - Entra ID
     - Lista
     - Salesforce
     - Local
   - Sincronización\* Sincronización directa: lista los usuario que se sincronizaron de manera directa desde el servidor de LDAP
     - Sin sincronización: lista los usuario que se eliminaron del servidor LDAP
     - Sincronización indirecta: lista los usuario que se sincronizaron de manera indirecta desde el servidor de LDAP
     - N/A
3. (Opcional) Haga clic en **Restablecer valores predeterminados** para restablecer la selección a los filtros predeterminados. La barra de navegación de Filtros muestra las secciones seleccionadas. Si desmarca todas las casillas del asistente de Administrar filtros, la barra de navegación lateral de Filtros mostrará todas las secciones.
4. Haga clic en cualquier lugar fuera del asistente de Administrar filtros para salir del asistente.
5. Haga clic en el icono x para cerrar la barra de navegación lateral del Filtros y haga clic en **Filtros** para volver a abrir la barra de navegación lateral.
