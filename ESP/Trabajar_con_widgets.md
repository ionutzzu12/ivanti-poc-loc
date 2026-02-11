---
title: Trabajar con widgets
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Añadir un widget**](./Trabajar_con_widgets.md)
- [**Organizar los widgets**](./Trabajar_con_widgets.md)
- [**Editar un widget**](./Trabajar_con_widgets.md)
- [**Revisar notificaciones**](./Trabajar_con_widgets.md)
- [**Informes**](./Trabajar_con_widgets.md)
- [**Audit Trails**](./Trabajar_con_widgets.md)

El panel muestra importantes estadísticas sobre los dispositivos registrados y los usuarios. Cada sección del panel se llama widget. En cada widget se define:

- la categoría de los datos mostrados (por ej. «dispositivos» o «usuarios»)
- cómo se agrupan los datos (por ej., por versión del SO o por modelo)
- cómo se filtran los datos (por ej., mostrar solo dispositivos iOS)
- cómo se muestran los datos (por ej., en un gráfico circular o gráfico de barras)

## Añadir un widget

1. Haga clic en **Añadir** (arriba a la derecha).
2. Asigne un nombre al widget.
3. Seleccione una categoría de datos.
4. Complete las opciones de filtrado a medida que se muestran.
5. Seleccione el tipo de visualización predeterminada (gráfico circular, gráfico de barras, gráfico de líneas).
6. Haga clic en **Hecho**.

## Organizar los widgets

Los widgets siempre se muestran en filas de tres. Sin embargo, pueden cambiar el orden en que aparecen:

1. Haga clic en **Organizar** (arriba a la derecha).
2. Arrastre los cuadros en el orden en que quiere que aparezcan los widgets.
3. Haga clic en **Aceptar**.

## Editar un widget

1. Haga clic en el icono de ajustes del widget (arriba a la derecha).
2. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/ZjC2Kjnr4YJnVfpSxTzzV_editdash.png" alt caption}
   Seleccione **Editar**.
3. Realice los cambios.
4. Haga clic en **Hecho**.

## Revisar notificaciones

Haga clic en el icono de la campana (arriba a la derecha) o vaya a la página **Panel > Notificaciones** para revisar las notificaciones y tomar medidas cuando sea necesario en función de los siguientes criterios:

- Tipo de componente
  - APP
  - LDAP
  - Entra ID
  - Lista de permitidos de dispositivos
  - Apps and Books
  - iOS
  - Android
  - macOS
  - visionOS
  - watchOS
  - Abonado
  - EC
  - Conector
  - Sentry
  - Token del servidor de inscripción de dispositivos
    Tipo de notificación
  - Caducidad
  - Sincronización de datos
  - Límite de uso
  - Acción administrativa
  - Error de autenticación del servidor
  - Error de validación
  - Cambio de estado
    Gravedad
  - Borrado
  - Información
  - Crítica
  - Advertencia

Los administradores pueden seleccionar el componente APP para revisar rápidamente todas las notificaciones específicas para la aplicaciónen la página de Notificaciones y también en la sección notificaciones de campana. Si hay que aceptar algún nuevo permiso para las aplicaciones de Google Play, los administradores podrán aceptarlos después de hacer clic en las notificaciones en lugar de visitando la página de cada aplicación para revisar y aceptar los permisos.

Ivanti Neurons for MDM los clientes/abonados obtendrán notificaciones de aprobación de la aplicación de Android Go aunque la aplicación no se haya importado al Catálogo de aplicaciones.

### Revisar la caducidad de la contraseña del usuario y las notificaciones de cambio de ID

Los administradores pueden revisar la próxima caducidad de las contraseñas en la página **Notificaciones**. También se les notifica de la caducidad de las contraseñas desde las dos semanas anteriores hasta el día anterior, incluidos enlaces a los archivos con informes CSV que contienen las listas de los usuarios correspondientes. Una vez que la contraseña expire, ya no se generarán más notificaciones.

Asimismo, los administradores pueden revisar una notificación que enumera los usuarios cuyas ID (UID) se han detectado que han sufrido cambios durante la última sincronización de LDAP.

Borrar una notificación

