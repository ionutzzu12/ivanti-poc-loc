---
title: Borrar un dispositivo
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Borrar un dispositivo elimina todos los datos y devuelve el dispositivo a los ajustes predeterminados de fábrica.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Dispositivos > Dispositivos**.
:::

:::WorkflowBlockItem
Seleccione el dispositivo.
:::

:::WorkflowBlockItem
Haga clic en **Acciones** (arriba a la derecha).
:::

:::WorkflowBlockItem
Seleccione **Borrar.**
:::

:::WorkflowBlockItem
Alternativamente, también puede hacer clic en el enlace del nombre del dispositivo para ir a la página de detalles del Dispositivo y hacer clic en el icono

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start"}

. Seleccione **Borrar** y haga clic en **Aceptar**.
:::

:::WorkflowBlockItem
Por defecto, se selecciona la opción **Preservar plan de datos**.

(Opcional, aplicable a dispositivos iOS 11.3+) Seleccione la opción **Omitir configuración de proximidad**.
:::

:::WorkflowBlockItem
Seleccione la opción **Habilitar retorno al servicio** para volver a inscribir automáticamente el dispositivo después de borrar los datos, de modo que no tenga que volver a inscribir el dispositivo manualmente después de un borrado. Seleccione **Datos del perfil Wifi** en el menú desplegable. El usuario debe desactivar todos los bloqueos de activación. Además, actualmente esto solo se aplica a los dispositivos iOS 17+ inscritos en el modo DEP
:::

:::WorkflowBlockItem
Para dispositivos macOS, puede enviar un PIN de 6 dígitos al dispositivo como código de acceso. En el dispositivo, se solicita al usuario que introduzca el PIN para acceder al dispositivo. Para continuar con la acción de borrado, el usuario del dispositivo debe:1) Introducir el PIN.
2\) Seleccionar la casilla para confirmar la acción de borrado del dispositivo.
3\) Hacer clic en **Sí, borrar este dispositivo**.
:::

:::WorkflowBlockItem
Para dispositivos de ChromeOS, cuando se lleva a cabo una operación Borrar desde la página **Detalles del dispositivo** o **Lista de dispositivos**, aparece una ventana con el mensaje "Borrar un dispositivo lo devuelve a los ajustes de fábrica, que puede resultar en pérdida de datos. La acción Borrar es distinta según la plataforma" aparece en la pantalla.

1. Marque la casilla "Entiendo que Borrar no se puede deshacer" para confirmar la acción de borrar el dispositivo.
2. Haga clic en **Borrar** para borrar el dispositivo.
   El estado del dispositivo cambia a "**Borrar enviado**". El estado del dispositivo actualizado será visible después de una sincronización de dispositivo periódica.
:::
::::

En dispositivos de Android Enterprise, puede llevar a cabo la acción **Borrar** dispositivo incluso después de que se reinicie el dispositivo y que permanezca bloqueado.

Los dispositivos de Android que se encuentran en estado **Pendiente de borrar** se pueden eliminar mediante la opción **Eliminar dispositivo** que se encuentra en la página **Detalles del dispositivo**. Cuando se ha eliminado el dispositivo, éste pierde la conexión con el servidor y deja de ser compatible. El usuario debe volver a inscribir el dispositivo después de llevar a cabo el restablecimiento de los valores de fábrica.
