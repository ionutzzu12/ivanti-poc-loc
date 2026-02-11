---
title: Configuración de Google BeyondCorp
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM se puede integrar con Google BeyondCorp para acceso condicional. Ivanti Neurons for MDM envía una señal de estado de legalidad del dispositivo a Google BeyondCorp. Esto garantiza que solo los dispositivos compatibles con N-MDM puedan acceder a las aplicaciones del espacio de trabajo de Google.

Requisitos previos

- Para Ivanti Neurons for MDM, debe tener una licencia Ivanti Professional Plus/Premium.
- Para Google, debe tener la licencia BeyondCorp Enterprise, Google Workspace Enterprise o Cloud Identity Premium.

Procedimiento (Google)

1. Inicie sesión en **Consola de administración de Google** con credenciales de administrador.
2. Vaya a **Dispositivos** > **Endpoints móviles** > **Configuración** > **Integraciones de terceros**.

::Image[]{src="Resources/Images/googlebc1.png" signedSrc="Resources/Images/googlebc1.png" size="27" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc1.png" githubPath="Resources/Images/googlebc1.png" position="flex-start" indent="2"}

3. Haga clic en **Seguridad y socios de MDM** > **Administrar**.

::Image[]{src="Resources/Images/googlebc2.png" signedSrc="Resources/Images/googlebc2.png" size="26" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc2.png" githubPath="Resources/Images/googlebc2.png" position="flex-start" indent="2"}

4. En la ventana **Administrar conexiones de socios** , seleccione **Ivanti**.

::Image[]{src="Resources/Images/googlebc3.png" signedSrc="Resources/Images/googlebc3.png" size="23" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc3.png" githubPath="Resources/Images/googlebc3.png" position="flex-start" indent="2"}

5. Haga clic en **Abrir conexión**.Serás redirigido a la página de inicio de sesión Ivanti Neurons for MDM; introduzca las credenciales de administrador del abonado. Una vez que inicie sesión en el abonado, verá que **Google BeyondCorp** está activado y vinculado a su cuenta de Google automáticamente.
6. En la Consola de administración de Google, vaya a **Seguridad** > **Acceso contextual** > **Niveles de acceso**.

::Image[]{src="Resources/Images/googlebc5.png" signedSrc="Resources/Images/googlebc5.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc5.png" githubPath="Resources/Images/googlebc5.png" position="flex-start" indent="2"}

7. Haga clic en **Crear nivel de acceso**.En la ventana Crear nivel de acceso, en la sección Condiciones de contexto, haga clic en **AVANZADO** y proporcione la información requerida.

::Image[]{src="Resources/Images/googlebc7.png" signedSrc="Resources/Images/googlebc7.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc7.png" githubPath="Resources/Images/googlebc7.png" position="flex-start" indent="2"}

8. Vaya a **Seguridad** > **Acceso consciente del contexto** > **Nivel de acceso**, seleccione la aplicación para la que desea asignar la política.

::Image[]{src="Resources/Images/googlebc9.png" signedSrc="Resources/Images/googlebc9.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc9.png" githubPath="Resources/Images/googlebc9.png" position="flex-start" indent="2"}

9. Haga clic en **Asignar**.
10. Desde la ventana **Seleccionar niveles de acceso**, seleccione las políticas que desea asignar y haga clic en **Guardar**.

::Image[]{src="Resources/Images/googlebc11.png" signedSrc="Resources/Images/googlebc11.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc11.png" githubPath="Resources/Images/googlebc11.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
Una vez completada la configuración anterior, puede crear la configuración de legalidad del dispositivo asociado mediante **Google BeyondCorp**.
:::

**Procedimiento (**&#x49;vanti Neurons for MD&#x4D;**)**:

1. Vaya a **Configuraciones** > **Agregar configuración**.
2. Seleccione la configuración de **Legalidad del dispositivo asociado**.
3. La página de configuración Crear legalidad de dispositivo asociado aparece en la pantalla.
   Introduzca un nombre para la configuración.
4. En la lista Elegir socio, seleccione **Google BeyondCorp**.
5. La sección Configuración aparece en la pantalla. Asegúrese de que la opción Informar estado de legalidad para dispositivos iOS y Android esté activada.
   Haga clic en **Siguiente**.
6. Seleccione **Habilitar esta configuración**.
7. Seleccione **Personalizado** para la opción de distribución.
8. Seleccione **Usuarios/Grupos de usuarios** en la opción **Distribución personalizada**.
9. En la sección **Seleccionar a continuación para distribuir esta configuración**, seleccione usuarios/grupos de usuarios de la lista.
10. Haga clic en **Hecho**.