Puede borrar manualmente las notificaciones de cualquier gravedad siempre que sea necesario desde la página **Notificaciones**.

1. En la página **Notificaciones**, haga clic en el icono de la columna **Acciones** para ver la notificación que desea borrar. Aparecerá la ventana **Confirmar borrado de la notificación**.
2. Haga clic en **Borrar notificación**. Una vez borrada, el estado de la notificación cambiará a **Borrada** en la columna **Estado**.El recuento total de las notificaciones que se borran se muestra en la página **Notificaciones**.

## Informes

En la página **Panel > Informes**, puede acceder a los datos de su sistema de administración unificada de puntos de conexión (UEM, Unified Endpoint Management). Por ejemplo, los administradores pueden agregar información, como Nombre de espacio del dispositivo y Atributos personalizados del dispositivo, a los informes mediante la opción de filtro correspondiente, al mismo tiempo que crear informes de dispositivos y de dispositivos bloqueados. Por consiguiente, estos informes tienen columnas para el Nombre del espacio del dispositivo y los Atributos personalizados del dispositivo, respectivamente. Los Atributos personalizados del dispositivo están disponibles en las opciones de filtrado mientras se crea un informe. Los administradores pueden elegir de la lista de claves de atributos de dispositivos personalizados que se utilizan para los dispositivos y seleccionar los operadores disponibles.

A partir de Ivanti Neurons for MDM 76, los operadores de todas las plantillas de informes tienen operadores estándar. Los operadores de las siguientes plantillas están estandarizados en esta versión:

- Panel de control > Informes > Crear informe

A continuación se describe el flujo de trabajo de un informe:

1. Elegir - seleccionar de una plantilla de informes predefinidos.
2. Definir alcance - establecer el período de tiempo de los datos del informe.
3. Establecer detalles - nombrar y personalizar su informe.
4. Ejecutar o programar - ejecutar el informe inmediatamente o crear una programación.
5. Compartir - especificar quién recibirá el informe.

**Temas relacionados**:

- [**Panel > Informes (programados)**](./Uso_de_Informes_programados.md)
- [**Panel > Informes (personalizados)**](./Uso_de_Informes_personalizados.md)

**Búsqueda rápida:** vaya a la pestaña Informes. El campo de búsqueda rápida le permite buscar a partir de las siguientes columnas, incluso si incluye espacios o caracteres especiales:

- NOMBRE
- DESCRIPCIÓN
- NOMBRE DE LA PLANTILLA

## Audit Trails

Audit Trails son un conjunto de registros cronológicos que captura las actividades realizadas sobre todas las entidades de Ivanti Neurons for MDM por parte de todos los actores, incluidos los administradores, los usuarios finales y distintos componentes del mismo sistema. A partir de la versión 80 de Ivanti Neurons for MDM, las trazas de auditorías están activados de forma predeterminada para todos los usuarios. El usuario puede optar por activar o desactivar los registros de auditoría de entrada del dispositivo. Para los usuarios que tenían activados los registros de auditoría anteriores a la versión R80, los eventos de registro permanecerán activados. Para todos los demás dispositivos, los registros de entrada estarán desactivados. Cuando vuelve a registrar un dispositivo Android, la página Audit Trails muestra el estado del dispositivo registrado actual como Acción de re-registro del dispositivo llevada a cabo y la entrada anterior como Acción de dispositivo retirado llevada a cabo. Para obtener más información, consulte [**Registro de dispositivos (iOS, macOS y Android)**](./Registro_de_dispositivos__iOS__macOS_y_Android_.md)

Las siguientes actividades serán rastreadas:

