---
title: App Catalog de Apple
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** iOS y macOS

La configuración del Apple App Catalog gestiona el acceso al Apple App Catalog a través de un clip web. A partir de la versión 83 de Ivanti Neurons for MDM, puede transicionar a la experiencia nativa de Apps\@Work desde la aplicación Go. Para abonados nuevos, la configuración de webclip de Apps\@work no se distribuye por defecto para dispositivos de iOS que estén instalados mediante iReg o un cliente. El administrador debe distribuir manualmente la configuración de webclip en los dispositivos que estén registrados mediante iReg o cliente.

El resultado de la búsqueda el webclip de Apps\@Work muestra solo 10 aplicaciones en los dispositivos iOS y iPad, aunque la solicitud de búsqueda tenga como parámetro filas superiores a 10.

**Procedimiento**

Los administradores pueden editar la distribución de esta configuración definida por el sistema del siguiente modo:

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Configuraciones**.
:::

:::WorkflowBlockItem
Haga clic en **Apple App Catalog**.
:::

:::WorkflowBlockItem
Haga clic en **Editar distribución**.
:::

:::WorkflowBlockItem
Seleccione una de las siguientes opciones de distribución:
:::

:::WorkflowBlockItem
- Todos los dispositivos: se enviará esta configuración a todos los dispositivos compatibles.
- Ningún dispositivo: se desactiva el acceso al App Catalog de Apple o se lanzará esta configuración para una posterior distribución.
- Predeterminada: se definen los grupos de dispositivos específicos a los que se enviará esta configuración.
  Haga clic en **Guardar**.
:::
::::
