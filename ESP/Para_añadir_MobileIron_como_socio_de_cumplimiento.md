---
title: Para añadir MobileIron como socio de cumplimiento
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

**Requisitos previos**

- una licencia de Microsoft Intune instalada. Consulte [**Aplicar la licencia de Intune a usuarios de dispositivos**](./Aplicar_la_licencia_de_Intune_a_usuarios_de_dispositivos.md).
- usuarios creados en Microsoft Azure.
- grupos creados en Microsoft Azure.

Procedimiento

1. Inicie sesión en: [**https://endpoint.microsoft.com**](https://endpoint.microsoft.com/).
2. En el panel izquierdo de la página del centro de administración de Microsoft Endpoint Manager, haga clic en Administrador de inquilinos. Haga clic en Conectores y tokens > Administración de cumplimiento de socios.

::Image[]{src="Resources/Images/AAD_Add MI as comp partner_01.png" signedSrc="Resources/Images/AAD_Add MI as comp partner_01.png" size="54" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Add MI as comp partner_01.png" githubPath="Resources/Images/AAD_Add MI as comp partner_01.png" position="flex-start" indent="2"}

1. A la derecha del campo Buscar, haga clic en + Añadir socio de cumplimiento.

::Image[]{src="Resources/Images/AAD_Add MI as comp partner_02.png" signedSrc="Resources/Images/AAD_Add MI as comp partner_02.png" size="65" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Add MI as comp partner_02.png" githubPath="Resources/Images/AAD_Add MI as comp partner_02.png" position="flex-start" indent="2"}

1. En la pestaña Básico, seleccione MobileIron Device Compliance Cloud en la lista desplegable del campo Asociado de cumplimiento.

::Image[]{src="Resources/Images/AAD_compliance partner.png" signedSrc="Resources/Images/AAD_compliance partner.png" size="70" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_compliance partner.png" githubPath="Resources/Images/AAD_compliance partner.png" position="flex-start" indent="2"}

1. En el campo Plataforma, seleccione iOS o Android y, a continuación, haga clic en Siguiente.
2. Haga clic en la pestaña Asignaciones. En la lista desplegable Asignar a, seleccione el usuario/grupo de usuarios de dispositivos para el cual corresponde el estado de cumplimiento. Seleccione el usuario/grupo que posea la licencia.

::Image[]{src="Resources/Images/AAD_Add MI as comp partner_04.png" signedSrc="Resources/Images/AAD_Add MI as comp partner_04.png" size="19" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Add MI as comp partner_04.png" githubPath="Resources/Images/AAD_Add MI as comp partner_04.png" position="flex-start" indent="2"}

1. Seleccione Siguiente.
2. Haga clic en Crear. El nuevo socio de cumplimiento aparece en la página de administración de cumplimiento del Socio.

::Image[]{src="Resources/Images/AAD_completed Conn with Azure.png" signedSrc="Resources/Images/AAD_completed Conn with Azure.png" size="63" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_completed Conn with Azure.png" githubPath="Resources/Images/AAD_completed Conn with Azure.png" position="flex-start" indent="2"}