- Añadir, retirar, borrar, eliminar y actualizar dispositivos
- Forzar el ingreso a los dispositivos
- Cambiar la propiedad del dispositivo
- Crear, actualizar y eliminar el ajuste de un usuario (los ajustes Registro de dispositivos, Límite de dispositivos y Términos de servicio)
- Bloquear y desbloquear dispositivos
- Crear, editar, borrar y priorizar configuraciones
- Crear, editar y borrar políticas
- Cambios en el grupo de distribución de las configuraciones.
- Crear, editar y borrar un usuario (no incluye la creación de un usuario de LDAP).
- Crear, editar y borrar un grupo de usuarios.
- Crear, editar y borrar filtros de distribución.
- Crear, editar y borrar un servidor LDAP.
- Sincronizar con el servidor LDAP en los siguientes casos:\* Inicio sincronizado de LDAP
  - Éxito de sincronización de LDAP
  - Descartar sincronización de LDAP (ocurre cuando el número de usuarios borrados excede el valor del umbral configurado).
  - Descartar parcialmente sincronización de LDAP (ocurre cuando se producen entradas fallidas durante la sincronización).
  - Servidor LDAP añadido
  - Servidor LDAP editado
  - Servidor LDAP eliminado
  - Sincronización del servidor LDAP iniciada
  - Ha habido un error en la sincronización del servidor LDAP
  - Sincronización del servidor LDAP completada
- Crear, editar y borrar aplicaciones.
- Crear, editar y borrar configuraciones de aplicaciones.
- Crear, editar y borrar [**secuencias de comandos**](./Todas_las_secuencia_de_comandos.md).
- Eliminar la entidad LDAP de administrador.
- Modificar las preferencias de LDAP.
- Cargar el certificado LDAP.
- Cambio del icono de la aplicación.

### Activar trazas de auditorías

Debe activar la función de trazas de auditorías para capturar las actividades realizadas dentro de Ivanti Neurons for MDM.

1. Seleccione **Administrador > Infraestructura > trazas de auditorías**. Aparecerá la página **Trazas de auditorías**.
2. Haga clic en **Activar Audit Trails**. Aparecerá la ventana **¿Activar trazas de auditorías?** para confirmar que desea activar las trazas de auditorías.
3. En la ventana **¿Activar trazas de auditorías?**, haga clic en **Activar trazas de auditorías**una vez que la active, no podrá desactivar la función Trazas de auditorías. Para desactivarla, contacte con la asistencia técnica.
4. En el campo **Exportar trazas de auditorías**, deslice la barra de alternancia a **ON (Activado)** para configurar la exportación de las trazas de auditorías. La opción Exportar Audit Trails se usa para exportar y cargar toda la información sobre Audit Trails a un servidor específico. La exportación de trazas de auditorías se realiza mediante el protocolo SSH File Transfer Protocol (SFTP). El servidor debe ser accesible desde el puerto predeterminado. Los usuarios pueden configurar los ajustes de exportación para que las trazas de auditorías se suban diariamente, de forma automática, a una ubicación específica. Para más información, véase [**Exportar trazas de auditorías**](./Exportar_trazas_de_auditorías.md).

### Ver las actividades de trazas de auditoría

Puede ver las actividades supervisadas en la página **Trazas de auditorías** en **Panel**. Si un elemento de la fila se extiende más allá del ancho de la columna predeterminada y está oculto debido al borde de la columna, se mostrará una elipsis y -al pasar el ratón por encima de la elipsis- se mostrará el elemento completo de la fila como información sobre herramientas.

En esta vista se muestran los siguientes detalles:

| Nombre de la columna | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre               | Nombre del dispositivo o el nombre del ajuste del usuario. Por ejemplo, para las actividades de dispositivos, muestra el nombre del dispositivo. Al hacer clic en el hipervínculo, se navega hasta la página Detalles del dispositivo.Si hay un usuario asociado al dispositivo, el nombre de usuario del propietario del dispositivo también aparecerá debajo del nombre del dispositivo.Al hacer clic en el icono del enlace **Ir al dispositivo** que hay junto al nombre del dispositivo, se navega a la página de detalles del mismo. En la página de detalles del dispositivo, puede hacer clic en el hipervínculo **Ir a Trazas de auditoría** para ver la página de detalles de la actividad de las Trazas de auditoría. |
| Tipo                 | Tipo de actividad que se activa.Ejemplo: "Cuenta" para una actividad de inicio de sesión.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Categoría            | La categoría de la actividad.Ejemplo: configuración, política.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Última actividad     | La última actividad que se ha realizado.Ejemplo: crear, borrar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Último usuario       | El usuario que realiza la actividad                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Realizado en         | La fecha y la hora de la actividad realizada son visibles sólo en formato de 24 horas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

**Vista Detalles de la actividad**

