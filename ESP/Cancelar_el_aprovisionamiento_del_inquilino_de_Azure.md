---
title: Cancelar el aprovisionamiento del inquilino de Azure
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Si se habilitan múltiples Ivanti Neurons for MDM para que utilicen el mismo abonado de Azure, cancele el aprovisionamiento de todos los Ivanti Neurons for MDM. Si un solo Ivanti Neurons for MDM precisa dejar de utilizar Azure, puede deshabilitar la directiva de cumplimiento de socios únicamente para ese Ivanti Neurons for MDM.

Si el administrador desconecta una Ivanti Neurons for MDM, esta deja de informar sobre el inventario del dispositivo y el estado de cumplimiento con Azure.

Requisitos previos

- asegúrese de que todos los dispositivos sean no gestionados
- asegurarse de que todos los dispositivos sean no conformes

Procedimiento

### Microsoft

1. Inicie sesión en Microsoft Azure.
2. Acceda a Intune > Acceso condicional. Asegúrese de que la directiva de acceso condicional esté deshabilitada.

### Ivanti Neurons for MDM

1. Inicie sesión en Ivanti Neurons for MDM y vaya a Administrador.
2. En el panel de navegación izquierdo, haga clic en Microsoft Azure > Cumplimiento de los dispositivos para iOS y Android.
3. Haga clic en Desconectar la cuenta.

::Image[]{src="Resources/Images/AAD_Deprov_confirm.png" signedSrc="Resources/Images/AAD_Deprov_confirm.png" size="36" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Deprov_confirm.png" githubPath="Resources/Images/AAD_Deprov_confirm.png" position="flex-start" indent="2"}

4. Haga clic en Sí.

### Retirar un dispositivo de Azure

Al retirar el dispositivo, Ivanti Neurons for MDM informa a Azure de que el dispositivo ya no se administra y de que no es compatible.

Azure elimina la entrada del dispositivo retirado después de 90 días.

### Actividad de la cuenta de Azure almacenada en los registros

Toda la actividad se almacena en los Registros.

![](Resources/Images/AAD_logs.png)
