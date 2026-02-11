---
title: Administración de actualización de Windows 10
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

Como administrador, puede ver y aprobar las actualizaciones notificadas por los dispositivos Windows 10 que desee actualizar mediante Windows 10 Update Management. Mediante esta característica, puede evitar que las actualizaciones innecesarias o no probadas se instalen en los dispositivos.

La función Administración de actualizaciones requiere que los dispositivos se configuren con la configuración **Actualizaciones de software** con la opción **Solicitar aprobación de actualización** habilitada. Solo aplicando esta configuración a los dispositivos, estos notificarán las actualizaciones para la instalación y esperarán la aprobación.

## Administrar actualizaciones

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Administración > Actualizaciones de Windows.** En la página se mostrarán los siguientes detalles de las actualizaciones.**Fecha de creación**: la fecha en la que se creó la actualización.**Título**: describe el tipo de actualización junto con el número de artículo de la base de conocimientos.Al hacer clic en la actualización, aparecerá su descripción.**Clasificación**: clasifica el tipo de actualización en una de las siguientes categorías:\* Actualizaciones críticas

- Actualizaciones de definiciones
- Actualizaciones de controladores
- Actualizaciones de seguridad
- Actualizaciones
- Actualización
- Actualizar lanzamientos**Distribución**: la distribución realizada para la actualización. Por ejemplo, indicará **Todos** cuando la actualización se haya distribuido a todos los dispositivos.Si la actualización se ha distribuido a un cierto número de grupos específico, indicará el recuento de la distribución. Por ejemplo, indicará 3 si la distribución se ha realizado solo en 3 grupos.
:::

:::WorkflowBlockItem
Además, puede ver si se ha distribuido o no una actualización en los dispositivos requeridos. Las columnas siguientes tienen números que indican el número de dispositivos presentes en distintas categorías de las actualizaciones: 

- Dispositivos elegibles
- Dispositivos instalados
- Dispositivos fallidos
- Reinice los dispositivos pendientes
  Cuando hace clic sobre cualquiera de estos números, se le dirigirá a la vista filtrada de la página Dispositivos para conocer el estado de las actualizaciones y llevar a cabo las acciones necesarias.

Revise las actualizaciones y seleccione la que desea distribuir a los dispositivos haciendo clic en la casilla de verificación de dicha actualización.
:::

:::WorkflowBlockItem
En **Acciones**, clic en **Establecer distribución**.
:::

:::WorkflowBlockItem
En la ventana **Distribuir actualización de Windows**, seleccione cualquiera de las siguientes opciones de distribución:**Todos los dispositivos**: distribuye las actualizaciones a todos los dispositivos.**Ningún dispositivo**: retiene las actualizaciones y no las distribuye a ningún dispositivo.**Personalizada**: distribuye las actualizaciones para los grupos de dispositivos especificados.
:::

:::WorkflowBlockItem
Haga clic en **Guardar**.
:::
::::

## Buscar y filtrar actualizaciones

Puede buscar y filtrar actualizaciones en función de los siguientes criterios:

- Id. del artículo de la base de conocimientos
- Distribución configurada

Filtrar en función de la Id. del artículo de la base de conocimientos:

1. En la página **Gestión de actualizaciones de Windows 10**, escriba el ID de la base de conocimientos en el campo de búsqueda rápida (solo el número en el campo Buscar).Ejemplo: para KB4056892, escriba 4056892. Aparecerá en la página la actualización que coincida con los criterios de búsqueda.Puede seguir buscando información adicional sobre la actualización haciendo clic en el enlace **Asistencia técnica** y **Más información**. Los enlaces de la **Asistencia técnica** dirigen a la página web de Microsoft que proporciona información sobre asistencia de productos para la actualización y **Más información** dirige a la página web de Microsoft que muestra más información sobre la actualización, como el artículo de la base de conocimientos.

Filtrar en función de la distribución configurada:

En la página **Gestión de actualizaciones de Windows 10**, seleccione cualquiera de las siguientes opciones de filtrado en función de la distribución configurada:

- **Todas**: se muestran todas las actualizaciones.
- **Configuradas**: se muestra la lista de actualizaciones que se han distribuido a los dispositivos.
- **No configuradas**: se muestra la lista de actualizaciones para las que no se ha especificado ninguna distribución.Los filtros Configuradas y No configuradas se basan en la distribución realizada y la distribución también puede ser **Ninguna**.

## Ver actualizaciones para un dispositivo

Para ver la información detallada sobre actualizaciones específicas para un dispositivo:

1. Vaya a **Dispositivos > Dispositivos**.
2. Haga clic en el nombre del dispositivo para visualizar la página de detalles.
3. Vaya a la pestaña **Actualizaciones**. Se mostrarán las actualizaciones para el dispositivo que estén pendientes (actualización aprobada por el administrador pero no notificada como instalada en el dispositivo), que hayan fallado y que se hayan instalado.También puede ver notificaciones sobre nuevas actualizaciones de Windows disponibles en la página «Notificaciones», en «Panel». La notificación incluye la fecha de creación de la misma, el número de notificaciones disponibles y el fin de dicha notificación. La notificación de la actualización de Windows también está visible la esquina superior derecha del Portal de administración.