Se accede a la vista Detalles de actividad (capa interna) haciendo clic en el enlace que hay bajo la columna de **Nombre** de la vista Entidades y se trata de una lista de todos los seguimientos de actividad histórica que afectan a esa entidad. En esta vista se muestran los siguientes detalles. Si un elemento de la fila se extiende más allá del ancho de la columna predeterminada y está oculto debido al borde de la columna, se mostrará una elipsis y -al pasar el ratón por encima de la elipsis- se mostrará el elemento completo de la fila como información sobre herramientas.

| Nombre de la columna          | Descripción                                                                                                                                                            |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Hora de la acción**         | La duración transcurrida desde la hora a la que se realizó la acción.                                                                                                  |
| **Actividad**                 | Describe la acción específica realizada.Ejemplo: aplicación añadida al App Catalog                                                                                     |
| **Realizado por**             | El usuario que realiza la actividad                                                                                                                                    |
| **Cambios - antes y después** | Haga clic en el icono para ver los detalles de la comparación de los registros de **auditoría en la ventana Cambios de los registros de auditoría - Antes y después**. |

Aparecerán los siguientes detalles en la ventana **Cambios en las trazas de auditoría - antes y después**.

| Nombre de la columna | Descripción                                                      |
| -------------------- | ---------------------------------------------------------------- |
| **Atributo**         | Aparece el nombre del atributo modificado.Ejemplo: **creadoEl**. |
| **Antes de**         | Valores de atributo se realizó antes de la acción.               |
| **Después de**       | Valores de atributo se realizó después de la acción.             |

Al hacer uso del icono del ajuste **Personalizar columnas** que aparece la parte superior derecha del encabezado de la columna, puede seleccionar o deseleccionar la casilla del nombre de la columna relevante para mostrar/ocultar las columnas en la vista Lista.

### Filtrar las actividades de trazas de auditoría

Mediante la opción **Filtros**, puede filtrar y ver la lista de actividades de registros de auditoría. A continuación se enumeran las opciones de filtros disponibles:

| Opciones de filtrados                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Filtrar por rango de fechas**                    | Seleccione el intervalo de fechas en los campos Fecha de inicio y Fecha de fin. Cuando se selecciona el intervalo, se enumeran las actividades de trazas de auditoría realizadas dentro del intervalo de fechas seleccionado. Esta opción de filtro está disponible en cualquiera de las opciones de vista (agrupada o ampliada).solo se permite seleccionar un máximo de 15 días como intervalo de fechas, con la fecha final como fecha actual. |
| **Categoría**(aplicable solo en la vista ampliada) | Seleccione el tipo de categoría de las siguientes opciones:\* Política                                                                                                                                                                                                                                                                                                                                                                            |

- Administración de dispositivos
- Administración de usuarios
- Administración de los ajustes del usuario
- LDAP
- Configuración
- Acceso al portal de administración
- Gestión de aplicaciones
- **Cumplimiento de los dispositivos Azure**La columna Categoría está oculta de manera predeterminada en la vista expandida.                                                |
  \| **Tipo**(aplicable solo en la vista ampliada)      | Seleccione las siguientes opciones para el **Tipo de entidad**:\* **Cuenta**
- **Dispositivo**
- **Autorización del registro**
- **Límite de dispositivos**
- **Condiciones del servicio**
- **Informe de compatibilidad**La columna Tipo está oculta de manera predeterminada en la vista ampliada.                                                                                                                                               |
  \| **Actividad**(aplicable solo en la vista ampliada) | Seleccione las actividades específicas que desea visualizar. A continuación se enumeran las opciones disponibles:\* **Eliminar**
- **Actualización de la distribución**
- **Forzar ingreso**
- **Borrar error de configuración**
- **Retirar**
- **Inicio de sesión**
- **Actualizar**
- **Actualizar propietario**
- **Borrar**
- **Bloquear**
- **Actualizar el cumplimiento de Intune**                                                         |
  \| **Nombre**,(aplicable solo en la vista ampliada)   | Filtre por el nombre del dispositivo o el nombre del ajuste del usuario.                                                                                                                                                                                                                                                                                                                                                                          |
  \| Realizado por                                      | Filtra según los usuarios que realizaron la acción.                                                                                                                                                                                                                                                                                                                                                                                               |
  \| Estado                                             | Filtra por el estado de acceso. A continuación se enumeran las opciones:\* **Éxito**
