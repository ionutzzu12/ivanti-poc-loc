---
title: Creación de una directiva de cumplimiento de los dispositivos de los socios
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Cree una política de cumplimientos para el dispositivos asociado en Ivanti Neurons for MDM y aplique la etiqueta que desee. La política de conformidad de socios informa del estado de conformidad del dispositivo a Azure o a BeyondCorp para el acceso condicional.

Requisitos previos

Debe tener configurado un ID de abonado de Azure o un ID de Google BeyondCorp. Para obtener más información sobre Conformidad con el dispositivo asociado de Azure, consulte [**Conexión de Microsoft Azure con Ivanti Neurons for MDM**](./Conexión_de_Microsoft_Azure_con_Ivanti_Neurons_for_MDM.md).

![](<Resources/Images/Device Compliance2.png>)

Procedimiento

1. Inicie sesión en Ivanti Neurons for MDM, vaya a Configuraciones.
2. Haga clic en **Agregar** y busque la configuración **Cumplimiento del dispositivo socio** .
3. Introduzca los siguientes datos en la página **Crear configuración de conformidad de dispositivos socios**: | Elemento                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
   \| ------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Nombre**,                                                                                                               | Introduzca nombre.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
   \| **+ Añadir descripción**                                                                                                  | Introduzca una explicación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
   \| **Elegir socio**                                                                                                          | Seleccione **Conformidad con Microsoft Azure**. o **Google BeyondCorp Compliance: beta**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   \| **Establecimiento de la configuración**Informar del estado de conformidad a Azure para dispositivos iOS, macOS y Android. | Está activado de manera predeterminada. Si no ve este campo, debe configurar su ID de abonado de Azure.Si la opción Informar del estado de conformidad de dispositivos iOS, macOS y Android está activada y la política de conformidad se aplica al cliente, este mostrará "Acceso a Microsoft 365" en los dispositivos en Configuración. Se informa del estado de cumplimiento del dispositivo cuando:\* el dispositivo no es compatible
   - el dispositivo es compatible
   - el dispositivo vuelve a ser compatible
   - pases de 24 horas. Si no hay cambios en el estado, se envía un informe una vez por semana/cada siete días. |
     \| Informar del estado de conformidad a Google BeyondCorp para dispositivos iOS, macOS y Android.                            | Está activado de manera predeterminada.Se informa del estado de cumplimiento del dispositivo cuando:\* el dispositivo no es compatible
   - el dispositivo es compatible
   - el dispositivo vuelve a ser compatible
   - pases de 24 horas. Si no hay cambios en el estado, se envía un informe cada 24 horas.                                                                                                                                                                                                                                                                                                                         |
4. Haga clic en Siguiente.
5. Habilitar esta configuración está seleccionada de manera predeterminada.
6. Seleccione un nivel de distribución para la configuración. Para obtener más información sobre la distribución de la configuración, consulte [**Añadir una configuración**](./Trabajar_con_configuraciones.md).
7. Haga clic en Hecho.
