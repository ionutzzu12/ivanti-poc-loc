---
title: Play Integrity (antes SafetyNet Attestation)
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

Play Integrity (antes SafetyNet) ayuda a evaluar la seguridad y compatibilidad de los dispositivos Android que utilizan las API Play Integrity de Google. Cuando está configurado, le permite analizar los dispositivos después de un intervalo de tiempo regular para determinar si el dispositivo se ha manipulado o no.

Play Integrity ahora es compatible con todas las versiones de Android.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
En la pestaña **Configuración**, haga clic en **+Añadir**.
:::

:::WorkflowBlockItem
Seleccione configuración de **Play Integrity**. Aparece la página **Configuración de Play Integrity**.
:::

:::WorkflowBlockItem
En el campo **Nombre**, introduzca un nombre adecuado para la configuración de Play Integrity.
:::

:::WorkflowBlockItem
Haga clic en el enlace +**Añadir descripción** para añadir una descripción de la configuración. Este campo es opcional.
:::

:::WorkflowBlockItem
En la sección **Ajuste de configuración**, introduzca un intervalo de tiempo mínimo (en horas) que se deberá aplicar para evaluar la seguridad y la compatibilidad de los dispositivos. El valor debe estar entre 1 y 24.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente** y seleccione una de las siguientes opciones de distribución:
:::

:::WorkflowBlockItem
- Todos los dispositivos
- Ningún dispositivo (predeterminada)
- personalizada
  Haga clic en **Hecho**.
:::
::::

Cuando los nonces Play Integrity y SafetyNet se envíen al dispositivo, el nonce Play Integrity tendrá prioridad sobre el nonce SafetyNet.