- **Error**                                                                                                                                                                                                                                                                                                                                                   |

el orden de visualización está basado en la hora a la que se realizó la actividad.

Al utilizar el icono del ajuste **Personalizar columnas** que aparece en la parte superior derecha del encabezado de la columna, se puede seleccionar o anular la selección de la casilla frente al nombre de la columna relevante para mostrar/ocultar las columnas en la vista Lista.

De forma predeterminada, se enumeran 50 actividades en la página. Si hay más de 50 actividades, puede hacer clic en el botón **Siguiente** que hay al final de la página para ver más actividades. Como alternativa, también puede hacer clic en la opción de la pantalla correspondiente en el campo **Mostrar** que aparece al final de la página. Por ejemplo, haga clic en **100** para mostrar la lista de las 100 actividades más recientes.

### Buscar actividades de trazas de auditoría

Mediante el campo de búsqueda, puede encontrar y ver la lista de actividades de trazas de auditoría en función de la palabra clave introducida. Actualmente, cuando se realiza una búsqueda rápida, se indexa toda la cadena, incluyendo los nombres de las propiedades. A partir de Ivanti Neurons for MDM 76, solo se indexan los valores de las propiedades. Los usuarios no están obligados a proporcionar las claves de detalles presentes en la columna de detalles cuando hagan una búsqueda rápida. La palabra clave introducida puede ser los valores aplicables a cualquiera de las siguientes columnas:

- **Actividad** (nombre del dispositivo o del usuario)
- **Tipo**
- **Categoría**
- **Realizado por**
- **Detalles**

Los valores de la columna Actividad no se pueden buscar.

El resultado mostrado también incluirá las actividades de trazas de auditoría que tengan alguna parte de los valores de la columna que coincidan con la palabra clave introducida.

## Uso de la búsqueda avanzada con Audit Trails

Puede utilizar la opción de Búsqueda avanzada para buscar audit trails basándose en reglas para identificar y ver las actividades con criterios específicos. Las opciones de reglas se pueden anidar juntas utilizando las opciones CUALQUIERA (O) o TODOS (Y). Puede utilizar los siguientes atributos para realizar la búsqueda:

- **Actividad**
- **Categoría**
- **Creado el**
- **Realizado por**
- **Realizado el**
- **Estado**
- **Tipo**

Las actividades que coinciden con la reglas se muestran debajo de la sección. Las regla se pueden crear con los operadores siguientes:

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

**Procedimiento**

1. Desde la página de Audit Trails, haga clic en el enlace **Búsqueda avanzada**.
2. Haga clic en **Cualquiera** si las actividades deben coincidir con al menos una de las reglas o en **Todas** si las actividades deben coincidir con todas las reglas.
3. Seleccione el atributo y los operadores correspondientes para crear una regla que defina los criterios de búsqueda.
4. (Opcional) Haga clic en **+** para crear reglas adicionales, si fuera necesario.
5. (Opcional) Haga clic en **Guardar** para guardar la consulta.
6. Haga clic en **Buscar**. En la página se muestran la lista de actividades de audit trail que coinciden con los criterios de búsqueda.
7. (Opcional) También puede eliminar la consulta guardada.

## Exportar Audit Trails a un archivo CSV

Puede exportar los registros de Audit Trail mediante la opción Exportar a CSV de la página Audit Trail.

**Procedimiento**

1. Vaya a **Panel** > **Audit Trails**.
2. Haga clic en el menú desplegable **Acciones** y seleccione la opción **Exportar a CSV**. También puede filtrar por rango de fechas antes de seleccionar la opción Exportar a CSV.Aparece un mensaje emergente que informa de que el informe de exportación tardará un tiempo en procesarse. Espere a que se complete la solicitud para enviar otra solicitud.
3. Haga clic en **Descargar**. Recibirá un correo electrónico con un enlace para descargar el informe.
4. (Opcional) Haga clic en **Eliminar&#x20;**&#x70;ara eliminar el informe.

Si no puede ver la página de la **Tablero**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Sistema de solo lectura
