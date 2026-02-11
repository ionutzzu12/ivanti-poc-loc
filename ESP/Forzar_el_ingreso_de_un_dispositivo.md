---
title: Forzar el ingreso de un dispositivo
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Los dispositivos deben comunicarse con Ivanti Neurons for MDM (ingresar) para proporcionar y recibir información. Los ingresos se programan a intervalos regulares. También se puede pedir a un dispositivo que ingrese a petición. Forzar el ingreso del dispositivo puede acelerar el proceso de aplicación de configuraciones, actualizar políticas, etc.

**Procedimiento**

1. Vaya a **Dispositivos > Dispositivos**.
2. Seleccione los dispositivos.
3. Haga clic en **Acciones**.
4. Seleccione **Forzar ingreso**.
5. Opcionalmente, también puede hacer clic en el enlace del nombre del dispositivo para ir a la página de detalles del Dispositivo, hacer clic en el icono **Forzar ingreso**

::Image[]{src="Forced_check_in_icon.png" signedSrc="Forced_check_in_icon.png" size="10" caption alt isUploading="false" sha initialPath="Forced_check_in_icon.png" githubPath="Forced_check_in_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
y, luego, clic en **Aceptar**.
:::

Si hay un error en el extremo del dispositivo mientras se procesa el comando de instalación de configuración durante el ingreso, Ivanti Neurons for MDM no reintentará instalar la configuración del dispositivo durante los siguientes ingresos automáticamente. El administrador tendrá que volver a intentar instalar la configuración manualmente desde la página de detalles del dispositivo. Para ello, vaya a la pestaña Configuración, seleccione la configuración del error y haga clic en **Reintentar la instalación**.
