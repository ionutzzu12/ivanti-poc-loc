---
title: Solicitar registros de depuración
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Puede enviar una solicitud a los dispositivos iOS, macOS y Android administrados en el trabajo para recuperar registros de depuración para solucionar problemas con los dispositivos. Mediante el comando «Solicitar registros de depuración» de la página de Dispositivos, las acciones y el éxito o fracaso de un evento se capturan en los registros de depuración

Esta función requiere los siguientes clientes:

- Los dispositivos iOS requieren Go 5.3.0 para iOS o versiones más recientes compatibles. Para los dispositivos migrados de Ivanti EPMM a Ivanti Neurons for MDM, esta función requiere Mobile\@Work 12.2.0 para iOS o versiones más recientes compatibles.
- Los dispositivos macOS requieren Mobile\@Work 1.5 para macOS o versiones más recientes compatibles.
- Los dispositivos Android gestionados por trabajo requieren Go 65 para Android o una versión más reciente compatible.

**Procedimiento**

1. Vaya a **Dispositivos > Dispositivos**.
2. Seleccione el dispositivo y haga clic en el enlace con el nombre del dispositivo para ir a la página de detalles del Dispositivo.
3. Haga clic en el icono

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
.
:::

4. Seleccione **Solicitar registros de depuración** y haga clic en **Aceptar**.

Una vez que se envíe la solicitud y los registros estén listos en el dispositivo, se enviará una notificación al administrador y aparecerá en los registros del dispositivo. Los registros del dispositivo también se pueden descargar haciendo clic en el enlace.
