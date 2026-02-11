---
title: Encontrar y filtrar dispositivos
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Buscar un dispositivo**](./Encontrar_y_filtrar_dispositivos.md)
- [**Filtrar dispositivos**](./Encontrar_y_filtrar_dispositivos.md)
- [**Uso de la búsqueda avanzada**](./Encontrar_y_filtrar_dispositivos.md)
- [**Carga de las consultas de búsqueda**](./Encontrar_y_filtrar_dispositivos.md)

## Buscar un dispositivo

El Administrador de Ivanti Neurons for MDM muestra el número de grupos de usuarios duplicados y el número correspondiente de GUID para identificar los grupos duplicados, cuando se selecciona el atributo Nombre del grupo de usuarios en el generador de reglas. Además, una tabla bajo esta regla muestra la lista de los grupos de usuarios duplicados y sus detalles, como el Nombre del Grupo de Usuarios, el GUID, la Fuente y el nombre distinguido (DN).

**Procedimiento**

1. Vaya a **Dispositivos**.
2. Escriba el nombre del dispositivo en el campo **Buscar**. Se enumeran todos los dispositivos que contienen los caracteres.

## Filtrar dispositivos

La barra de navegación lateral de Filtros tiene una lista con varias secciones que le ayudan a buscar un dispositivo concreto en la lista total de dispositivos. El asistente de Administrar filtros contiene la lista de todas la secciones que puede seleccionar para que se muestren en la barra de navegación de Filtros.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Dispositivos**.
:::

:::WorkflowBlockItem
Haga clic en las casillas relevantes de las secciones que se listan en la barra de navegación lateral de Filtros.**Ejemplo**:
:::

:::WorkflowBlockItem
- Desde la sección **Usuario activo**, seleccione **Sí** para que aparezcan solo los dispositivos en los que los usuarios están en estado activo.
- Si ha asignado atributos personalizados a los dispositivos, puede filtrar los dispositivos en función de dichos atributos haciendo clic en el icono de ajustes (cog).
- Desde la sección **Estado**, seleccione **Retirado** y **iOS** para que se muestren solo los dispositivos iOS retirados.
  (Opcional) Haga clic en **Restablecer valores predeterminados** para restablecer la selección a los filtros predeterminados. La barra de navegación de Filtros muestra las secciones seleccionadas. Si desmarca todas las casillas del asistente de Administrar filtros, la barra de navegación lateral de Filtros mostrará todas las secciones.
:::

:::WorkflowBlockItem
Haga clic en cualquier lugar fuera del asistente de Administrar filtros para salir del asistente.
:::

:::WorkflowBlockItem
(Opcional) Haga clic en el icono x para cerrar la barra de navegación lateral del Filtros y haga clic en **Filtros** para volver a abrir la barra de navegación lateral.
:::
::::

:::Paragraph{listStyleType="disc" indent="2"}
Si utiliza alguna de las palabras de parada que se listan en el archivostopwords.txt, que forma parte de la configuración del servidor de Apache SOLR, las palabras no se indexarán, como resultado, las entidades que contienen las palabras de parada, no se mostrarán en los resultados de búsqueda.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Entre los ejemplos de entidades, se incluyen dispositivos, usuarios, grupos, atributos, aplicaciones, certificados, registros de auditorías, contenido y módulos de notificación.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Ejemplos de palabras de parada: a, un, si, ser, en, entre otras.
:::

## Uso de la búsqueda avanzada

Puede utilizar la opción de Búsqueda avanzada para buscar un dispositivo en función de reglas para identificar y ver los dispositivos con criterios específicos. Estas reglas se pueden crear usando los operadores correspondientes, como «comienza con», «termina con», «contiene», «no contiene», «no comienza con», «no termina con», «es menor que», «es mayor que», «está en el intervalo», «es igual a» y «no es igual a». Las opciones de reglas se pueden anidar juntas utilizando las opciones CUALQUIERA (O) o TODOS (Y). Los dispositivos que coinciden con las reglas se muestran debajo de la sección.

El Administrador de Ivanti Neurons for MDM muestra el número de grupos de usuarios duplicados y el número correspondiente de GUID para identificar los grupos duplicados, cuando se selecciona el atributo Nombre del grupo de usuarios en el generador de reglas. Además, una tabla bajo esta regla muestra la lista de los grupos de usuarios duplicados y sus detalles, como el Nombre del Grupo de Usuarios, el GUID, la Fuente y el nombre distinguido (DN).

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
En la página Dispositivos, haga clic en el enlace **Búsqueda avanzada**. Se abre el asistente de Búsqueda avanzada.
:::

:::WorkflowBlockItem
Haga clic en una de las siguientes opciones:
:::

:::WorkflowBlockItem
- **Cualquiera**: si los dispositivos tienen que cumplir al menos una de las reglas.
- **Todas**: si los dispositivos deben cumplir todas la regla
  Cree una regla que defina los criterios de búsqueda. **Por ejemplo**: "Preparado para APNS equivale a Sí".
:::

:::WorkflowBlockItem
(Opcional) Haga clic en **+** para crear reglas adicionales, si fuera necesario.
:::

:::WorkflowBlockItem
Haga clic en **Buscar**. En la página se muestran la lista de dispositivos que coinciden con los criterios de búsqueda.
:::
::::

:::Paragraph{listStyleType="disc" indent="2"}
Para los dispositivos iOS 14.0+, la ID de eSIM (EID) de un dispositivo estará disponible en la página de detalles del dispositivo. La ID de eSIM (EID) permite a los operadores asignar la SIM a un dispositivo específico. El campo de la ID de eSIM (EID) cumple con el RGPD.
:::

:::Paragraph{listStyleType="disc" indent="2"}
Dado que se añaden campos de GDPR nuevos (como Dirección IP e ID de eSIM) a las versiones de Ivanti Neurons for MDM, los administrados que ya tienen GDPR configurado deben editar el perfil de GDPR si desean ocultar los campos nuevos.
:::

:::Paragraph{listStyleType="disc" indent="2"}
La búsqueda avanzada muestra el estado del bloqueo de recuperación de un dispositivo.
:::

## Carga de las consultas de búsqueda

Puede ver la lista de consultas de búsqueda guardadas.

**Procedimiento**

1. Haga clic en Búsqueda avanzada y luego en el icono de la carpeta. La lista de las consultas de búsqueda creadas se muestra en la sección **Cargar consulta** y se muestran los detalles siguientes:\* **Nombre de la consulta**: el nombre de la consulta cargada.
   - **Contenido de la consulta** muestra el contenido de las reglas que definen la consulta de búsqueda.
   - **Acciones**: seleccione la acción que se realizará en la consulta.
2. Haga clic en **Cargar consulta** en la columna **Acciones** para ver la lista de dispositivos que coinciden con los criterios definidos en la consulta cargada.
3. Haga clic en **Eliminar** para borrar una consulta guardada.
