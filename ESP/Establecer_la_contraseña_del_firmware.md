---
title: Establecer la contraseña del firmware
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** macOS 10.13 o versiones más recientes compatibles.

El administrador puede establecer o actualizar la contraseña del firmware (EFI) para un dispositivo macOS. La contraseña del firmware evita que el dispositivo macOS se inicie desde cualquier dispositivo de almacenamiento interno o externo que no sea el disco de inicio seleccionado por el usuario del dispositivo. Como resultado, también bloquea la posibilidad de usar la mayoría de las combinaciones de claves de inicio.

**Procedimiento**:

::::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Dispositivos**.
:::

:::WorkflowBlockItem
Para establecer o cambiar la contraseña del firmware para un solo dispositivo:
:::

:::::WorkflowBlockItem
::::WorkflowBlock
:::WorkflowBlockItem
Haga clic en el nombre de usuario con el que está asociado el dispositivo para ver la página de detalles del dispositivo.
:::

:::WorkflowBlockItem
En la sección General, amplíe **Contraseña del firmware** y haga clic en **Establecer contraseña** o en **Establecer/cambiar contraseña del firmware&#x20;**&#x64;esde el menú de Acciones del dispositivo.
:::

:::WorkflowBlockItem
En esta sección se muestra la siguiente información:

1. **Contraseña:&#x20;**&#x6C;a contraseña o una lista de posibles contraseñas.Cuando un administrador establece la contraseña del firmware, se envía el comando al dispositivo. Si el dispositivo no responde a tiempo, la contraseña se almacena temporalmente y de muestra en este campo. La nueva contraseña no entrará en vigor hasta que el dispositivo la reconozca y el dispositivo se reinicie. Hasta entonces, se mostrarán todas las posibles contraseñas. Una vez que el dispositivo se reinicie y el cambio de contraseña se reconozca, todas las contraseñas no deseadas se borrarán.
2. **Cambio pendiente:** indica si el cambio de contraseña está pendiente.
3. **Estado del comando:&#x20;**&#x69;ndica si el cambio de contraseña fue un éxito o un fracaso.
4. **Permitir ROM opcionales:** indica si las ROM opcionales se deben habilitar. Por defecto, está configurado como No.
:::
::::

Para establecer o cambiar la contraseña del firmware para más de un dispositivo:
:::::

:::WorkflowBlockItem
1. Seleccione los dispositivos.
2. Desde el menú Acciones, haga clic en **Establecer/cambiar contraseña del firmware**.
   Introduzca la contraseña actual y la nueva.Si es la primera vez, la contraseña actual se puede dejar vacía.Para restablecer la contraseña, deje vacío el campo de la contraseña nueva.
:::

:::WorkflowBlockItem
Haga clic en **Guardar**.
:::
::::::

Solo los dispositivos con versiones de macOS compatibles se actualizarán con la nueva contraseña. Los dispositivos no compatibles se omitirán.
