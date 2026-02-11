---
title: Permisos predeterminados del tiempo de ejecución de las aplicaciones
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** las aplicaciones creadas para Android API 23+ y con Android 6.0+ en dispositivos con Android Enterprise.

Los administradores pueden establecer la configuración de los permisos del tiempo de ejecución para las aplicaciones instaladas en dispositivos con Android Enterprise. Las aplicaciones creadas para API 23 (o posterior) y con Android 6.0 o posterior pueden solicitar a los usuarios permisos en el tiempo de ejecución. La configuración de los Permisos predeterminados del tiempo de ejecución de las aplicaciones establece el valor predeterminado para los permisos del tiempo de ejecución de estas aplicaciones. Ivanti Neurons for MDM crea esta configuración por defecto. Puede editar la configuración predeterminada del sistema o crear una nueva configuración de acuerdo con sus requisitos.

Los permisos específicos para cada aplicación prevalecen sobre la configuración general de permisos para aplicaciones. Las aplicaciones internas están sujetas a los permisos globales. No está permitido definir los permisos por aplicación para aplicaciones internas.

## Definir los permisos globales de tiempo de ejecución

Los administradores pueden editar los permisos predeterminados del tiempo de ejecución de aplicaciones y la distribución de esta configuración del siguiente modo:

Procedure**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Configuraciones**.
:::

:::WorkflowBlockItem
Lleve a cabo una de las siguientes acciones:
:::

:::WorkflowBlockItem
- Para editar la configuración predeterminada del sistema, haga clic en **Permisos predeterminados del tiempo de ejecución de las aplicaciones**y, a continuación, en **Editar**.
- Para añadir una nueva configuración, haga clic en **Añadir > Permisos predeterminados del tiempo de ejecución de las aplicaciones**.
  Introduzca un nombre para la configuración.
:::

:::WorkflowBlockItem
Introduzca una descripción.
:::

:::WorkflowBlockItem
En la sección Ajustes de la configuración, establezca uno de los siguientes permisos predeterminados del tiempo de ejecución:
:::

:::WorkflowBlockItem
- Solicitud al usuario (opción predeterminada)
- Concesión automática
- Denegación automática (usar con precaución)
  Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione la opción **Habilitar esta configuración**.Si deselecciona esta opción, la configuración no se aplicará a ningún dispositivo. Si se aplicó previamente a algún dispositivo, se eliminará.
:::

:::WorkflowBlockItem
Seleccione una de las siguientes opciones de distribución:
:::

:::WorkflowBlockItem
- Todos los dispositivos
- Ningún dispositivo (predeterminada)
- Personalizada
  Haga clic en **Hecho**.
:::
::::

## Definir permisos de tiempo de ejecución específicos para cada aplicación

Los administradores pueden definir los permisos de tiempo de ejecución predeterminados para cada aplicación individual del siguiente modo:

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Aplicaciones**.
:::

:::WorkflowBlockItem
Haga clic en el nombre de la aplicación.
:::

:::WorkflowBlockItem
Haga clic en **Configuraciones de aplicaciones > Android Enterprise**.
:::

:::WorkflowBlockItem
Haga clic en **Añadir** o en el nombre de la configuración para editar una configuración existente.
:::

:::WorkflowBlockItem
Defina las opciones de configuración como el nombre, la descripción y las restricciones.
:::

:::WorkflowBlockItem
En la sección Permisos de tiempo de ejecución, haga clic en **Administrar permisos**.
:::

:::WorkflowBlockItem
Seleccione los permisos de la ventana que aparece y haga clic en **Seleccionar**.Solo se incluyen para seleccionar los permisos peligrosos aplicables a la aplicación específica. La lista completa de los permisos peligrosos (como leer sus contactos, encontrar cuentas en el dispositivo, escribir registros de llamadas, etc.) están enumerados en [**https://developer.android.com/guide/topics/permissions/requesting.html#perm-groups.**](https://developer.android.com/guide/topics/permissions/requesting.html#perm-groups)
:::

:::WorkflowBlockItem
- Los permisos se aplican solamente cuando la aplicación los solicita.
- Los permisos no se aplican si los usuarios los han aceptado o denegado previamente.
  En la sección Permisos de tiempo de ejecución, seleccione uno de los siguientes permisos predeterminados del tiempo de ejecución:
:::

:::WorkflowBlockItem
- Predeterminado/global (opción predeterminada)
- Concesión automática
- Denegación automática (usar con precaución)
  En la sección Distribuir la configuración de esta aplicación, seleccione una de las siguientes opciones de distribución:
:::

:::WorkflowBlockItem
- A todas las personas con la aplicación
- A nadie
- Personalizada
  Haga clic en **Guardar**.
:::
::::
